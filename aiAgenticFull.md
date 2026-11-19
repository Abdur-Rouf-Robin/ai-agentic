# AI Agentic

## LLM fundamentals

- A large language model continues text. It predicts the next token from the tokens it has seen. It is not a database and it is not a calculator you can trust without a check.
- Training teaches the weights. Inference is a forward pass that samples or picks the next token.
- Temperature near 0 is repetitive and steadier. Higher temperature is more varied and less reliable.
- It will produce a confident wrong answer. That is a hallucination. You check facts against a system you trust.
- Use the model as an assistant beside Postgres. Do not use it as the source of a demurrage figure.
- A model is a well-read colleague who sometimes invents a citation. You do not let them sign the cheque.
- careful: Sending the model a question whose answer must come from your tables, and not looking the row up.
- Can the model replace the laytime function?
- No. The function is deterministic and tested. The model can explain the result. If the model and the function disagree, the function wins.

```
user: what is demurrage on port call 42?
bad: ask the model to remember
good: SQL for the number, model only to phrase the sentence
```

- homework
```
user: what is demurrage on port call 42?
bad: ask the model to remember
good: SQL for the number, model only to phrase the sentence
```

## Tokens and context window

- A token is a chunk of text, often a word or a piece of a word. The context window is how many tokens the model can see at once.
- A long Bangla word or a code identifier may be several tokens.
- The window holds the system prompt, the history, the retrieved notes, and the answer.
- Past the window, the oldest text falls off. The model does not remember it.
- You pay and you wait by the token, so you do not paste a whole repository.
- The window is a desk of a fixed size. What slides off the back is gone, however important it felt.
- careful: Pasting the whole database schema and every log into one prompt.
- Why did it forget the start of the chat?
- The early tokens were outside the window. I keep a short summary and the relevant rows, not the entire transcript.

```typescript
budget = window - answer reserve
notes must fit in the budget
```

- homework
```typescript
budget = window - answer reserve
notes must fit in the budget
```

## Prompt engineering

- A prompt is the instruction and the evidence you give the model. Good prompting is specific, and it still is not a security boundary.
- Say the task, the format, and what to do when the data is missing.
- Give a short example of the output you want. That is one-shot.
- Put the untrusted text, such as a user comment, in a clearly marked block, and tell the model it is data, not instructions.
- Judge the result with a test, not with a feeling.
- A prompt is a briefing. A briefing does not stop a stranger from slipping a second note into the folder. That second note is why you separate data from instructions.
- careful: A paragraph of adjectives and no example and no rule for missing data.
- What is one-shot versus zero-shot?
- Zero-shot is the instruction alone. One-shot includes an example. I add an example when the format keeps drifting.

```
Task: turn this port call row into two sentences.
If a field is null, say it is unknown. Do not invent a time.
Row: {json}
```

- homework
```
Task: turn this port call row into two sentences.
If a field is null, say it is unknown. Do not invent a time.
Row: {json}
```

## Structured outputs

- Structured output forces the model to return JSON that matches a schema, so your code can read it.
- Give a JSON schema: fields, types, enums.
- Reject and retry, or fail, when the parse fails. Do not eval the text.
- Zod on the result is the same habit as Zod on an HTTP body.
- The schema does not make the facts true. It makes the shape stable.
- It is a form with boxes. The person can still write a lie in a box. They cannot easily tape a novel to the form.
- careful: eval of model text.
- Why not ask for 'a JSON-ish answer'?
- Because one day the model adds a sentence before the brace and JSON.parse throws in production. A schema, or the provider's structured mode, plus Zod, is the same discipline as an API.

```typescript
const Summary = z.object({
  vessel: z.string(),
  hoursUsed: z.number().nullable(),
});
const parsed = Summary.parse(JSON.parse(modelText));
```

- homework
```typescript
const Summary = z.object({
  vessel: z.string(),
  hoursUsed: z.number().nullable(),
});
const parsed = Summary.parse(JSON.parse(modelText));
```

## Embeddings

- An embedding is a list of numbers that represents the meaning of a text, so similar texts sit near each other.
- A model turns a sentence into a vector.
- Nearness is usually cosine similarity.
- The vector is not a summary you can read. It is useful for search.
- Two sentences can be near and still disagree on a fact. You read the original text afterwards.
- An embedding is a map pin for a sentence. Nearby pins are related. The pin is not the sentence.
- careful: Treating the nearest neighbour as true without reading it.
- Is a bigger vector always better?
- Not for your data. A smaller model may be enough for short notes and is cheaper. I would measure retrieval on real questions, not pick the longest vector.

