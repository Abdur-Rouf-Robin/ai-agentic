# AI Agentic

## chapter 1 LLM fundamentals

- a large language model continues text. it predicts the next token from the tokens it has seen
- training sets the weights. inference is a forward pass that picks or samples the next token
- temperature near 0 is steadier. higher temperature is more varied and less reliable for a number
- a confident wrong answer is a hallucination. we check facts against a system we trust
- the model is not a database and it is not the calculator for money
- the demurrage figure comes from the laytime function. the model may explain the sentence around it
- these notes are the subject. the three products do not yet call a model for port calls

```text
user: what is demurrage on port call 42?
bad: ask the model to remember the row
good: our code loads the row, calls laytime(), and the model may phrase the result
```

- the good path can fail closed. no row, no number, the reply says it does not know

- homework of chapter 1
```text
// 1a  who computes 7500 for 72 allowed, 84 used, 15000 a day
// 1b  what temperature we want for a money explanation
// 1c  the word for a confident answer that is not true
```

## chapter 2 Tokens and the context window

- a token = a piece of text, often part of a word
- the context window = the maximum tokens the model can see at once
- the window holds the instructions, the retrieved text, and the answer it is writing
- tokens at the start fall out when the window is full. a long chat forgets the first rule
- we pay and we wait in proportion to tokens in plus tokens out
- a rough English estimate is characters divided by 4. the provider's tokenizer is the real count

```ts
function roughTokens(text: string): number {
  return Math.ceil(text.length / 4);
}
```

- a 12,000 character contract is about 3,000 tokens, before the instructions
- we put the rule and the few retrieved rows in the window. we do not paste the whole database
- the answer is short on purpose. a long answer spends the window and the bill

- homework of chapter 2
```ts
// 2a  rough tokens of a 400 character prompt
// 2b  three things that spend the window
// 2c  what happens to the first message when the window is full
```

## chapter 3 Prompt engineering

- a prompt = the instruction plus the evidence
- the system message is ours. the role, the task, the output shape, and the rule to say "I do not know"
- the user message is data. we do not paste user text into the system message
- untrusted text stays labeled as data
- one example in the prompt is one-shot. two or three is few-shot. we use an example when the format is easy to miss
- a reason the model writes is not proof. a source id is a check we can do in code

```ts
const system = [
  "You answer questions about a port call.",
  "Use only the JSON in the user message.",
  "If the JSON does not contain the fact, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
```

- the user's question and the rows go in the user message as JSON
- we do not put a secret in the system message. prompts are logged more often than password fields

- homework of chapter 3
```ts
// 3a  which lines belong in the system message
// 3b  add the sentence that forces "I do not know"
// 3c  where the vessel name from the user goes
```

## chapter 4 Structured outputs

- free text is hard to code against
- a schema is a contract. Zod is the same tool we use on a POST body
- we ask for JSON that matches the schema, or we parse and retry once
- if it still fails, we return an error. we do not guess the missing field
- the model is another untrusted caller

```ts
import { z } from "zod";

const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});

function readAnswer(raw: unknown) {
  return Answer.parse(raw);
}
```

- `sourceId` null means there was nothing to cite
- a number field uses `z.number()`, and we still compare a money field to the function result
- parse throws on a missing key. the route turns that into an error the user can see

- homework of chapter 4
```ts
// 4a  a schema for winner: string, confidence: number from 0 to 1
// 4b  what we do when parse throws
// 4c  why the model does not get to skip the schema
```

## chapter 5 Embeddings and vector databases

- an embedding = a list of numbers that stands for a piece of text
- similar text lands near each other. we usually measure cosine distance
- the embedding model and the chat model are different
- we do not mix vectors from two embedding models in one index
- an embedding is not a summary a person can read
- a vector database stores the lists and finds the nearest ones
- Postgres can do this with a vector extension. a separate product is optional
- we store the original text and the source id beside the vector
- we filter by tenant before the search. company A's notes are not neighbours for company B
- we have not run a dedicated vector cluster. Postgres is the database we already operate

