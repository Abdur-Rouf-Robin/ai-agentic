# llm

Revise this for an AI viva. Same shape as the JavaScript notes: a fact, a small piece of code, then homework.

Be honest about the boundary. You ship TypeScript, NestJS, and Postgres. You can explain an LLM system and wire a safe tool call. Do not describe a model cluster, a fine-tune, or a vector database you have not run.

A model predicts the next token. It does not look up your database unless you build that path. The path is retrieval, or a tool that runs your own code.

## LLM fundamentals

- a large language model is a function from tokens so far to the next token
- it was trained to continue text. It was not trained to be a database of your port calls
- temperature near 0 is more repeatable. Higher temperature is more varied and worse for a money figure
- you judge the result with a test, not with a feeling

Say this: the model writes a likely continuation. If the number matters, my code computes the number.

### homework

- one sentence on what the model was trained to do
- one sentence on who computes demurrage: the model, or the laytime function

## Tokens and the context window

- a token is a piece of a word, not always a whole word
- the context window is the maximum tokens the model can see at once: the instructions, the retrieved text, and the answer it is writing
- tokens at the start can fall out when the window is full. That is why a long chat forgets the first rule
- you pay and you wait in proportion to tokens in plus tokens out

```ts
type ChatMessage = { role: "system" | "user" | "assistant"; content: string };

function roughBudget(messages: ChatMessage[]): number {
  const chars = messages.reduce((sum, message) => sum + message.content.length, 0);
  return Math.ceil(chars / 4);
}
```

- a character divided by 4 is only a rough English estimate. Use the provider's tokenizer when the limit matters

Say this: the window is a budget. I put the rule and the retrieved rows in that budget, and I keep the answer short.

### homework

- name the three things that spend the window
- say what happens to the first message when the window is full

## Prompt engineering

- a prompt is the instruction plus the evidence
- put the role, the task, the output shape, and the refusal in the system message
- put the user's words in the user message. Do not mix them into the system message
- untrusted text is data. It is not a new instruction
- show one good example when the format is easy to miss. That is a one-shot prompt. Two or three examples is few-shot
- ask for the answer and a short reason only if a person will read the reason. A reason the model writes is not proof

```ts
const system = [
  "You answer questions about a port call.",
  "Use only the JSON in the user message.",
  "If the JSON does not contain the fact, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
```

Say this: the system message is mine. The user message is data. I tell it to say it does not know.

### homework

- mark which lines belong in the system message and which belong in the user message
- add the sentence that forces "I do not know"

## Structured outputs

- free text is hard to code against. A schema is a contract, the same idea as Zod on the API
- ask the provider for JSON that matches a schema, or parse the text with Zod and retry once
- if it still fails, return an error to the user. Do not guess the missing field

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

Say this: Zod is the same tool I use on a POST body. The model is just another untrusted caller.

### homework

- write a schema for a match summary: winner string, confidence number from 0 to 1
- say what you do when `parse` throws

## Embeddings

- an embedding is a list of numbers that stands for a piece of text
- similar text lands near each other. The distance is usually cosine distance
- the embedding model and the chat model are different. You embed with the model you will search with, and you do not mix vectors from two embedding models in one index
- an embedding is not a summary a person can read