```typescript
similarity = cosine(embed(question), embed(note))
```

- homework
```typescript
similarity = cosine(embed(question), embed(note))
```

## Vector databases

- A vector database stores embeddings and finds the nearest ones quickly.
- You store the vector and the id of the original row in Postgres.
- An approximate index answers 'near' fast on millions of rows.
- Postgres with a vector extension is enough until the scale says otherwise. You already operate Postgres.
- The text itself stays in a normal table so you can show the source.
- It is an index by meaning, the way a B+ tree is an index by order.
- careful: Storing only the vector and losing the sentence you needed to show the user.
- Do I need a separate product on day one?
- Not if the corpus is small. I can rank in the application or use Postgres. I add a specialised store when the latency or the size forces it.

```
table notes(id, body, embedding)
query: nearest embedding to the question, limit 5
```

- homework
```
table notes(id, body, embedding)
query: nearest embedding to the question, limit 5
```

## RAG pipelines

- Retrieval-augmented generation looks up your documents and puts them in the prompt, so the model answers from them.
- Split the documents. Embed the chunks. Store them.
- On a question, embed the question, fetch the nearest chunks, and send those chunks plus the question.
- Tell the model to say it does not know when the chunks do not contain the answer.
- Show the source id. A demurrage answer without a port-call id is not acceptable.
- RAG is an open-book exam. The model may use the pages you put on the desk. It may not go to the library in its head.
- careful: No instruction to abstain, so the model fills a gap with a plausible hour.
- Why not fine-tune instead?
- Fine-tuning changes style and habits. It does not reliably memorise today's rows. RAG reads today's rows. Laytime numbers change. I would retrieve them.

```
question -> embed -> nearest notes -> prompt with notes -> answer + source ids
```

- homework
```
question -> embed -> nearest notes -> prompt with notes -> answer + source ids
```

## Chunking strategies

- Chunking is how you cut documents before embedding them.
- Too small, and the chunk has no context. Too large, and the question matches a paragraph that is mostly irrelevant.
- Split on headings and paragraphs before you split on a raw character count.
- Overlap a sentence so a fact on a boundary is in at least one chunk.
- Keep the port call id and the heading in metadata, not only inside the vector.
- Chunking is cutting a manual into cards. A card that starts mid-sentence will be found and still be useless.
- careful: Fixed 100-character cuts through the middle of a rule.
- What do you tune first?
- The chunk boundary and the metadata, on a list of real questions. I do not tune the model first.

```typescript
chunk = one section, about 400 to 800 tokens, 50 tokens overlap
metadata: { portCallId, heading }
```

- homework
```typescript
chunk = one section, about 400 to 800 tokens, 50 tokens overlap
metadata: { portCallId, heading }
```

## Reranking

- Reranking takes the nearest chunks and scores them again with a slower, more careful model.
- The first search is fast and approximate. It returns 30 chunks.
- A reranker reads the question and each chunk and sorts them.
- You keep the top 5 for the prompt. The window stays small and the quality goes up.
- You pay latency. Use it when the first search often puts the right page at position 12.
- The first search pulls a shelf. The reranker reads the titles and hands you the three that answer the question.
- careful: Sending all 30 chunks into the window and calling that reranking.
- When do you skip it?
- When the corpus is tiny or the first hit is already right in your tests. Reranking is a measured fix, not a default ornament.

```typescript
vector search -> 30 candidates -> rerank -> 5 into the prompt
```

- homework
```typescript
vector search -> 30 candidates -> rerank -> 5 into the prompt
```

## Tool calling

- Tool calling lets the model ask your code to run a function, such as a database read, and then use the result.
- You describe the tools: name, JSON arguments, what they do.
- The model returns a tool call. Your code runs it. You send the result back.
- The model does not touch Postgres. Your function does, with the user's permissions.
- Allowlist the tools. A tool that runs shell is not a toy.
- Tool calling is a junior who may ask the clerk for a file by number. The junior does not get the keys to the archive.
- careful: A tool with no authorisation, so the model can ask for any customer's row.
- Why not let the model write SQL?
- Because a wrong or hostile question becomes a query you did not review. A function with an id parameter and a role check is a door. Free SQL is an open wall.