```ts
function cosine(a: number[], b: number[]): number {
  let dot = 0;
  let na = 0;
  let nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i];
    na += a[i] * a[i];
    nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
```

- cosine 1 means the same direction
- the columns beside the vector are the text and the source id, plus the tenant id we filter on

- homework of chapter 5
```ts
// 5a  why two vendors' vectors cannot share an index
// 5b  the columns stored beside the vector
// 5c  why the tenant filter happens before the nearest-neighbour search
```

## chapter 6 RAG and chunking

- RAG = search our own text, put the best pieces in the prompt, then let the model answer from those pieces
- the model was not trained on today's port call. RAG is how it sees it
- the answer cites a source id. if the search returns nothing, the answer is that we do not know
- RAG does not run SQL. a tool does that, and the tool is our code
- a chunk = the piece we embed
- too small and the sentence loses its meaning. too large and the window fills with one document
- split on headings or paragraphs. a small overlap keeps a fact on the boundary in two chunks
- every chunk stores the document id, the heading, and the tenant

```ts
async function answerQuestion(question: string, tenantId: string) {
  const chunks = await searchChunks({ tenantId, question, limit: 4 });
  if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
  const raw = await model.complete({
    system: "Answer only from the chunks. Include sourceId.",
    user: JSON.stringify({ question, chunks }),
  });
  return Answer.parse(raw);
}
```

- the four steps are embed the question, filter the tenant, take the top chunks, parse the JSON
- a 20-page contract is not one vector. it is many chunks with one document id

- homework of chapter 6
```ts
// 6a  the reply when the search is empty
// 6b  the metadata on a chunk
// 6c  why one vector for a whole charter party is a weak chunk
```

## chapter 7 Reranking

- the first search is fast and approximate
- a reranker reads the question and each candidate and scores them again
- we retrieve 20 and rerank to 4. we do not rerank the whole table
- the winners are what enter the prompt
- this is worth the cost when the wrong paragraph would make the answer wrong

```text
search -> 20 chunks
rerank -> 4 chunks
prompt -> those 4, with their source ids
```

- the reranker is another model call. it spends tokens or its own compute. that is why the list is short
- if the first search missed the right paragraph, reranking cannot invent it. the fix is chunking or the query, not a bigger rerank

- homework of chapter 7
```text
// 7a  the two numbers: how many we retrieve, how many we keep
// 7b  why we do not rerank every row
// 7c  what reranking cannot fix
```

## chapter 8 Tool calling and MCP

- a tool = a function we wrote. the model may ask us to run it. our process runs it
- the model does not get a shell, a database password, or a way past a guard
- the arguments are untrusted JSON. Zod checks them
- the tool returns data. the model may then write a sentence
- a money figure still comes from laytime(), not from the model's arithmetic
- MCP is a standard shape for advertising tools to a client. a server lists tools. a host calls them
- MCP does not add trust. a tool on MCP is still our function, with the same permission check
- we treat an MCP tool like a route. schema in, auth, then the service

```ts
const LaytimeArgs = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});

const tools = {
  laytime: (raw: unknown) => laytime(LaytimeArgs.parse(raw)),
};
```

- 72, 84, and 15000 must return 7500 from the function
- the model is not allowed to invent that 7500

- homework of chapter 8
```ts
// 8a  what the tool returns for 72, 84, 15000
// 8b  which part Zod is responsible for
// 8c  what MCP standardizes, and what it does not replace
```

## chapter 9 ReAct, planning, and reflection