```ts
type Vector = number[];

function cosine(a: Vector, b: Vector): number {
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

Say this: near in this list of numbers means similar in meaning. I keep one embedding model per index.

### homework

- say why two vectors from two vendors cannot share an index
- say what cosine similarity of 1 means

## Vector databases

- a vector database stores those lists and finds the nearest ones
- Postgres can do this with a vector extension. A separate product is optional
- you still store the original text and the source id beside the vector. The vector alone cannot be shown to the user
- filter by tenant before you search. Vessel notes from company A must not be nearest-neighbors for company B

Say this: I would start with Postgres, because that is the database I already operate. I have not run a dedicated vector cluster.

### homework

- name the two columns you store beside the vector
- say why the tenant filter happens before the nearest-neighbor search

## RAG

- retrieval augmented generation means: search your own text, put the best pieces in the prompt, then let the model answer from those pieces
- the model is not trained on your port calls. RAG is how it sees them
- the answer should cite the source id. If retrieval returns nothing, the answer is "I do not know"
- RAG does not let the model run SQL. A tool does that, and the tool is your code

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

Say this: search first, then generate. No chunks, no answer. The citation is the source id.

### homework

- list the four steps: embed the question, filter the tenant, take the top chunks, parse the JSON
- say the reply when the search is empty

## Chunking

- a chunk is the piece you embed and retrieve
- too small and the sentence loses its meaning. Too large and the window fills with one document
- split on headings or paragraphs. Keep a small overlap so a fact on the boundary is in two chunks
- store the document id, the heading, and the tenant on every chunk

Say this: I chunk on structure, I overlap a little, and every chunk knows which document it came from.

### homework

- a 20-page charter party. Would you embed it as one vector?
- name the metadata on a chunk

## Reranking

- the first search is fast and approximate
- a reranker reads the question and each candidate and scores them again, more carefully, on a short list
- you retrieve 20 and rerank to 4. You do not rerank the whole table
- this is worth it when the wrong paragraph would make the answer wrong

Say this: search wide, rerank narrow, put only the winners in the prompt.

### homework

- say the two numbers: how many you retrieve, how many you keep
- say why you do not rerank every row in the table

## Tool calling

- a tool is a function you wrote. The model may ask you to run it. Your process runs it
- the model does not get a shell, a database password, or the right to skip a guard
- the tool's arguments are untrusted JSON. Validate them with Zod
- the tool returns data. The model may then write a sentence about that data
- a money figure still comes from the laytime function, not from the model's arithmetic

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

Say this: the model chooses the tool. My code checks the arguments and returns the number. The model is not allowed to invent 7,500.

### homework

- 72 allowed, 84 used, 15,000 a day. What must the tool return?
- say which part Zod is responsible for

## MCP

- MCP, the Model Context Protocol, is a standard way to expose tools to a client
- a server advertises tools. A host calls them. The shape is JSON
- it does not add trust. A tool on MCP is still your function, with the same permission check
- I would treat an MCP tool like a route: schema in, auth, then the service

Say this: MCP is a plug shape for tools. The guard is still mine.

### homework

- one sentence on what MCP standardizes
- one sentence on what it does not replace

## The ReAct loop

- ReAct is reason, act, observe, then repeat
- the model writes a next step, you run a tool, you append the tool result, the model continues
- put a limit on steps. A loop that never stops is a bug and a bill
- stop when the model returns a final answer that passes Zod, or when the step limit is hit

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  const value = tools[turn.tool](turn.args);
  messages.push({ role: "tool", content: JSON.stringify(value) });
}
throw new Error("step limit");
```

Say this: I cap the loop. Each tool result goes back into the messages. The final answer still has to match the schema.

### homework

- what do you append after the tool runs?
- what do you do on step 5 if the limit is 4?

## Planning and reflection

- a plan is a list of steps before any tool runs. It helps when the task has an order
- reflection is a second pass that checks the draft against the sources
- both cost tokens. Use them when a wrong answer is expensive, not on every caption
- a reflection that only says "looks good" is not a check. The check is a test or a citation that exists

Say this: I plan when the order matters. I reflect by checking the source id, not by asking the model if it feels correct.

### homework

- name a task that needs a plan: "compare two contracts and cite both"
- name a task that does not: "spell the vessel name that is already in the JSON"

## Memory

- the window is short memory. It dies when the conversation ends or when it overflows
- long memory is a row you store: a summary, a preference, a document
- store a summary you can audit. Do not store every raw token forever by default
- memory is per user or per tenant. It is not global
- a memory write is a tool with permission, not a hidden side effect

Say this: the window forgets. A table remembers. I can show the row I stored.

### homework

- which memory answers "what did we decide about despatch in this chat yesterday"?
- why is that row scoped to the tenant?