```
tools: getPortCall(id) -> your Nest service, with the caller's role
the model never receives a database URL
```

- homework
```
tools: getPortCall(id) -> your Nest service, with the caller's role
the model never receives a database URL
```

## MCP

- MCP, the Model Context Protocol, is a standard way for an assistant to talk to tools and data sources.
- A server exposes tools, resources, and prompts.
- A client, the assistant, calls those tools over the protocol.
- It is the same idea as tool calling, with a shared shape so many clients can use one server.
- The security question does not change. The tool still runs as some user, and that user must be the right one.
- MCP is a standard plug. A standard plug can still be wired to the wrong circuit.
- careful: Exposing every table as a tool because the protocol makes it easy.
- Does MCP make the database safe?
- No. It standardises the plug. The permission check is still yours. I would expose getPortCall, not an open query.

```typescript
assistant -- MCP --> your server --> Nest / Postgres, as that user
```

- homework
```typescript
assistant -- MCP --> your server --> Nest / Postgres, as that user
```

## ReAct agent loop

- ReAct is a loop: the model reasons, acts with a tool, observes the result, and repeats until it can answer.
- Reason is a plan in words. Act is a tool call. Observe is the tool result.
- You cap the steps. A loop that may call tools forever will.
- Each observation should be short. Do not feed a whole table back.
- Log every step. You will need to explain a wrong answer.
- It is a person with a radio. They think, they ask a question on the radio, they listen, they think again. You take the radio away after a fixed number of calls.
- careful: No step limit, and a tool that can call the model again.
- What is the stop condition?
- The model returns a final answer, or the step cap, or a tool error you choose not to retry. I always have the cap.

```
for step in 1..max:
  model -> thought + maybe a tool
  if no tool: return the answer
  observe = run tool
  append observation
```

- homework
```
for step in 1..max:
  model -> thought + maybe a tool
  if no tool: return the answer
  observe = run tool
  append observation
```

## Planning and reflection

- Planning is producing the steps before the tools. Reflection is looking at the result and deciding it is wrong.
- A plan is a list: find the port call, run laytime, phrase the answer.
- Reflection asks a second pass to check the answer against the tool output.
- A second pass costs tokens and can still be wrong. A unit test of the tool is stronger than a model's opinion of itself.
- Use reflection for wording. Use code for numbers.
- Planning is a shopping list. Reflection is checking the bag against the list. Neither one cooks the meal correctly if the scales are wrong.
- careful: A reflection prompt as the only test.
- Would you reflect on a money figure?
- I would compare it to the function output in code. I would not ask the model if the model feels the number is right.

```typescript
plan: lookup, calculate, explain
reflect: does the sentence's number match the tool JSON?
```

- homework
```typescript
plan: lookup, calculate, explain
reflect: does the sentence's number match the tool JSON?
```

## Agent memory

- Memory is what the agent can use later. Some of it is the window. Some of it is a store you own.
- Working memory is the current prompt.
- Episodic memory is a log of past steps or chats, summarised.
- Semantic memory is facts in your database, retrieved, not 'remembered' in the weights.
- Write a fact to Postgres when it must be true next week. Do not hope the model memorised it.
- The window is a short-term desk. Your database is the filing cabinet. The model is not the cabinet.
- careful: Telling a user the bot will remember, with no row written.
- Where do you store 'this user prefers Bangla captions'?
- In our user table. I may also put it in the prompt. The table is the memory. The prompt is a copy.

```typescript
chat summary in a row
port calls in Postgres
nothing important only inside the weights
```

- homework
```typescript
chat summary in a row
port calls in Postgres
nothing important only inside the weights
```

## Multi-agent systems

- Several agents split a job, each with a role and tools.
- One researches, one checks the calculation, one writes.
- They coordinate through messages, not through shared hope.
- More agents mean more cost and more ways to disagree.
- Start with one agent and tools. Split when one prompt is doing two jobs badly.
- It is a small team with job titles. A team of five for a one-person errand spends the day in meetings.
- careful: Agents that can all write to the database.
- Why is one agent not enough?
- Sometimes it is enough. I split when I need a checker who does not see the writer's draft, or a tool set I do not want in the same pair of hands.

```typescript
researcher may only read
calculator may only call laytime()
writer may only phrase the calculator's JSON
```