- ReAct = reason, act, observe, then repeat
- the model writes a next step. we run a tool. we append the result. the model continues
- we cap the steps. a loop that never stops is a bug and a bill
- we stop when the final answer passes Zod, or when the step limit is hit
- a plan = a list of steps before any tool runs. useful when the order matters
- reflection = a second pass that checks the draft against the sources
- both cost tokens. we use them when a wrong answer is expensive
- a reflection that only says "looks good" is not a check. the check is a source id that exists, or a number that matches the function

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  const value = tools[turn.tool](turn.args);
  messages.push({ role: "tool", content: JSON.stringify(value) });
}
throw new Error("step limit");
```

- our service owns the loop. the model is a call inside it
- compare two contracts and cite both: a plan helps. spell a name that is already in the JSON: a plan is wasted tokens

- homework of chapter 9
```ts
// 9a  what we append after the tool runs
// 9b  what we do on step 5 if the limit is 4
// 9c  a task that needs a plan, and a task that does not
```

## chapter 10 Memory, agents, and orchestration

- the window is short memory. it dies when the chat ends or when it overflows
- long memory is a row we store. a summary, a preference, a document id
- we store a summary we can read later. we do not keep every raw token forever by default
- memory is per user or per tenant. it is not global
- a memory write is a tool with permission
- several prompts with different jobs are still functions. they do not gain authority by being called agents
- more agents means more tokens and more places to drop a fact
- we start with one loop and a laytime tool. a second role is a check we can test, such as "every number has a source id"
- orchestration = who runs the loop. that is our Nest service
- the service holds the step count, the timeout, the tenant id, and the logs
- the model never opens Prisma itself
- a slow loop can be a BullMQ job. the HTTP request returns a job id

```text
user -> Nest (role, tenant, step count) -> search or tool -> model -> Zod
```

- Nest increments the step counter. the model does not
- a second agent that only restates the first answer is a cost, not a design

- homework of chapter 10
```text
// 10a  which memory answers "what did we decide about despatch yesterday"
// 10b  why that row is scoped to the tenant
// 10c  who increments the step counter
// 10d  one reason to add a checker, and one reason not to add four agents on day one
```

## chapter 11 Guardrails and evals

- a guardrail = a check around the model
- before the call: may this user ask about this tenant
- on the arguments: does Zod accept them
- after the call: does the answer cite a source we retrieved. does the money equal the tool result
- untrusted text can try to override the instruction. the defense is not a clever sentence
- the defense is that tools have permissions, and numbers are checked against code
- we do not list trick phrases. a filter catches yesterday's wording
- an eval = a test set. each case has an input, the allowed sources, and the expected fact
- we score citations and exact facts. we do not score "sounds fluent"
- we run the eval when we change the prompt, the chunk size, or the model
- a small set lives next to the code, the same way the laytime tests do

```ts
const cases = [
  { question: "Demurrage if allowed is 72 and used is 84 at 15000 a day?", expect: 7500 },
  { question: "Demurrage for a port call that does not exist?", expect: "I do not know." },
];
```

- the first case must match the function, not a paragraph
- the second case is the empty-search reply

- homework of chapter 11
```ts
// 11a  the three checks: before, on the arguments, after
// 11b  where the demurrage number must come from
// 11c  write one case whose right answer is "I do not know."
// 11d  why "the paragraph looks confident" is not a score
```

## chapter 12 Tracing and fine-tuning

- a trace = the log of one question
- it has the retrieval ids, the tool names, the token counts, and whether Zod passed
- we need it when an answer is wrong and we have to see which chunk was used
- we do not log a password, a TOTP secret, or a full contract if the log store is wider than the app
- this is a request id, plus the model steps
- fine-tuning continues training on our examples. it changes weights
- LoRA trains a small add-on instead of every weight. it is cheaper. it is still a model we must host and evaluate
- fine-tuning does not replace retrieval. it will not know a port call created this morning
- RAG is for facts that change. a fine-tune is for a format we cannot get any other way, and only after an eval
- we have not fine-tuned a model for these products

```text
trace: requestId, tenantId, sourceIds, toolName, toolResult, tokensIn, tokensOut, parsed=true
```

- if the answer is wrong we want the source ids and the tool result
- a vessel name that changed this morning is a retrieval problem, not a LoRA problem

- homework of chapter 12
```text
// 12a  four fields on a trace
// 12b  two fields we leave out
// 12c  a new port call today. RAG or a fine-tune
// 12d  what LoRA saves us from training
```