## Multi-agent systems

- several models, or several prompts, with different jobs: one retrieves, one writes, one checks
- they are still functions. They do not get new authority because you called them agents
- more agents means more tokens and more places to drop a fact
- start with one model and tools. Split a role only when one prompt is doing two jobs badly

Say this: I would start with one loop and a laytime tool. A second agent is for a check I can test, such as "every number has a source id".

### homework

- give one reason to add a checker
- give one reason not to add four agents on day one

## Orchestration

- orchestration is who runs the loop: your Nest service, not the model
- the service holds the step count, the timeout, the tenant id, and the logs
- the model never opens Prisma itself. It calls a tool that uses the same guards as the HTTP API
- a queue is appropriate when the job is slow. The HTTP request can return a job id

Say this: Nest owns the loop. The model is a library call inside that loop.

### homework

- who increments the step counter, your service or the model?
- when would you put the loop on BullMQ instead of inside the request?

## Guardrails

- a guardrail is a check around the model
- before the call: is this user allowed to ask about this tenant?
- on the arguments: does Zod accept them?
- after the call: does the answer cite a source you retrieved? Is the money equal to the tool result?
- untrusted text can try to override the instruction. The defense is not a clever sentence. The defense is that tools have permissions, and numbers are checked against code
- do not put secrets in the prompt. The prompt is logged more often than a password field

Say this: I check the tenant, I check the tool arguments, and I check that 7,500 came from the function. I do not trust a paragraph that claims to be a new system rule.

### homework

- list the three checks: before, on the arguments, after
- say where the demurrage number must come from

## Evals

- an eval is a test set for the model path
- each case has an input, the allowed sources, and the expected fact
- you score citations and exact facts. You do not score "sounds fluent"
- run the eval when you change the prompt, the chunk size, or the model
- keep a small set in the repo, the same way laytime tests sit next to the function

```ts
const cases = [
  {
    question: "Demurrage if allowed is 72 and used is 84 at 15000 a day?",
    expect: 7500,
  },
];
```

Say this: I treat the prompt like code. A change has to pass the cases.

### homework

- write one case where the right answer is "I do not know"
- say why "the paragraph looks confident" is not a score

## Tracing

- a trace is the log of one question: the retrieval ids, the tool names, the token counts, the final parse
- you need it when an answer is wrong and you have to see which chunk was used
- do not log the raw password, the TOTP secret, or a full contract if the log store is wider than the app
- this is the same idea as a request id in Nest, plus the model steps

Say this: if the answer is wrong I want the source ids and the tool result, not a screenshot of the chat.

### homework

- list four fields on a trace
- name two fields you leave out

## Fine-tuning and LoRA

- fine-tuning continues training on your examples. It changes weights
- LoRA trains a small add-on instead of every weight. It is cheaper. It is still a new model you must host and evaluate
- fine-tuning does not replace retrieval. It will not memorize today's port call
- use it when the style or the format is stable and RAG plus a schema is not enough
- I have not fine-tuned a model for these products. I would measure a prompt and a tool call first

Say this: RAG for facts that change. A fine-tune only for a format I cannot get any other way, and only after an eval.

### homework

- a vessel name that changed this morning. RAG or a fine-tune?
- say what LoRA saves you from training

## A full spoken answer

Question: how would you let a user ask "what is the demurrage on this port call?"

Answer: Nest checks the role and the tenant. A tool loads the port call and calls the laytime function. Zod checks the arguments. The model may explain the result in a sentence. It may not invent the money. If there is no port call, the answer is that I do not know. I log the source id, the tool result, and the token count. I have not shipped this path yet. The function and the tests are the part I already trust.

## Homework for the whole file

1. Draw boxes: user, Nest, search, tool, model, Zod. Put the laytime function in the tool box.
2. Write the Zod answer schema and the cosine function from memory.
3. Say the empty-search reply out loud.
4. Explain why a fine-tune will not know a port call created today.