- homework
```typescript
researcher may only read
calculator may only call laytime()
writer may only phrase the calculator's JSON
```

## Agent orchestration

- Orchestration is the code that decides which agent or tool runs next. It is not the model.
- A graph or a state machine: lookup, then calculate, then explain.
- The orchestrator enforces the cap, the timeouts, and the permissions.
- The model may choose a branch only where you allow a branch.
- This is a saga again. Failures need a defined stop, not a retry forever.
- The orchestrator is the floor manager. The model is a skilled worker on one station.
- careful: A loop of agents with no state machine and no owner.
- Who is in charge?
- The orchestrator. The model is a step. If I cannot point at the code that stops the loop, I do not have an orchestration. I have a chat.

```typescript
states: retrieve -> calculate -> explain -> done
calculate can only call the pure function
```

- homework
```typescript
states: retrieve -> calculate -> explain -> done
calculate can only call the pure function
```

## Guardrails

- A guardrail is a check that blocks an input or an output that breaks a rule.
- On the way in: size limits, and a refusal if the text is trying to override the instruction in a context you do not trust.
- On the way out: the schema, a check that numbers match the tool, and a block on secrets in the answer.
- A guardrail is code. A sentence in the prompt is a wish.
- Log the block. Do not only swallow it.
- A guardrail is the barrier at the platform. A polite sign is not a barrier.
- careful: Filtering only the input and trusting the output.
- Is the system prompt a guardrail?
- It is a request. A guardrail is a check that still runs when the request is ignored. I want both, and I trust the check.

```
if (!Summary.safeParse(text).success) reject
if (answer.hours !== tool.hours) reject
```

- homework
```
if (!Summary.safeParse(text).success) reject
if (answer.hours !== tool.hours) reject
```

## Evals

- An eval is a test set for a model task. You run it when you change the prompt, the model, or the retrieval.
- Write questions you know the answer to, from real port calls and real tournaments.
- Score retrieval separately from the wording. Did the right chunk appear? Did the number match?
- Keep the set in git. A prompt change that drops the score does not ship.
- Ten hard real cases beat a hundred vague ones.
- An eval is the unit test of a prompt. If you would not merge a function without a test, do not merge a prompt without a case.
- careful: Changing models in production because a demo felt better.
- What do you measure?
- Faithfulness to the tool output, and whether the right source was retrieved. I do not measure whether the sentence sounds clever.

```typescript
case: port call 42, expected hours 84, expected demurrage 7500
fail if the answer's number differs
```

- homework
```typescript
case: port call 42, expected hours 84, expected demurrage 7500
fail if the answer's number differs
```

## Observability and tracing

- You log every step of an agent so a wrong answer can be explained.
- A trace id joins the user request, the retrieval, the tool calls, and the final text.
- Store the prompt version. 'The model got worse' is useless if you do not know which prompt.
- Do not store secrets or full payment details in the trace.
- Sentry for exceptions still applies. A model error is an exception if it breaks the request.
- A trace is the CCTV of the agent's shift. Without it you have a rumour.
- careful: Logging the entire customer record into a third-party trace product.
- The answer was wrong yesterday and right today. What do you open?
- The trace: which chunks came back, which tool result, which prompt version. I do not re-run it once and guess.

```
trace: request id, prompt version, tool name, tool args, tool result hash, token count
```

- homework
```
trace: request id, prompt version, tool name, tool args, tool result hash, token count
```

## Fine-tuning with LoRA

- Fine-tuning changes the model on your examples. LoRA trains a small set of extra weights instead of all of them.
- You use it for a format or a tone that prompting cannot hold.
- You do not use it to store facts that change, such as today's laytime.
- It needs a clean dataset and an eval. A pile of chats is not a dataset.
- RAG remains the way to inject private facts. LoRA does not replace retrieval.
- Fine-tuning is teaching a clerk a house style. It is not uploading the filing cabinet into their memory.
- careful: Fine-tuning on private data and assuming that is access control. The weights are not a permission system.
- Would you fine-tune for VMS?
- Not for the numbers. I would retrieve the row and call the function. I would consider a small tune only if a fixed phrasing had to be followed and prompts kept failing the eval.

```typescript
facts that change -> RAG or tools
stable style -> maybe LoRA, after an eval
```

- homework
```typescript
facts that change -> RAG or tools
stable style -> maybe LoRA, after an eval
```
