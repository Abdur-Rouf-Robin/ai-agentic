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

- example 1. the model does not own pc_12
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id pc_12
field vesselName = Ocean Star
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 1a  who returns 7500.0 when the inputs say so
// 1b  low temperature for that sentence
// 1c  hallucination = a confident answer that is not in the row pc_12
```

- example 2. the model does not own m_1
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id m_1
field home = Ada
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 2a  who returns 7500.0 when the inputs say so
// 2b  low temperature for that sentence
// 2c  hallucination = a confident answer that is not in the row m_1
```

- example 3. the model does not own t_9
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id t_9
field name = Rajshahi Open
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 3a  who returns 7500.0 when the inputs say so
// 3b  low temperature for that sentence
// 3c  hallucination = a confident answer that is not in the row t_9
```

- example 4. the model does not own v_4
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id v_4
field title = Episode 1
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 4a  who returns 7500.0 when the inputs say so
// 4b  low temperature for that sentence
// 4c  hallucination = a confident answer that is not in the row v_4
```

- example 5. the model does not own f_2
- it continues text. temperature near 0 for a figure
- the number 250.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id f_2
field kind = NOR
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 5a  who returns 250.0 when the inputs say so
// 5b  low temperature for that sentence
// 5c  hallucination = a confident answer that is not in the row f_2
```

- example 6. the model does not own u_3
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id u_3
field email = a@example.com
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 6a  who returns 7500.0 when the inputs say so
// 6b  low temperature for that sentence
// 6c  hallucination = a confident answer that is not in the row u_3
```

- example 7. the model does not own pay_8
- it continues text. temperature near 0 for a figure
- the number 0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id pay_8
field eventId = evt_1
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 7a  who returns 0 when the inputs say so
// 7b  low temperature for that sentence
// 7c  hallucination = a confident answer that is not in the row pay_8
```

- example 8. the model does not own room_2
- it continues text. temperature near 0 for a figure
- the number 0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id room_2
field sessionId = s_9
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 8a  who returns 0 when the inputs say so
// 8b  low temperature for that sentence
// 8c  hallucination = a confident answer that is not in the row room_2
```

- example 9. the model does not own vs_7
- it continues text. temperature near 0 for a figure
- the number 4000.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id vs_7
field name = North Wind
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 9a  who returns 4000.0 when the inputs say so
// 9b  low temperature for that sentence
// 9c  hallucination = a confident answer that is not in the row vs_7
```

- example 10. the model does not own sc_3
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id sc_3
field points = 11
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 10a  who returns 7500.0 when the inputs say so
// 10b  low temperature for that sentence
// 10c  hallucination = a confident answer that is not in the row sc_3
```

- example 11. the model does not own tm_2
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id tm_2
field name = Blue
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 11a  who returns 7500.0 when the inputs say so
// 11b  low temperature for that sentence
// 11c  hallucination = a confident answer that is not in the row tm_2
```

- example 12. the model does not own up_6
- it continues text. temperature near 0 for a figure
- the number 0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id up_6
field key = videos/u_1/a.mp4
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 12a  who returns 0 when the inputs say so
// 12b  low temperature for that sentence
// 12c  hallucination = a confident answer that is not in the row up_6
```

- example 13. the model does not own st_1
- it continues text. temperature near 0 for a figure
- the number 125000.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id st_1
field player = player_a
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 13a  who returns 125000.0 when the inputs say so
// 13b  low temperature for that sentence
// 13c  hallucination = a confident answer that is not in the row st_1
```

- example 14. the model does not own n_2
- it continues text. temperature near 0 for a figure
- the number 3000.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id n_2
field port = Chattogram
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 14a  who returns 3000.0 when the inputs say so
// 14b  low temperature for that sentence
// 14c  hallucination = a confident answer that is not in the row n_2
```

- example 15. the model does not own b_3
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id b_3
field round = semi
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 15a  who returns 7500.0 when the inputs say so
// 15b  low temperature for that sentence
// 15c  hallucination = a confident answer that is not in the row b_3
```

- example 16. the model does not own se_1
- it continues text. temperature near 0 for a figure
- the number 0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id se_1
field userId = u_3
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 16a  who returns 0 when the inputs say so
// 16b  low temperature for that sentence
// 16c  hallucination = a confident answer that is not in the row se_1
```

- example 17. the model does not own q_1
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id q_1
field name = laytime
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 17a  who returns 7500.0 when the inputs say so
// 17b  low temperature for that sentence
// 17c  hallucination = a confident answer that is not in the row q_1
```

- example 18. the model does not own r_1
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id r_1
field name = operator
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 18a  who returns 7500.0 when the inputs say so
// 18b  low temperature for that sentence
// 18c  hallucination = a confident answer that is not in the row r_1
```

- example 19. the model does not own pc_12
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id pc_12
field vesselName = Ocean Star
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 19a  who returns 7500.0 when the inputs say so
// 19b  low temperature for that sentence
// 19c  hallucination = a confident answer that is not in the row pc_12
```

- example 20. the model does not own m_1
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id m_1
field home = Ada
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 20a  who returns 7500.0 when the inputs say so
// 20b  low temperature for that sentence
// 20c  hallucination = a confident answer that is not in the row m_1
```

- example 21. the model does not own t_9
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id t_9
field name = Rajshahi Open
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 21a  who returns 7500.0 when the inputs say so
// 21b  low temperature for that sentence
// 21c  hallucination = a confident answer that is not in the row t_9
```

- example 22. the model does not own v_4
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id v_4
field title = Episode 1
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 22a  who returns 7500.0 when the inputs say so
// 22b  low temperature for that sentence
// 22c  hallucination = a confident answer that is not in the row v_4
```

- example 23. the model does not own f_2
- it continues text. temperature near 0 for a figure
- the number 250.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id f_2
field kind = NOR
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 23a  who returns 250.0 when the inputs say so
// 23b  low temperature for that sentence
// 23c  hallucination = a confident answer that is not in the row f_2
```

- example 24. the model does not own u_3
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id u_3
field email = a@example.com
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 24a  who returns 7500.0 when the inputs say so
// 24b  low temperature for that sentence
// 24c  hallucination = a confident answer that is not in the row u_3
```

- example 25. the model does not own pay_8
- it continues text. temperature near 0 for a figure
- the number 0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id pay_8
field eventId = evt_1
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 25a  who returns 0 when the inputs say so
// 25b  low temperature for that sentence
// 25c  hallucination = a confident answer that is not in the row pay_8
```

- example 26. the model does not own room_2
- it continues text. temperature near 0 for a figure
- the number 0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id room_2
field sessionId = s_9
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 26a  who returns 0 when the inputs say so
// 26b  low temperature for that sentence
// 26c  hallucination = a confident answer that is not in the row room_2
```

- example 27. the model does not own vs_7
- it continues text. temperature near 0 for a figure
- the number 4000.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id vs_7
field name = North Wind
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 27a  who returns 4000.0 when the inputs say so
// 27b  low temperature for that sentence
// 27c  hallucination = a confident answer that is not in the row vs_7
```

- example 28. the model does not own sc_3
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id sc_3
field points = 11
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 28a  who returns 7500.0 when the inputs say so
// 28b  low temperature for that sentence
// 28c  hallucination = a confident answer that is not in the row sc_3
```

- example 29. the model does not own tm_2
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id tm_2
field name = Blue
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 29a  who returns 7500.0 when the inputs say so
// 29b  low temperature for that sentence
// 29c  hallucination = a confident answer that is not in the row tm_2
```

- example 30. the model does not own up_6
- it continues text. temperature near 0 for a figure
- the number 0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id up_6
field key = videos/u_1/a.mp4
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 30a  who returns 0 when the inputs say so
// 30b  low temperature for that sentence
// 30c  hallucination = a confident answer that is not in the row up_6
```

- example 31. the model does not own st_1
- it continues text. temperature near 0 for a figure
- the number 125000.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id st_1
field player = player_a
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 31a  who returns 125000.0 when the inputs say so
// 31b  low temperature for that sentence
// 31c  hallucination = a confident answer that is not in the row st_1
```

- example 32. the model does not own n_2
- it continues text. temperature near 0 for a figure
- the number 3000.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id n_2
field port = Chattogram
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 32a  who returns 3000.0 when the inputs say so
// 32b  low temperature for that sentence
// 32c  hallucination = a confident answer that is not in the row n_2
```

- example 33. the model does not own b_3
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id b_3
field round = semi
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 33a  who returns 7500.0 when the inputs say so
// 33b  low temperature for that sentence
// 33c  hallucination = a confident answer that is not in the row b_3
```

- example 34. the model does not own se_1
- it continues text. temperature near 0 for a figure
- the number 0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id se_1
field userId = u_3
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 34a  who returns 0 when the inputs say so
// 34b  low temperature for that sentence
// 34c  hallucination = a confident answer that is not in the row se_1
```

- example 35. the model does not own q_1
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id q_1
field name = laytime
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 35a  who returns 7500.0 when the inputs say so
// 35b  low temperature for that sentence
// 35c  hallucination = a confident answer that is not in the row q_1
```

- example 36. the model does not own r_1
- it continues text. temperature near 0 for a figure
- the number 7500.0 comes from laytime when the inputs are the real ones
- no row means we say we do not know

```text
id r_1
field name = operator
bad: ask the model to remember the row
good: code loads the row and calls the function
```

- homework
```text
// 36a  who returns 7500.0 when the inputs say so
// 36b  low temperature for that sentence
// 36c  hallucination = a confident answer that is not in the row r_1
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

- example 1. rough tokens of "Ocean Star"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about pc_12 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Ocean Star"); // 2
```

- homework
```ts
// 1a  roughTokens("Ocean Star")
// 1b  instructions + row pc_12 + answer share one window
// 1c  the start of a long chat falls out when the window fills
```

- example 2. rough tokens of "Ada"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about m_1 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Ada"); // 1
```

- homework
```ts
// 2a  roughTokens("Ada")
// 2b  instructions + row m_1 + answer share one window
// 2c  the start of a long chat falls out when the window fills
```

- example 3. rough tokens of "Rajshahi Open"
- about 3 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about t_9 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Rajshahi Open"); // 3
```

- homework
```ts
// 3a  roughTokens("Rajshahi Open")
// 3b  instructions + row t_9 + answer share one window
// 3c  the start of a long chat falls out when the window fills
```

- example 4. rough tokens of "Episode 1"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about v_4 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Episode 1"); // 2
```

- homework
```ts
// 4a  roughTokens("Episode 1")
// 4b  instructions + row v_4 + answer share one window
// 4c  the start of a long chat falls out when the window fills
```

- example 5. rough tokens of "NOR"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about f_2 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("NOR"); // 1
```

- homework
```ts
// 5a  roughTokens("NOR")
// 5b  instructions + row f_2 + answer share one window
// 5c  the start of a long chat falls out when the window fills
```

- example 6. rough tokens of "a@example.com"
- about 3 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about u_3 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("a@example.com"); // 3
```

- homework
```ts
// 6a  roughTokens("a@example.com")
// 6b  instructions + row u_3 + answer share one window
// 6c  the start of a long chat falls out when the window fills
```

- example 7. rough tokens of "evt_1"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about pay_8 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("evt_1"); // 1
```

- homework
```ts
// 7a  roughTokens("evt_1")
// 7b  instructions + row pay_8 + answer share one window
// 7c  the start of a long chat falls out when the window fills
```

- example 8. rough tokens of "s_9"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about room_2 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("s_9"); // 1
```

- homework
```ts
// 8a  roughTokens("s_9")
// 8b  instructions + row room_2 + answer share one window
// 8c  the start of a long chat falls out when the window fills
```

- example 9. rough tokens of "North Wind"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about vs_7 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("North Wind"); // 2
```

- homework
```ts
// 9a  roughTokens("North Wind")
// 9b  instructions + row vs_7 + answer share one window
// 9c  the start of a long chat falls out when the window fills
```

- example 10. rough tokens of "11"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about sc_3 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("11"); // 1
```

- homework
```ts
// 10a  roughTokens("11")
// 10b  instructions + row sc_3 + answer share one window
// 10c  the start of a long chat falls out when the window fills
```

- example 11. rough tokens of "Blue"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about tm_2 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Blue"); // 1
```

- homework
```ts
// 11a  roughTokens("Blue")
// 11b  instructions + row tm_2 + answer share one window
// 11c  the start of a long chat falls out when the window fills
```

- example 12. rough tokens of "videos/u_1/a.mp4"
- about 4 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about up_6 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("videos/u_1/a.mp4"); // 4
```

- homework
```ts
// 12a  roughTokens("videos/u_1/a.mp4")
// 12b  instructions + row up_6 + answer share one window
// 12c  the start of a long chat falls out when the window fills
```

- example 13. rough tokens of "player_a"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about st_1 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("player_a"); // 2
```

- homework
```ts
// 13a  roughTokens("player_a")
// 13b  instructions + row st_1 + answer share one window
// 13c  the start of a long chat falls out when the window fills
```

- example 14. rough tokens of "Chattogram"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about n_2 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Chattogram"); // 2
```

- homework
```ts
// 14a  roughTokens("Chattogram")
// 14b  instructions + row n_2 + answer share one window
// 14c  the start of a long chat falls out when the window fills
```

- example 15. rough tokens of "semi"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about b_3 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("semi"); // 1
```

- homework
```ts
// 15a  roughTokens("semi")
// 15b  instructions + row b_3 + answer share one window
// 15c  the start of a long chat falls out when the window fills
```

- example 16. rough tokens of "u_3"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about se_1 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("u_3"); // 1
```

- homework
```ts
// 16a  roughTokens("u_3")
// 16b  instructions + row se_1 + answer share one window
// 16c  the start of a long chat falls out when the window fills
```

- example 17. rough tokens of "laytime"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about q_1 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("laytime"); // 1
```

- homework
```ts
// 17a  roughTokens("laytime")
// 17b  instructions + row q_1 + answer share one window
// 17c  the start of a long chat falls out when the window fills
```

- example 18. rough tokens of "operator"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about r_1 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("operator"); // 2
```

- homework
```ts
// 18a  roughTokens("operator")
// 18b  instructions + row r_1 + answer share one window
// 18c  the start of a long chat falls out when the window fills
```

- example 19. rough tokens of "Ocean Star"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about pc_12 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Ocean Star"); // 2
```

- homework
```ts
// 19a  roughTokens("Ocean Star")
// 19b  instructions + row pc_12 + answer share one window
// 19c  the start of a long chat falls out when the window fills
```

- example 20. rough tokens of "Ada"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about m_1 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Ada"); // 1
```

- homework
```ts
// 20a  roughTokens("Ada")
// 20b  instructions + row m_1 + answer share one window
// 20c  the start of a long chat falls out when the window fills
```

- example 21. rough tokens of "Rajshahi Open"
- about 3 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about t_9 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Rajshahi Open"); // 3
```

- homework
```ts
// 21a  roughTokens("Rajshahi Open")
// 21b  instructions + row t_9 + answer share one window
// 21c  the start of a long chat falls out when the window fills
```

- example 22. rough tokens of "Episode 1"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about v_4 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Episode 1"); // 2
```

- homework
```ts
// 22a  roughTokens("Episode 1")
// 22b  instructions + row v_4 + answer share one window
// 22c  the start of a long chat falls out when the window fills
```

- example 23. rough tokens of "NOR"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about f_2 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("NOR"); // 1
```

- homework
```ts
// 23a  roughTokens("NOR")
// 23b  instructions + row f_2 + answer share one window
// 23c  the start of a long chat falls out when the window fills
```

- example 24. rough tokens of "a@example.com"
- about 3 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about u_3 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("a@example.com"); // 3
```

- homework
```ts
// 24a  roughTokens("a@example.com")
// 24b  instructions + row u_3 + answer share one window
// 24c  the start of a long chat falls out when the window fills
```

- example 25. rough tokens of "evt_1"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about pay_8 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("evt_1"); // 1
```

- homework
```ts
// 25a  roughTokens("evt_1")
// 25b  instructions + row pay_8 + answer share one window
// 25c  the start of a long chat falls out when the window fills
```

- example 26. rough tokens of "s_9"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about room_2 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("s_9"); // 1
```

- homework
```ts
// 26a  roughTokens("s_9")
// 26b  instructions + row room_2 + answer share one window
// 26c  the start of a long chat falls out when the window fills
```

- example 27. rough tokens of "North Wind"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about vs_7 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("North Wind"); // 2
```

- homework
```ts
// 27a  roughTokens("North Wind")
// 27b  instructions + row vs_7 + answer share one window
// 27c  the start of a long chat falls out when the window fills
```

- example 28. rough tokens of "11"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about sc_3 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("11"); // 1
```

- homework
```ts
// 28a  roughTokens("11")
// 28b  instructions + row sc_3 + answer share one window
// 28c  the start of a long chat falls out when the window fills
```

- example 29. rough tokens of "Blue"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about tm_2 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Blue"); // 1
```

- homework
```ts
// 29a  roughTokens("Blue")
// 29b  instructions + row tm_2 + answer share one window
// 29c  the start of a long chat falls out when the window fills
```

- example 30. rough tokens of "videos/u_1/a.mp4"
- about 4 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about up_6 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("videos/u_1/a.mp4"); // 4
```

- homework
```ts
// 30a  roughTokens("videos/u_1/a.mp4")
// 30b  instructions + row up_6 + answer share one window
// 30c  the start of a long chat falls out when the window fills
```

- example 31. rough tokens of "player_a"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about st_1 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("player_a"); // 2
```

- homework
```ts
// 31a  roughTokens("player_a")
// 31b  instructions + row st_1 + answer share one window
// 31c  the start of a long chat falls out when the window fills
```

- example 32. rough tokens of "Chattogram"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about n_2 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("Chattogram"); // 2
```

- homework
```ts
// 32a  roughTokens("Chattogram")
// 32b  instructions + row n_2 + answer share one window
// 32c  the start of a long chat falls out when the window fills
```

- example 33. rough tokens of "semi"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about b_3 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("semi"); // 1
```

- homework
```ts
// 33a  roughTokens("semi")
// 33b  instructions + row b_3 + answer share one window
// 33c  the start of a long chat falls out when the window fills
```

- example 34. rough tokens of "u_3"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about se_1 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("u_3"); // 1
```

- homework
```ts
// 34a  roughTokens("u_3")
// 34b  instructions + row se_1 + answer share one window
// 34c  the start of a long chat falls out when the window fills
```

- example 35. rough tokens of "laytime"
- about 1 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about q_1 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("laytime"); // 1
```

- homework
```ts
// 35a  roughTokens("laytime")
// 35b  instructions + row q_1 + answer share one window
// 35c  the start of a long chat falls out when the window fills
```

- example 36. rough tokens of "operator"
- about 2 tokens by the characters/4 estimate
- the window holds instructions, evidence, and the answer
- a full database dump does not fit. a few rows about r_1 might

```ts
function roughTokens(text: string) {
  return Math.ceil(text.length / 4);
}
roughTokens("operator"); // 2
```

- homework
```ts
// 36a  roughTokens("operator")
// 36b  instructions + row r_1 + answer share one window
// 36c  the start of a long chat falls out when the window fills
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

- example 1. system text versus the user data Ocean Star
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds pc_12 and vesselName
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "pc_12", vesselName: "Ocean Star" });
```

- homework
```ts
// 1a  Ocean Star stays in the user message
// 1b  the "do not know" sentence stays in the system message
// 1c  sourceId may be pc_12
```

- example 2. system text versus the user data Ada
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds m_1 and home
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "m_1", home: "Ada" });
```

- homework
```ts
// 2a  Ada stays in the user message
// 2b  the "do not know" sentence stays in the system message
// 2c  sourceId may be m_1
```

- example 3. system text versus the user data Rajshahi Open
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds t_9 and name
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "t_9", name: "Rajshahi Open" });
```

- homework
```ts
// 3a  Rajshahi Open stays in the user message
// 3b  the "do not know" sentence stays in the system message
// 3c  sourceId may be t_9
```

- example 4. system text versus the user data Episode 1
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds v_4 and title
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "v_4", title: "Episode 1" });
```

- homework
```ts
// 4a  Episode 1 stays in the user message
// 4b  the "do not know" sentence stays in the system message
// 4c  sourceId may be v_4
```

- example 5. system text versus the user data NOR
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds f_2 and kind
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "f_2", kind: "NOR" });
```

- homework
```ts
// 5a  NOR stays in the user message
// 5b  the "do not know" sentence stays in the system message
// 5c  sourceId may be f_2
```

- example 6. system text versus the user data a@example.com
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds u_3 and email
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "u_3", email: "a@example.com" });
```

- homework
```ts
// 6a  a@example.com stays in the user message
// 6b  the "do not know" sentence stays in the system message
// 6c  sourceId may be u_3
```

- example 7. system text versus the user data evt_1
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds pay_8 and eventId
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "pay_8", eventId: "evt_1" });
```

- homework
```ts
// 7a  evt_1 stays in the user message
// 7b  the "do not know" sentence stays in the system message
// 7c  sourceId may be pay_8
```

- example 8. system text versus the user data s_9
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds room_2 and sessionId
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "room_2", sessionId: "s_9" });
```

- homework
```ts
// 8a  s_9 stays in the user message
// 8b  the "do not know" sentence stays in the system message
// 8c  sourceId may be room_2
```

- example 9. system text versus the user data North Wind
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds vs_7 and name
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "vs_7", name: "North Wind" });
```

- homework
```ts
// 9a  North Wind stays in the user message
// 9b  the "do not know" sentence stays in the system message
// 9c  sourceId may be vs_7
```

- example 10. system text versus the user data 11
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds sc_3 and points
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "sc_3", points: "11" });
```

- homework
```ts
// 10a  11 stays in the user message
// 10b  the "do not know" sentence stays in the system message
// 10c  sourceId may be sc_3
```

- example 11. system text versus the user data Blue
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds tm_2 and name
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "tm_2", name: "Blue" });
```

- homework
```ts
// 11a  Blue stays in the user message
// 11b  the "do not know" sentence stays in the system message
// 11c  sourceId may be tm_2
```

- example 12. system text versus the user data videos/u_1/a.mp4
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds up_6 and key
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "up_6", key: "videos/u_1/a.mp4" });
```

- homework
```ts
// 12a  videos/u_1/a.mp4 stays in the user message
// 12b  the "do not know" sentence stays in the system message
// 12c  sourceId may be up_6
```

- example 13. system text versus the user data player_a
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds st_1 and player
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "st_1", player: "player_a" });
```

- homework
```ts
// 13a  player_a stays in the user message
// 13b  the "do not know" sentence stays in the system message
// 13c  sourceId may be st_1
```

- example 14. system text versus the user data Chattogram
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds n_2 and port
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "n_2", port: "Chattogram" });
```

- homework
```ts
// 14a  Chattogram stays in the user message
// 14b  the "do not know" sentence stays in the system message
// 14c  sourceId may be n_2
```

- example 15. system text versus the user data semi
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds b_3 and round
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "b_3", round: "semi" });
```

- homework
```ts
// 15a  semi stays in the user message
// 15b  the "do not know" sentence stays in the system message
// 15c  sourceId may be b_3
```

- example 16. system text versus the user data u_3
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds se_1 and userId
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "se_1", userId: "u_3" });
```

- homework
```ts
// 16a  u_3 stays in the user message
// 16b  the "do not know" sentence stays in the system message
// 16c  sourceId may be se_1
```

- example 17. system text versus the user data laytime
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds q_1 and name
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "q_1", name: "laytime" });
```

- homework
```ts
// 17a  laytime stays in the user message
// 17b  the "do not know" sentence stays in the system message
// 17c  sourceId may be q_1
```

- example 18. system text versus the user data operator
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds r_1 and name
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "r_1", name: "operator" });
```

- homework
```ts
// 18a  operator stays in the user message
// 18b  the "do not know" sentence stays in the system message
// 18c  sourceId may be r_1
```

- example 19. system text versus the user data Ocean Star
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds pc_12 and vesselName
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "pc_12", vesselName: "Ocean Star" });
```

- homework
```ts
// 19a  Ocean Star stays in the user message
// 19b  the "do not know" sentence stays in the system message
// 19c  sourceId may be pc_12
```

- example 20. system text versus the user data Ada
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds m_1 and home
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "m_1", home: "Ada" });
```

- homework
```ts
// 20a  Ada stays in the user message
// 20b  the "do not know" sentence stays in the system message
// 20c  sourceId may be m_1
```

- example 21. system text versus the user data Rajshahi Open
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds t_9 and name
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "t_9", name: "Rajshahi Open" });
```

- homework
```ts
// 21a  Rajshahi Open stays in the user message
// 21b  the "do not know" sentence stays in the system message
// 21c  sourceId may be t_9
```

- example 22. system text versus the user data Episode 1
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds v_4 and title
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "v_4", title: "Episode 1" });
```

- homework
```ts
// 22a  Episode 1 stays in the user message
// 22b  the "do not know" sentence stays in the system message
// 22c  sourceId may be v_4
```

- example 23. system text versus the user data NOR
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds f_2 and kind
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "f_2", kind: "NOR" });
```

- homework
```ts
// 23a  NOR stays in the user message
// 23b  the "do not know" sentence stays in the system message
// 23c  sourceId may be f_2
```

- example 24. system text versus the user data a@example.com
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds u_3 and email
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "u_3", email: "a@example.com" });
```

- homework
```ts
// 24a  a@example.com stays in the user message
// 24b  the "do not know" sentence stays in the system message
// 24c  sourceId may be u_3
```

- example 25. system text versus the user data evt_1
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds pay_8 and eventId
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "pay_8", eventId: "evt_1" });
```

- homework
```ts
// 25a  evt_1 stays in the user message
// 25b  the "do not know" sentence stays in the system message
// 25c  sourceId may be pay_8
```

- example 26. system text versus the user data s_9
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds room_2 and sessionId
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "room_2", sessionId: "s_9" });
```

- homework
```ts
// 26a  s_9 stays in the user message
// 26b  the "do not know" sentence stays in the system message
// 26c  sourceId may be room_2
```

- example 27. system text versus the user data North Wind
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds vs_7 and name
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "vs_7", name: "North Wind" });
```

- homework
```ts
// 27a  North Wind stays in the user message
// 27b  the "do not know" sentence stays in the system message
// 27c  sourceId may be vs_7
```

- example 28. system text versus the user data 11
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds sc_3 and points
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "sc_3", points: "11" });
```

- homework
```ts
// 28a  11 stays in the user message
// 28b  the "do not know" sentence stays in the system message
// 28c  sourceId may be sc_3
```

- example 29. system text versus the user data Blue
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds tm_2 and name
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "tm_2", name: "Blue" });
```

- homework
```ts
// 29a  Blue stays in the user message
// 29b  the "do not know" sentence stays in the system message
// 29c  sourceId may be tm_2
```

- example 30. system text versus the user data videos/u_1/a.mp4
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds up_6 and key
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "up_6", key: "videos/u_1/a.mp4" });
```

- homework
```ts
// 30a  videos/u_1/a.mp4 stays in the user message
// 30b  the "do not know" sentence stays in the system message
// 30c  sourceId may be up_6
```

- example 31. system text versus the user data player_a
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds st_1 and player
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "st_1", player: "player_a" });
```

- homework
```ts
// 31a  player_a stays in the user message
// 31b  the "do not know" sentence stays in the system message
// 31c  sourceId may be st_1
```

- example 32. system text versus the user data Chattogram
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds n_2 and port
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "n_2", port: "Chattogram" });
```

- homework
```ts
// 32a  Chattogram stays in the user message
// 32b  the "do not know" sentence stays in the system message
// 32c  sourceId may be n_2
```

- example 33. system text versus the user data semi
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds b_3 and round
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "b_3", round: "semi" });
```

- homework
```ts
// 33a  semi stays in the user message
// 33b  the "do not know" sentence stays in the system message
// 33c  sourceId may be b_3
```

- example 34. system text versus the user data u_3
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds se_1 and userId
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "se_1", userId: "u_3" });
```

- homework
```ts
// 34a  u_3 stays in the user message
// 34b  the "do not know" sentence stays in the system message
// 34c  sourceId may be se_1
```

- example 35. system text versus the user data laytime
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds q_1 and name
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "q_1", name: "laytime" });
```

- homework
```ts
// 35a  laytime stays in the user message
// 35b  the "do not know" sentence stays in the system message
// 35c  sourceId may be q_1
```

- example 36. system text versus the user data operator
- system: use only the JSON, say we do not know, reply with answer and sourceId
- user JSON holds r_1 and name
- no secret in the system text

```ts
const system = [
  "Use only the JSON in the user message.",
  "If the fact is missing, say you do not know.",
  "Reply as JSON with keys answer and sourceId.",
].join(" ");
const user = JSON.stringify({ id: "r_1", name: "operator" });
```

- homework
```ts
// 36a  operator stays in the user message
// 36b  the "do not know" sentence stays in the system message
// 36c  sourceId may be r_1
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

- example 1. Zod for an answer about pc_12
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "Ocean Star", sourceId: "pc_12" });
```

- homework
```ts
// 1a  parse succeeds for sourceId pc_12
// 1b  parse throws if answer is a number
// 1c  do not invent vesselName when parse throws
```

- example 2. Zod for an answer about m_1
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "Ada", sourceId: "m_1" });
```

- homework
```ts
// 2a  parse succeeds for sourceId m_1
// 2b  parse throws if answer is a number
// 2c  do not invent home when parse throws
```

- example 3. Zod for an answer about t_9
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "Rajshahi Open", sourceId: "t_9" });
```

- homework
```ts
// 3a  parse succeeds for sourceId t_9
// 3b  parse throws if answer is a number
// 3c  do not invent name when parse throws
```

- example 4. Zod for an answer about v_4
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "Episode 1", sourceId: "v_4" });
```

- homework
```ts
// 4a  parse succeeds for sourceId v_4
// 4b  parse throws if answer is a number
// 4c  do not invent title when parse throws
```

- example 5. Zod for an answer about f_2
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "NOR", sourceId: "f_2" });
```

- homework
```ts
// 5a  parse succeeds for sourceId f_2
// 5b  parse throws if answer is a number
// 5c  do not invent kind when parse throws
```

- example 6. Zod for an answer about u_3
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "a@example.com", sourceId: "u_3" });
```

- homework
```ts
// 6a  parse succeeds for sourceId u_3
// 6b  parse throws if answer is a number
// 6c  do not invent email when parse throws
```

- example 7. Zod for an answer about pay_8
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "evt_1", sourceId: "pay_8" });
```

- homework
```ts
// 7a  parse succeeds for sourceId pay_8
// 7b  parse throws if answer is a number
// 7c  do not invent eventId when parse throws
```

- example 8. Zod for an answer about room_2
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "s_9", sourceId: "room_2" });
```

- homework
```ts
// 8a  parse succeeds for sourceId room_2
// 8b  parse throws if answer is a number
// 8c  do not invent sessionId when parse throws
```

- example 9. Zod for an answer about vs_7
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "North Wind", sourceId: "vs_7" });
```

- homework
```ts
// 9a  parse succeeds for sourceId vs_7
// 9b  parse throws if answer is a number
// 9c  do not invent name when parse throws
```

- example 10. Zod for an answer about sc_3
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "11", sourceId: "sc_3" });
```

- homework
```ts
// 10a  parse succeeds for sourceId sc_3
// 10b  parse throws if answer is a number
// 10c  do not invent points when parse throws
```

- example 11. Zod for an answer about tm_2
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "Blue", sourceId: "tm_2" });
```

- homework
```ts
// 11a  parse succeeds for sourceId tm_2
// 11b  parse throws if answer is a number
// 11c  do not invent name when parse throws
```

- example 12. Zod for an answer about up_6
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "videos/u_1/a.mp4", sourceId: "up_6" });
```

- homework
```ts
// 12a  parse succeeds for sourceId up_6
// 12b  parse throws if answer is a number
// 12c  do not invent key when parse throws
```

- example 13. Zod for an answer about st_1
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "player_a", sourceId: "st_1" });
```

- homework
```ts
// 13a  parse succeeds for sourceId st_1
// 13b  parse throws if answer is a number
// 13c  do not invent player when parse throws
```

- example 14. Zod for an answer about n_2
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "Chattogram", sourceId: "n_2" });
```

- homework
```ts
// 14a  parse succeeds for sourceId n_2
// 14b  parse throws if answer is a number
// 14c  do not invent port when parse throws
```

- example 15. Zod for an answer about b_3
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "semi", sourceId: "b_3" });
```

- homework
```ts
// 15a  parse succeeds for sourceId b_3
// 15b  parse throws if answer is a number
// 15c  do not invent round when parse throws
```

- example 16. Zod for an answer about se_1
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "u_3", sourceId: "se_1" });
```

- homework
```ts
// 16a  parse succeeds for sourceId se_1
// 16b  parse throws if answer is a number
// 16c  do not invent userId when parse throws
```

- example 17. Zod for an answer about q_1
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "laytime", sourceId: "q_1" });
```

- homework
```ts
// 17a  parse succeeds for sourceId q_1
// 17b  parse throws if answer is a number
// 17c  do not invent name when parse throws
```

- example 18. Zod for an answer about r_1
- parse throws if answer or sourceId is the wrong shape
- we do not fill a missing field ourselves
- a money field still has to match the function

```ts
const Answer = z.object({
  answer: z.string(),
  sourceId: z.string().nullable(),
});
Answer.parse({ answer: "operator", sourceId: "r_1" });
```

- homework
```ts
// 18a  parse succeeds for sourceId r_1
// 18b  parse throws if answer is a number
// 18c  do not invent name when parse throws
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

- example 1. a vector beside text Ocean Star
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and pc_12 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row pc_12 keeps text "Ocean Star"
```

- homework
```ts
// 1a  cosine 1 means the same direction
// 1b  do not mix two embedding models in the index that holds pc_12
// 1c  tenant filter first, then neighbours of "Ocean Star"
```

- example 2. a vector beside text Ada
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and m_1 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row m_1 keeps text "Ada"
```

- homework
```ts
// 2a  cosine 1 means the same direction
// 2b  do not mix two embedding models in the index that holds m_1
// 2c  tenant filter first, then neighbours of "Ada"
```

- example 3. a vector beside text Rajshahi Open
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and t_9 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row t_9 keeps text "Rajshahi Open"
```

- homework
```ts
// 3a  cosine 1 means the same direction
// 3b  do not mix two embedding models in the index that holds t_9
// 3c  tenant filter first, then neighbours of "Rajshahi Open"
```

- example 4. a vector beside text Episode 1
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and v_4 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row v_4 keeps text "Episode 1"
```

- homework
```ts
// 4a  cosine 1 means the same direction
// 4b  do not mix two embedding models in the index that holds v_4
// 4c  tenant filter first, then neighbours of "Episode 1"
```

- example 5. a vector beside text NOR
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and f_2 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row f_2 keeps text "NOR"
```

- homework
```ts
// 5a  cosine 1 means the same direction
// 5b  do not mix two embedding models in the index that holds f_2
// 5c  tenant filter first, then neighbours of "NOR"
```

- example 6. a vector beside text a@example.com
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and u_3 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row u_3 keeps text "a@example.com"
```

- homework
```ts
// 6a  cosine 1 means the same direction
// 6b  do not mix two embedding models in the index that holds u_3
// 6c  tenant filter first, then neighbours of "a@example.com"
```

- example 7. a vector beside text evt_1
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and pay_8 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row pay_8 keeps text "evt_1"
```

- homework
```ts
// 7a  cosine 1 means the same direction
// 7b  do not mix two embedding models in the index that holds pay_8
// 7c  tenant filter first, then neighbours of "evt_1"
```

- example 8. a vector beside text s_9
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and room_2 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row room_2 keeps text "s_9"
```

- homework
```ts
// 8a  cosine 1 means the same direction
// 8b  do not mix two embedding models in the index that holds room_2
// 8c  tenant filter first, then neighbours of "s_9"
```

- example 9. a vector beside text North Wind
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and vs_7 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row vs_7 keeps text "North Wind"
```

- homework
```ts
// 9a  cosine 1 means the same direction
// 9b  do not mix two embedding models in the index that holds vs_7
// 9c  tenant filter first, then neighbours of "North Wind"
```

- example 10. a vector beside text 11
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and sc_3 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row sc_3 keeps text "11"
```

- homework
```ts
// 10a  cosine 1 means the same direction
// 10b  do not mix two embedding models in the index that holds sc_3
// 10c  tenant filter first, then neighbours of "11"
```

- example 11. a vector beside text Blue
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and tm_2 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row tm_2 keeps text "Blue"
```

- homework
```ts
// 11a  cosine 1 means the same direction
// 11b  do not mix two embedding models in the index that holds tm_2
// 11c  tenant filter first, then neighbours of "Blue"
```

- example 12. a vector beside text videos/u_1/a.mp4
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and up_6 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row up_6 keeps text "videos/u_1/a.mp4"
```

- homework
```ts
// 12a  cosine 1 means the same direction
// 12b  do not mix two embedding models in the index that holds up_6
// 12c  tenant filter first, then neighbours of "videos/u_1/a.mp4"
```

- example 13. a vector beside text player_a
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and st_1 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row st_1 keeps text "player_a"
```

- homework
```ts
// 13a  cosine 1 means the same direction
// 13b  do not mix two embedding models in the index that holds st_1
// 13c  tenant filter first, then neighbours of "player_a"
```

- example 14. a vector beside text Chattogram
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and n_2 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row n_2 keeps text "Chattogram"
```

- homework
```ts
// 14a  cosine 1 means the same direction
// 14b  do not mix two embedding models in the index that holds n_2
// 14c  tenant filter first, then neighbours of "Chattogram"
```

- example 15. a vector beside text semi
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and b_3 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row b_3 keeps text "semi"
```

- homework
```ts
// 15a  cosine 1 means the same direction
// 15b  do not mix two embedding models in the index that holds b_3
// 15c  tenant filter first, then neighbours of "semi"
```

- example 16. a vector beside text u_3
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and se_1 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row se_1 keeps text "u_3"
```

- homework
```ts
// 16a  cosine 1 means the same direction
// 16b  do not mix two embedding models in the index that holds se_1
// 16c  tenant filter first, then neighbours of "u_3"
```

- example 17. a vector beside text laytime
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and q_1 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row q_1 keeps text "laytime"
```

- homework
```ts
// 17a  cosine 1 means the same direction
// 17b  do not mix two embedding models in the index that holds q_1
// 17c  tenant filter first, then neighbours of "laytime"
```

- example 18. a vector beside text operator
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and r_1 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row r_1 keeps text "operator"
```

- homework
```ts
// 18a  cosine 1 means the same direction
// 18b  do not mix two embedding models in the index that holds r_1
// 18c  tenant filter first, then neighbours of "operator"
```

- example 19. a vector beside text Ocean Star
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and pc_12 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row pc_12 keeps text "Ocean Star"
```

- homework
```ts
// 19a  cosine 1 means the same direction
// 19b  do not mix two embedding models in the index that holds pc_12
// 19c  tenant filter first, then neighbours of "Ocean Star"
```

- example 20. a vector beside text Ada
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and m_1 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row m_1 keeps text "Ada"
```

- homework
```ts
// 20a  cosine 1 means the same direction
// 20b  do not mix two embedding models in the index that holds m_1
// 20c  tenant filter first, then neighbours of "Ada"
```

- example 21. a vector beside text Rajshahi Open
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and t_9 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row t_9 keeps text "Rajshahi Open"
```

- homework
```ts
// 21a  cosine 1 means the same direction
// 21b  do not mix two embedding models in the index that holds t_9
// 21c  tenant filter first, then neighbours of "Rajshahi Open"
```

- example 22. a vector beside text Episode 1
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and v_4 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row v_4 keeps text "Episode 1"
```

- homework
```ts
// 22a  cosine 1 means the same direction
// 22b  do not mix two embedding models in the index that holds v_4
// 22c  tenant filter first, then neighbours of "Episode 1"
```

- example 23. a vector beside text NOR
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and f_2 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row f_2 keeps text "NOR"
```

- homework
```ts
// 23a  cosine 1 means the same direction
// 23b  do not mix two embedding models in the index that holds f_2
// 23c  tenant filter first, then neighbours of "NOR"
```

- example 24. a vector beside text a@example.com
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and u_3 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row u_3 keeps text "a@example.com"
```

- homework
```ts
// 24a  cosine 1 means the same direction
// 24b  do not mix two embedding models in the index that holds u_3
// 24c  tenant filter first, then neighbours of "a@example.com"
```

- example 25. a vector beside text evt_1
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and pay_8 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row pay_8 keeps text "evt_1"
```

- homework
```ts
// 25a  cosine 1 means the same direction
// 25b  do not mix two embedding models in the index that holds pay_8
// 25c  tenant filter first, then neighbours of "evt_1"
```

- example 26. a vector beside text s_9
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and room_2 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row room_2 keeps text "s_9"
```

- homework
```ts
// 26a  cosine 1 means the same direction
// 26b  do not mix two embedding models in the index that holds room_2
// 26c  tenant filter first, then neighbours of "s_9"
```

- example 27. a vector beside text North Wind
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and vs_7 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row vs_7 keeps text "North Wind"
```

- homework
```ts
// 27a  cosine 1 means the same direction
// 27b  do not mix two embedding models in the index that holds vs_7
// 27c  tenant filter first, then neighbours of "North Wind"
```

- example 28. a vector beside text 11
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and sc_3 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row sc_3 keeps text "11"
```

- homework
```ts
// 28a  cosine 1 means the same direction
// 28b  do not mix two embedding models in the index that holds sc_3
// 28c  tenant filter first, then neighbours of "11"
```

- example 29. a vector beside text Blue
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and tm_2 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row tm_2 keeps text "Blue"
```

- homework
```ts
// 29a  cosine 1 means the same direction
// 29b  do not mix two embedding models in the index that holds tm_2
// 29c  tenant filter first, then neighbours of "Blue"
```

- example 30. a vector beside text videos/u_1/a.mp4
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and up_6 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row up_6 keeps text "videos/u_1/a.mp4"
```

- homework
```ts
// 30a  cosine 1 means the same direction
// 30b  do not mix two embedding models in the index that holds up_6
// 30c  tenant filter first, then neighbours of "videos/u_1/a.mp4"
```

- example 31. a vector beside text player_a
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and st_1 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row st_1 keeps text "player_a"
```

- homework
```ts
// 31a  cosine 1 means the same direction
// 31b  do not mix two embedding models in the index that holds st_1
// 31c  tenant filter first, then neighbours of "player_a"
```

- example 32. a vector beside text Chattogram
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and n_2 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row n_2 keeps text "Chattogram"
```

- homework
```ts
// 32a  cosine 1 means the same direction
// 32b  do not mix two embedding models in the index that holds n_2
// 32c  tenant filter first, then neighbours of "Chattogram"
```

- example 33. a vector beside text semi
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and b_3 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row b_3 keeps text "semi"
```

- homework
```ts
// 33a  cosine 1 means the same direction
// 33b  do not mix two embedding models in the index that holds b_3
// 33c  tenant filter first, then neighbours of "semi"
```

- example 34. a vector beside text u_3
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and se_1 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row se_1 keeps text "u_3"
```

- homework
```ts
// 34a  cosine 1 means the same direction
// 34b  do not mix two embedding models in the index that holds se_1
// 34c  tenant filter first, then neighbours of "u_3"
```

- example 35. a vector beside text laytime
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and q_1 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row q_1 keeps text "laytime"
```

- homework
```ts
// 35a  cosine 1 means the same direction
// 35b  do not mix two embedding models in the index that holds q_1
// 35c  tenant filter first, then neighbours of "laytime"
```

- example 36. a vector beside text operator
- cosine compares two lists of numbers
- one embedding model per index
- filter tenant before nearest neighbour
- store the text and r_1 next to the vector

```ts
function cosine(a: number[], b: number[]) {
  let dot = 0, na = 0, nb = 0;
  for (let i = 0; i < a.length; i++) {
    dot += a[i] * b[i]; na += a[i] * a[i]; nb += b[i] * b[i];
  }
  return dot / (Math.sqrt(na) * Math.sqrt(nb));
}
// row r_1 keeps text "operator"
```

- homework
```ts
// 36a  cosine 1 means the same direction
// 36b  do not mix two embedding models in the index that holds r_1
// 36c  tenant filter first, then neighbours of "operator"
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

- example 1. chunks for document pc_12
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document pc_12, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "Ocean Star", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id pc_12
```

- homework
```ts
// 1a  empty search for "Ocean Star"
// 1b  chunk metadata includes pc_12
// 1c  a 20 page file is many chunks, not one vector
```

- example 2. chunks for document m_1
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document m_1, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "Ada", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id m_1
```

- homework
```ts
// 2a  empty search for "Ada"
// 2b  chunk metadata includes m_1
// 2c  a 20 page file is many chunks, not one vector
```

- example 3. chunks for document t_9
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document t_9, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "Rajshahi Open", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id t_9
```

- homework
```ts
// 3a  empty search for "Rajshahi Open"
// 3b  chunk metadata includes t_9
// 3c  a 20 page file is many chunks, not one vector
```

- example 4. chunks for document v_4
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document v_4, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "Episode 1", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id v_4
```

- homework
```ts
// 4a  empty search for "Episode 1"
// 4b  chunk metadata includes v_4
// 4c  a 20 page file is many chunks, not one vector
```

- example 5. chunks for document f_2
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document f_2, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "NOR", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id f_2
```

- homework
```ts
// 5a  empty search for "NOR"
// 5b  chunk metadata includes f_2
// 5c  a 20 page file is many chunks, not one vector
```

- example 6. chunks for document u_3
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document u_3, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "a@example.com", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id u_3
```

- homework
```ts
// 6a  empty search for "a@example.com"
// 6b  chunk metadata includes u_3
// 6c  a 20 page file is many chunks, not one vector
```

- example 7. chunks for document pay_8
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document pay_8, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "evt_1", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id pay_8
```

- homework
```ts
// 7a  empty search for "evt_1"
// 7b  chunk metadata includes pay_8
// 7c  a 20 page file is many chunks, not one vector
```

- example 8. chunks for document room_2
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document room_2, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "s_9", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id room_2
```

- homework
```ts
// 8a  empty search for "s_9"
// 8b  chunk metadata includes room_2
// 8c  a 20 page file is many chunks, not one vector
```

- example 9. chunks for document vs_7
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document vs_7, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "North Wind", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id vs_7
```

- homework
```ts
// 9a  empty search for "North Wind"
// 9b  chunk metadata includes vs_7
// 9c  a 20 page file is many chunks, not one vector
```

- example 10. chunks for document sc_3
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document sc_3, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "11", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id sc_3
```

- homework
```ts
// 10a  empty search for "11"
// 10b  chunk metadata includes sc_3
// 10c  a 20 page file is many chunks, not one vector
```

- example 11. chunks for document tm_2
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document tm_2, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "Blue", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id tm_2
```

- homework
```ts
// 11a  empty search for "Blue"
// 11b  chunk metadata includes tm_2
// 11c  a 20 page file is many chunks, not one vector
```

- example 12. chunks for document up_6
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document up_6, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "videos/u_1/a.mp4", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id up_6
```

- homework
```ts
// 12a  empty search for "videos/u_1/a.mp4"
// 12b  chunk metadata includes up_6
// 12c  a 20 page file is many chunks, not one vector
```

- example 13. chunks for document st_1
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document st_1, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "player_a", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id st_1
```

- homework
```ts
// 13a  empty search for "player_a"
// 13b  chunk metadata includes st_1
// 13c  a 20 page file is many chunks, not one vector
```

- example 14. chunks for document n_2
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document n_2, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "Chattogram", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id n_2
```

- homework
```ts
// 14a  empty search for "Chattogram"
// 14b  chunk metadata includes n_2
// 14c  a 20 page file is many chunks, not one vector
```

- example 15. chunks for document b_3
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document b_3, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "semi", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id b_3
```

- homework
```ts
// 15a  empty search for "semi"
// 15b  chunk metadata includes b_3
// 15c  a 20 page file is many chunks, not one vector
```

- example 16. chunks for document se_1
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document se_1, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "u_3", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id se_1
```

- homework
```ts
// 16a  empty search for "u_3"
// 16b  chunk metadata includes se_1
// 16c  a 20 page file is many chunks, not one vector
```

- example 17. chunks for document q_1
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document q_1, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "laytime", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id q_1
```

- homework
```ts
// 17a  empty search for "laytime"
// 17b  chunk metadata includes q_1
// 17c  a 20 page file is many chunks, not one vector
```

- example 18. chunks for document r_1
- search, then generate. empty search says we do not know
- overlap keeps a fact on the boundary in two chunks
- metadata: document r_1, heading, tenant

```ts
const chunks = await searchChunks({ tenantId: "t", question: "operator", limit: 4 });
if (chunks.length === 0) return { answer: "I do not know.", sourceId: null };
// else the prompt receives the chunks and source id r_1
```

- homework
```ts
// 18a  empty search for "operator"
// 18b  chunk metadata includes r_1
// 18c  a 20 page file is many chunks, not one vector
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

- example 1. retrieve 20, keep 4, for question about pc_12
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Ocean Star" -> 20
rerank -> 4
keep source pc_12 on each winner
```

- homework
```text
// 1a  20 then 4 for pc_12
// 1b  do not rerank the whole table
// 1c  a missed paragraph is a search or chunk problem
```

- example 2. retrieve 20, keep 4, for question about m_1
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Ada" -> 20
rerank -> 4
keep source m_1 on each winner
```

- homework
```text
// 2a  20 then 4 for m_1
// 2b  do not rerank the whole table
// 2c  a missed paragraph is a search or chunk problem
```

- example 3. retrieve 20, keep 4, for question about t_9
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Rajshahi Open" -> 20
rerank -> 4
keep source t_9 on each winner
```

- homework
```text
// 3a  20 then 4 for t_9
// 3b  do not rerank the whole table
// 3c  a missed paragraph is a search or chunk problem
```

- example 4. retrieve 20, keep 4, for question about v_4
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Episode 1" -> 20
rerank -> 4
keep source v_4 on each winner
```

- homework
```text
// 4a  20 then 4 for v_4
// 4b  do not rerank the whole table
// 4c  a missed paragraph is a search or chunk problem
```

- example 5. retrieve 20, keep 4, for question about f_2
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "NOR" -> 20
rerank -> 4
keep source f_2 on each winner
```

- homework
```text
// 5a  20 then 4 for f_2
// 5b  do not rerank the whole table
// 5c  a missed paragraph is a search or chunk problem
```

- example 6. retrieve 20, keep 4, for question about u_3
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "a@example.com" -> 20
rerank -> 4
keep source u_3 on each winner
```

- homework
```text
// 6a  20 then 4 for u_3
// 6b  do not rerank the whole table
// 6c  a missed paragraph is a search or chunk problem
```

- example 7. retrieve 20, keep 4, for question about pay_8
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "evt_1" -> 20
rerank -> 4
keep source pay_8 on each winner
```

- homework
```text
// 7a  20 then 4 for pay_8
// 7b  do not rerank the whole table
// 7c  a missed paragraph is a search or chunk problem
```

- example 8. retrieve 20, keep 4, for question about room_2
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "s_9" -> 20
rerank -> 4
keep source room_2 on each winner
```

- homework
```text
// 8a  20 then 4 for room_2
// 8b  do not rerank the whole table
// 8c  a missed paragraph is a search or chunk problem
```

- example 9. retrieve 20, keep 4, for question about vs_7
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "North Wind" -> 20
rerank -> 4
keep source vs_7 on each winner
```

- homework
```text
// 9a  20 then 4 for vs_7
// 9b  do not rerank the whole table
// 9c  a missed paragraph is a search or chunk problem
```

- example 10. retrieve 20, keep 4, for question about sc_3
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "11" -> 20
rerank -> 4
keep source sc_3 on each winner
```

- homework
```text
// 10a  20 then 4 for sc_3
// 10b  do not rerank the whole table
// 10c  a missed paragraph is a search or chunk problem
```

- example 11. retrieve 20, keep 4, for question about tm_2
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Blue" -> 20
rerank -> 4
keep source tm_2 on each winner
```

- homework
```text
// 11a  20 then 4 for tm_2
// 11b  do not rerank the whole table
// 11c  a missed paragraph is a search or chunk problem
```

- example 12. retrieve 20, keep 4, for question about up_6
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "videos/u_1/a.mp4" -> 20
rerank -> 4
keep source up_6 on each winner
```

- homework
```text
// 12a  20 then 4 for up_6
// 12b  do not rerank the whole table
// 12c  a missed paragraph is a search or chunk problem
```

- example 13. retrieve 20, keep 4, for question about st_1
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "player_a" -> 20
rerank -> 4
keep source st_1 on each winner
```

- homework
```text
// 13a  20 then 4 for st_1
// 13b  do not rerank the whole table
// 13c  a missed paragraph is a search or chunk problem
```

- example 14. retrieve 20, keep 4, for question about n_2
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Chattogram" -> 20
rerank -> 4
keep source n_2 on each winner
```

- homework
```text
// 14a  20 then 4 for n_2
// 14b  do not rerank the whole table
// 14c  a missed paragraph is a search or chunk problem
```

- example 15. retrieve 20, keep 4, for question about b_3
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "semi" -> 20
rerank -> 4
keep source b_3 on each winner
```

- homework
```text
// 15a  20 then 4 for b_3
// 15b  do not rerank the whole table
// 15c  a missed paragraph is a search or chunk problem
```

- example 16. retrieve 20, keep 4, for question about se_1
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "u_3" -> 20
rerank -> 4
keep source se_1 on each winner
```

- homework
```text
// 16a  20 then 4 for se_1
// 16b  do not rerank the whole table
// 16c  a missed paragraph is a search or chunk problem
```

- example 17. retrieve 20, keep 4, for question about q_1
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "laytime" -> 20
rerank -> 4
keep source q_1 on each winner
```

- homework
```text
// 17a  20 then 4 for q_1
// 17b  do not rerank the whole table
// 17c  a missed paragraph is a search or chunk problem
```

- example 18. retrieve 20, keep 4, for question about r_1
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "operator" -> 20
rerank -> 4
keep source r_1 on each winner
```

- homework
```text
// 18a  20 then 4 for r_1
// 18b  do not rerank the whole table
// 18c  a missed paragraph is a search or chunk problem
```

- example 19. retrieve 20, keep 4, for question about pc_12
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Ocean Star" -> 20
rerank -> 4
keep source pc_12 on each winner
```

- homework
```text
// 19a  20 then 4 for pc_12
// 19b  do not rerank the whole table
// 19c  a missed paragraph is a search or chunk problem
```

- example 20. retrieve 20, keep 4, for question about m_1
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Ada" -> 20
rerank -> 4
keep source m_1 on each winner
```

- homework
```text
// 20a  20 then 4 for m_1
// 20b  do not rerank the whole table
// 20c  a missed paragraph is a search or chunk problem
```

- example 21. retrieve 20, keep 4, for question about t_9
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Rajshahi Open" -> 20
rerank -> 4
keep source t_9 on each winner
```

- homework
```text
// 21a  20 then 4 for t_9
// 21b  do not rerank the whole table
// 21c  a missed paragraph is a search or chunk problem
```

- example 22. retrieve 20, keep 4, for question about v_4
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Episode 1" -> 20
rerank -> 4
keep source v_4 on each winner
```

- homework
```text
// 22a  20 then 4 for v_4
// 22b  do not rerank the whole table
// 22c  a missed paragraph is a search or chunk problem
```

- example 23. retrieve 20, keep 4, for question about f_2
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "NOR" -> 20
rerank -> 4
keep source f_2 on each winner
```

- homework
```text
// 23a  20 then 4 for f_2
// 23b  do not rerank the whole table
// 23c  a missed paragraph is a search or chunk problem
```

- example 24. retrieve 20, keep 4, for question about u_3
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "a@example.com" -> 20
rerank -> 4
keep source u_3 on each winner
```

- homework
```text
// 24a  20 then 4 for u_3
// 24b  do not rerank the whole table
// 24c  a missed paragraph is a search or chunk problem
```

- example 25. retrieve 20, keep 4, for question about pay_8
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "evt_1" -> 20
rerank -> 4
keep source pay_8 on each winner
```

- homework
```text
// 25a  20 then 4 for pay_8
// 25b  do not rerank the whole table
// 25c  a missed paragraph is a search or chunk problem
```

- example 26. retrieve 20, keep 4, for question about room_2
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "s_9" -> 20
rerank -> 4
keep source room_2 on each winner
```

- homework
```text
// 26a  20 then 4 for room_2
// 26b  do not rerank the whole table
// 26c  a missed paragraph is a search or chunk problem
```

- example 27. retrieve 20, keep 4, for question about vs_7
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "North Wind" -> 20
rerank -> 4
keep source vs_7 on each winner
```

- homework
```text
// 27a  20 then 4 for vs_7
// 27b  do not rerank the whole table
// 27c  a missed paragraph is a search or chunk problem
```

- example 28. retrieve 20, keep 4, for question about sc_3
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "11" -> 20
rerank -> 4
keep source sc_3 on each winner
```

- homework
```text
// 28a  20 then 4 for sc_3
// 28b  do not rerank the whole table
// 28c  a missed paragraph is a search or chunk problem
```

- example 29. retrieve 20, keep 4, for question about tm_2
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Blue" -> 20
rerank -> 4
keep source tm_2 on each winner
```

- homework
```text
// 29a  20 then 4 for tm_2
// 29b  do not rerank the whole table
// 29c  a missed paragraph is a search or chunk problem
```

- example 30. retrieve 20, keep 4, for question about up_6
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "videos/u_1/a.mp4" -> 20
rerank -> 4
keep source up_6 on each winner
```

- homework
```text
// 30a  20 then 4 for up_6
// 30b  do not rerank the whole table
// 30c  a missed paragraph is a search or chunk problem
```

- example 31. retrieve 20, keep 4, for question about st_1
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "player_a" -> 20
rerank -> 4
keep source st_1 on each winner
```

- homework
```text
// 31a  20 then 4 for st_1
// 31b  do not rerank the whole table
// 31c  a missed paragraph is a search or chunk problem
```

- example 32. retrieve 20, keep 4, for question about n_2
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "Chattogram" -> 20
rerank -> 4
keep source n_2 on each winner
```

- homework
```text
// 32a  20 then 4 for n_2
// 32b  do not rerank the whole table
// 32c  a missed paragraph is a search or chunk problem
```

- example 33. retrieve 20, keep 4, for question about b_3
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "semi" -> 20
rerank -> 4
keep source b_3 on each winner
```

- homework
```text
// 33a  20 then 4 for b_3
// 33b  do not rerank the whole table
// 33c  a missed paragraph is a search or chunk problem
```

- example 34. retrieve 20, keep 4, for question about se_1
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "u_3" -> 20
rerank -> 4
keep source se_1 on each winner
```

- homework
```text
// 34a  20 then 4 for se_1
// 34b  do not rerank the whole table
// 34c  a missed paragraph is a search or chunk problem
```

- example 35. retrieve 20, keep 4, for question about q_1
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "laytime" -> 20
rerank -> 4
keep source q_1 on each winner
```

- homework
```text
// 35a  20 then 4 for q_1
// 35b  do not rerank the whole table
// 35c  a missed paragraph is a search or chunk problem
```

- example 36. retrieve 20, keep 4, for question about r_1
- rerank cannot invent a paragraph the search missed
- only the winners enter the prompt

```text
search "operator" -> 20
rerank -> 4
keep source r_1 on each winner
```

- homework
```text
// 36a  20 then 4 for r_1
// 36b  do not rerank the whole table
// 36c  a missed paragraph is a search or chunk problem
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

- example 1. tool arguments checked before laytime
- Zod rejects a bad vesselName
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row pc_12
```

- homework
```ts
// 1a  the tool result is 7500.0 for these inputs
// 1b  Zod runs before the function
// 1c  MCP does not skip the role check for pc_12
```

- example 2. tool arguments checked before laytime
- Zod rejects a bad home
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row m_1
```

- homework
```ts
// 2a  the tool result is 7500.0 for these inputs
// 2b  Zod runs before the function
// 2c  MCP does not skip the role check for m_1
```

- example 3. tool arguments checked before laytime
- Zod rejects a bad name
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row t_9
```

- homework
```ts
// 3a  the tool result is 7500.0 for these inputs
// 3b  Zod runs before the function
// 3c  MCP does not skip the role check for t_9
```

- example 4. tool arguments checked before laytime
- Zod rejects a bad title
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row v_4
```

- homework
```ts
// 4a  the tool result is 7500.0 for these inputs
// 4b  Zod runs before the function
// 4c  MCP does not skip the role check for v_4
```

- example 5. tool arguments checked before laytime
- Zod rejects a bad kind
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 250.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 500 });
// money 250.0. source row f_2
```

- homework
```ts
// 5a  the tool result is 250.0 for these inputs
// 5b  Zod runs before the function
// 5c  MCP does not skip the role check for f_2
```

- example 6. tool arguments checked before laytime
- Zod rejects a bad email
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row u_3
```

- homework
```ts
// 6a  the tool result is 7500.0 for these inputs
// 6b  Zod runs before the function
// 6c  MCP does not skip the role check for u_3
```

- example 7. tool arguments checked before laytime
- Zod rejects a bad eventId
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 15000, usedHours: 7500, demurragePerDay: 15000 });
// money 0. source row pay_8
```

- homework
```ts
// 7a  the tool result is 0 for these inputs
// 7b  Zod runs before the function
// 7c  MCP does not skip the role check for pay_8
```

- example 8. tool arguments checked before laytime
- Zod rejects a bad sessionId
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 40, demurragePerDay: 15000 });
// money 0. source row room_2
```

- homework
```ts
// 8a  the tool result is 0 for these inputs
// 8b  Zod runs before the function
// 8c  MCP does not skip the role check for room_2
```

- example 9. tool arguments checked before laytime
- Zod rejects a bad name
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 4000.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 48, usedHours: 60, demurragePerDay: 8000 });
// money 4000.0. source row vs_7
```

- homework
```ts
// 9a  the tool result is 4000.0 for these inputs
// 9b  Zod runs before the function
// 9c  MCP does not skip the role check for vs_7
```

- example 10. tool arguments checked before laytime
- Zod rejects a bad points
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row sc_3
```

- homework
```ts
// 10a  the tool result is 7500.0 for these inputs
// 10b  Zod runs before the function
// 10c  MCP does not skip the role check for sc_3
```

- example 11. tool arguments checked before laytime
- Zod rejects a bad name
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row tm_2
```

- homework
```ts
// 11a  the tool result is 7500.0 for these inputs
// 11b  Zod runs before the function
// 11c  MCP does not skip the role check for tm_2
```

- example 12. tool arguments checked before laytime
- Zod rejects a bad key
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 200, usedHours: 84, demurragePerDay: 15000 });
// money 0. source row up_6
```

- homework
```ts
// 12a  the tool result is 0 for these inputs
// 12b  Zod runs before the function
// 12c  MCP does not skip the role check for up_6
```

- example 13. tool arguments checked before laytime
- Zod rejects a bad player
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 125000.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 1500, usedHours: 1700, demurragePerDay: 15000 });
// money 125000.0. source row st_1
```

- homework
```ts
// 13a  the tool result is 125000.0 for these inputs
// 13b  Zod runs before the function
// 13c  MCP does not skip the role check for st_1
```

- example 14. tool arguments checked before laytime
- Zod rejects a bad port
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 3000.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 24, usedHours: 30, demurragePerDay: 12000 });
// money 3000.0. source row n_2
```

- homework
```ts
// 14a  the tool result is 3000.0 for these inputs
// 14b  Zod runs before the function
// 14c  MCP does not skip the role check for n_2
```

- example 15. tool arguments checked before laytime
- Zod rejects a bad round
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row b_3
```

- homework
```ts
// 15a  the tool result is 7500.0 for these inputs
// 15b  Zod runs before the function
// 15c  MCP does not skip the role check for b_3
```

- example 16. tool arguments checked before laytime
- Zod rejects a bad userId
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 60, demurragePerDay: 15000 });
// money 0. source row se_1
```

- homework
```ts
// 16a  the tool result is 0 for these inputs
// 16b  Zod runs before the function
// 16c  MCP does not skip the role check for se_1
```

- example 17. tool arguments checked before laytime
- Zod rejects a bad name
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row q_1
```

- homework
```ts
// 17a  the tool result is 7500.0 for these inputs
// 17b  Zod runs before the function
// 17c  MCP does not skip the role check for q_1
```

- example 18. tool arguments checked before laytime
- Zod rejects a bad name
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row r_1
```

- homework
```ts
// 18a  the tool result is 7500.0 for these inputs
// 18b  Zod runs before the function
// 18c  MCP does not skip the role check for r_1
```

- example 19. tool arguments checked before laytime
- Zod rejects a bad vesselName
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row pc_12
```

- homework
```ts
// 19a  the tool result is 7500.0 for these inputs
// 19b  Zod runs before the function
// 19c  MCP does not skip the role check for pc_12
```

- example 20. tool arguments checked before laytime
- Zod rejects a bad home
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row m_1
```

- homework
```ts
// 20a  the tool result is 7500.0 for these inputs
// 20b  Zod runs before the function
// 20c  MCP does not skip the role check for m_1
```

- example 21. tool arguments checked before laytime
- Zod rejects a bad name
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row t_9
```

- homework
```ts
// 21a  the tool result is 7500.0 for these inputs
// 21b  Zod runs before the function
// 21c  MCP does not skip the role check for t_9
```

- example 22. tool arguments checked before laytime
- Zod rejects a bad title
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row v_4
```

- homework
```ts
// 22a  the tool result is 7500.0 for these inputs
// 22b  Zod runs before the function
// 22c  MCP does not skip the role check for v_4
```

- example 23. tool arguments checked before laytime
- Zod rejects a bad kind
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 250.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 500 });
// money 250.0. source row f_2
```

- homework
```ts
// 23a  the tool result is 250.0 for these inputs
// 23b  Zod runs before the function
// 23c  MCP does not skip the role check for f_2
```

- example 24. tool arguments checked before laytime
- Zod rejects a bad email
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row u_3
```

- homework
```ts
// 24a  the tool result is 7500.0 for these inputs
// 24b  Zod runs before the function
// 24c  MCP does not skip the role check for u_3
```

- example 25. tool arguments checked before laytime
- Zod rejects a bad eventId
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 15000, usedHours: 7500, demurragePerDay: 15000 });
// money 0. source row pay_8
```

- homework
```ts
// 25a  the tool result is 0 for these inputs
// 25b  Zod runs before the function
// 25c  MCP does not skip the role check for pay_8
```

- example 26. tool arguments checked before laytime
- Zod rejects a bad sessionId
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 40, demurragePerDay: 15000 });
// money 0. source row room_2
```

- homework
```ts
// 26a  the tool result is 0 for these inputs
// 26b  Zod runs before the function
// 26c  MCP does not skip the role check for room_2
```

- example 27. tool arguments checked before laytime
- Zod rejects a bad name
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 4000.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 48, usedHours: 60, demurragePerDay: 8000 });
// money 4000.0. source row vs_7
```

- homework
```ts
// 27a  the tool result is 4000.0 for these inputs
// 27b  Zod runs before the function
// 27c  MCP does not skip the role check for vs_7
```

- example 28. tool arguments checked before laytime
- Zod rejects a bad points
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row sc_3
```

- homework
```ts
// 28a  the tool result is 7500.0 for these inputs
// 28b  Zod runs before the function
// 28c  MCP does not skip the role check for sc_3
```

- example 29. tool arguments checked before laytime
- Zod rejects a bad name
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row tm_2
```

- homework
```ts
// 29a  the tool result is 7500.0 for these inputs
// 29b  Zod runs before the function
// 29c  MCP does not skip the role check for tm_2
```

- example 30. tool arguments checked before laytime
- Zod rejects a bad key
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 200, usedHours: 84, demurragePerDay: 15000 });
// money 0. source row up_6
```

- homework
```ts
// 30a  the tool result is 0 for these inputs
// 30b  Zod runs before the function
// 30c  MCP does not skip the role check for up_6
```

- example 31. tool arguments checked before laytime
- Zod rejects a bad player
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 125000.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 1500, usedHours: 1700, demurragePerDay: 15000 });
// money 125000.0. source row st_1
```

- homework
```ts
// 31a  the tool result is 125000.0 for these inputs
// 31b  Zod runs before the function
// 31c  MCP does not skip the role check for st_1
```

- example 32. tool arguments checked before laytime
- Zod rejects a bad port
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 3000.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 24, usedHours: 30, demurragePerDay: 12000 });
// money 3000.0. source row n_2
```

- homework
```ts
// 32a  the tool result is 3000.0 for these inputs
// 32b  Zod runs before the function
// 32c  MCP does not skip the role check for n_2
```

- example 33. tool arguments checked before laytime
- Zod rejects a bad round
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row b_3
```

- homework
```ts
// 33a  the tool result is 7500.0 for these inputs
// 33b  Zod runs before the function
// 33c  MCP does not skip the role check for b_3
```

- example 34. tool arguments checked before laytime
- Zod rejects a bad userId
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 60, demurragePerDay: 15000 });
// money 0. source row se_1
```

- homework
```ts
// 34a  the tool result is 0 for these inputs
// 34b  Zod runs before the function
// 34c  MCP does not skip the role check for se_1
```

- example 35. tool arguments checked before laytime
- Zod rejects a bad name
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row q_1
```

- homework
```ts
// 35a  the tool result is 7500.0 for these inputs
// 35b  Zod runs before the function
// 35c  MCP does not skip the role check for q_1
```

- example 36. tool arguments checked before laytime
- Zod rejects a bad name
- the function returns the number. the model does not
- MCP is the plug shape. the guard is still ours
- inputs that match the famous example return 7500. these inputs return 7500.0

```ts
const Args = z.object({
  allowedHours: z.number().positive(),
  usedHours: z.number().nonnegative(),
  demurragePerDay: z.number().positive(),
});
Args.parse({ allowedHours: 72, usedHours: 84, demurragePerDay: 15000 });
// money 7500.0. source row r_1
```

- homework
```ts
// 36a  the tool result is 7500.0 for these inputs
// 36b  Zod runs before the function
// 36c  MCP does not skip the role check for r_1
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

- example 1. at most 4 steps for pc_12
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling Ocean Star that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "pc_12" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 1a  what we push after the tool for pc_12
// 1b  step 5 stops
// 1c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 2. at most 4 steps for m_1
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling Ada that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "m_1" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 2a  what we push after the tool for m_1
// 2b  step 5 stops
// 2c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 3. at most 4 steps for t_9
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling Rajshahi Open that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "t_9" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 3a  what we push after the tool for t_9
// 3b  step 5 stops
// 3c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 4. at most 4 steps for v_4
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling Episode 1 that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "v_4" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 4a  what we push after the tool for v_4
// 4b  step 5 stops
// 4c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 5. at most 4 steps for f_2
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling NOR that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "f_2" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 5a  what we push after the tool for f_2
// 5b  step 5 stops
// 5c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 6. at most 4 steps for u_3
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling a@example.com that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "u_3" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 6a  what we push after the tool for u_3
// 6b  step 5 stops
// 6c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 7. at most 4 steps for pay_8
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling evt_1 that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "pay_8" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 7a  what we push after the tool for pay_8
// 7b  step 5 stops
// 7c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 8. at most 4 steps for room_2
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling s_9 that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "room_2" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 8a  what we push after the tool for room_2
// 8b  step 5 stops
// 8c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 9. at most 4 steps for vs_7
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling North Wind that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "vs_7" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 9a  what we push after the tool for vs_7
// 9b  step 5 stops
// 9c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 10. at most 4 steps for sc_3
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling 11 that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "sc_3" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 10a  what we push after the tool for sc_3
// 10b  step 5 stops
// 10c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 11. at most 4 steps for tm_2
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling Blue that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "tm_2" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 11a  what we push after the tool for tm_2
// 11b  step 5 stops
// 11c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 12. at most 4 steps for up_6
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling videos/u_1/a.mp4 that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "up_6" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 12a  what we push after the tool for up_6
// 12b  step 5 stops
// 12c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 13. at most 4 steps for st_1
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling player_a that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "st_1" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 13a  what we push after the tool for st_1
// 13b  step 5 stops
// 13c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 14. at most 4 steps for n_2
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling Chattogram that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "n_2" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 14a  what we push after the tool for n_2
// 14b  step 5 stops
// 14c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 15. at most 4 steps for b_3
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling semi that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "b_3" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 15a  what we push after the tool for b_3
// 15b  step 5 stops
// 15c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 16. at most 4 steps for se_1
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling u_3 that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "se_1" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 16a  what we push after the tool for se_1
// 16b  step 5 stops
// 16c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 17. at most 4 steps for q_1
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling laytime that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "q_1" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 17a  what we push after the tool for q_1
// 17b  step 5 stops
// 17c  reflection checks the source id, it does not ask the model if it feels correct
```

- example 18. at most 4 steps for r_1
- append the tool JSON, then continue
- step 5 throws the limit
- a plan helps when we must cite two documents. spelling operator that is already in JSON does not need a plan

```ts
for (let step = 0; step < 4; step++) {
  const turn = await model.next(messages);
  if (turn.final) return Answer.parse(turn.final);
  messages.push({ role: "tool", content: JSON.stringify({ id: "r_1" }) });
}
throw new Error("step limit");
```

- homework
```ts
// 18a  what we push after the tool for r_1
// 18b  step 5 stops
// 18c  reflection checks the source id, it does not ask the model if it feels correct
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

- example 1. memory row and one loop for tenant of pc_12
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for pc_12
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 1a  yesterday's decision about pc_12 is a row
// 1b  Nest increments the step
// 1c  four agents on day one add tokens and drop facts
```

- example 2. memory row and one loop for tenant of m_1
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for m_1
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 2a  yesterday's decision about m_1 is a row
// 2b  Nest increments the step
// 2c  four agents on day one add tokens and drop facts
```

- example 3. memory row and one loop for tenant of t_9
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for t_9
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 3a  yesterday's decision about t_9 is a row
// 3b  Nest increments the step
// 3c  four agents on day one add tokens and drop facts
```

- example 4. memory row and one loop for tenant of v_4
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for v_4
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 4a  yesterday's decision about v_4 is a row
// 4b  Nest increments the step
// 4c  four agents on day one add tokens and drop facts
```

- example 5. memory row and one loop for tenant of f_2
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for f_2
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 5a  yesterday's decision about f_2 is a row
// 5b  Nest increments the step
// 5c  four agents on day one add tokens and drop facts
```

- example 6. memory row and one loop for tenant of u_3
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for u_3
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 6a  yesterday's decision about u_3 is a row
// 6b  Nest increments the step
// 6c  four agents on day one add tokens and drop facts
```

- example 7. memory row and one loop for tenant of pay_8
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for pay_8
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 7a  yesterday's decision about pay_8 is a row
// 7b  Nest increments the step
// 7c  four agents on day one add tokens and drop facts
```

- example 8. memory row and one loop for tenant of room_2
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for room_2
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 8a  yesterday's decision about room_2 is a row
// 8b  Nest increments the step
// 8c  four agents on day one add tokens and drop facts
```

- example 9. memory row and one loop for tenant of vs_7
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for vs_7
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 9a  yesterday's decision about vs_7 is a row
// 9b  Nest increments the step
// 9c  four agents on day one add tokens and drop facts
```

- example 10. memory row and one loop for tenant of sc_3
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for sc_3
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 10a  yesterday's decision about sc_3 is a row
// 10b  Nest increments the step
// 10c  four agents on day one add tokens and drop facts
```

- example 11. memory row and one loop for tenant of tm_2
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for tm_2
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 11a  yesterday's decision about tm_2 is a row
// 11b  Nest increments the step
// 11c  four agents on day one add tokens and drop facts
```

- example 12. memory row and one loop for tenant of up_6
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for up_6
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 12a  yesterday's decision about up_6 is a row
// 12b  Nest increments the step
// 12c  four agents on day one add tokens and drop facts
```

- example 13. memory row and one loop for tenant of st_1
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for st_1
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 13a  yesterday's decision about st_1 is a row
// 13b  Nest increments the step
// 13c  four agents on day one add tokens and drop facts
```

- example 14. memory row and one loop for tenant of n_2
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for n_2
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 14a  yesterday's decision about n_2 is a row
// 14b  Nest increments the step
// 14c  four agents on day one add tokens and drop facts
```

- example 15. memory row and one loop for tenant of b_3
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for b_3
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 15a  yesterday's decision about b_3 is a row
// 15b  Nest increments the step
// 15c  four agents on day one add tokens and drop facts
```

- example 16. memory row and one loop for tenant of se_1
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for se_1
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 16a  yesterday's decision about se_1 is a row
// 16b  Nest increments the step
// 16c  four agents on day one add tokens and drop facts
```

- example 17. memory row and one loop for tenant of q_1
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for q_1
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 17a  yesterday's decision about q_1 is a row
// 17b  Nest increments the step
// 17c  four agents on day one add tokens and drop facts
```

- example 18. memory row and one loop for tenant of r_1
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for r_1
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 18a  yesterday's decision about r_1 is a row
// 18b  Nest increments the step
// 18c  four agents on day one add tokens and drop facts
```

- example 19. memory row and one loop for tenant of pc_12
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for pc_12
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 19a  yesterday's decision about pc_12 is a row
// 19b  Nest increments the step
// 19c  four agents on day one add tokens and drop facts
```

- example 20. memory row and one loop for tenant of m_1
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for m_1
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 20a  yesterday's decision about m_1 is a row
// 20b  Nest increments the step
// 20c  four agents on day one add tokens and drop facts
```

- example 21. memory row and one loop for tenant of t_9
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for t_9
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 21a  yesterday's decision about t_9 is a row
// 21b  Nest increments the step
// 21c  four agents on day one add tokens and drop facts
```

- example 22. memory row and one loop for tenant of v_4
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for v_4
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 22a  yesterday's decision about v_4 is a row
// 22b  Nest increments the step
// 22c  four agents on day one add tokens and drop facts
```

- example 23. memory row and one loop for tenant of f_2
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for f_2
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 23a  yesterday's decision about f_2 is a row
// 23b  Nest increments the step
// 23c  four agents on day one add tokens and drop facts
```

- example 24. memory row and one loop for tenant of u_3
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for u_3
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 24a  yesterday's decision about u_3 is a row
// 24b  Nest increments the step
// 24c  four agents on day one add tokens and drop facts
```

- example 25. memory row and one loop for tenant of pay_8
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for pay_8
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 25a  yesterday's decision about pay_8 is a row
// 25b  Nest increments the step
// 25c  four agents on day one add tokens and drop facts
```

- example 26. memory row and one loop for tenant of room_2
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for room_2
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 26a  yesterday's decision about room_2 is a row
// 26b  Nest increments the step
// 26c  four agents on day one add tokens and drop facts
```

- example 27. memory row and one loop for tenant of vs_7
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for vs_7
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 27a  yesterday's decision about vs_7 is a row
// 27b  Nest increments the step
// 27c  four agents on day one add tokens and drop facts
```

- example 28. memory row and one loop for tenant of sc_3
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for sc_3
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 28a  yesterday's decision about sc_3 is a row
// 28b  Nest increments the step
// 28c  four agents on day one add tokens and drop facts
```

- example 29. memory row and one loop for tenant of tm_2
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for tm_2
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 29a  yesterday's decision about tm_2 is a row
// 29b  Nest increments the step
// 29c  four agents on day one add tokens and drop facts
```

- example 30. memory row and one loop for tenant of up_6
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for up_6
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 30a  yesterday's decision about up_6 is a row
// 30b  Nest increments the step
// 30c  four agents on day one add tokens and drop facts
```

- example 31. memory row and one loop for tenant of st_1
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for st_1
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 31a  yesterday's decision about st_1 is a row
// 31b  Nest increments the step
// 31c  four agents on day one add tokens and drop facts
```

- example 32. memory row and one loop for tenant of n_2
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for n_2
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 32a  yesterday's decision about n_2 is a row
// 32b  Nest increments the step
// 32c  four agents on day one add tokens and drop facts
```

- example 33. memory row and one loop for tenant of b_3
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for b_3
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 33a  yesterday's decision about b_3 is a row
// 33b  Nest increments the step
// 33c  four agents on day one add tokens and drop facts
```

- example 34. memory row and one loop for tenant of se_1
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for se_1
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 34a  yesterday's decision about se_1 is a row
// 34b  Nest increments the step
// 34c  four agents on day one add tokens and drop facts
```

- example 35. memory row and one loop for tenant of q_1
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for q_1
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 35a  yesterday's decision about q_1 is a row
// 35b  Nest increments the step
// 35c  four agents on day one add tokens and drop facts
```

- example 36. memory row and one loop for tenant of r_1
- the window forgets. a table remembers
- the row is per tenant
- Nest holds the step count. the model does not open Prisma
- start with one loop. a second agent only for a check we can test

```text
Nest tenant + step count
tool or search for r_1
model
Zod
memory row: tenant, summary, not every raw token
```

- homework
```text
// 36a  yesterday's decision about r_1 is a row
// 36b  Nest increments the step
// 36c  four agents on day one add tokens and drop facts
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

- example 1. checks and a case for pc_12
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 7500.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "pc_12", expect: 7500.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 1a  three checks around pc_12
// 1b  expect 7500.0 only if the function says 7500.0
// 1c  a new wording does not get a new permission
```

- example 2. checks and a case for m_1
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 7500.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "m_1", expect: 7500.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 2a  three checks around m_1
// 2b  expect 7500.0 only if the function says 7500.0
// 2c  a new wording does not get a new permission
```

- example 3. checks and a case for t_9
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 7500.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "t_9", expect: 7500.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 3a  three checks around t_9
// 3b  expect 7500.0 only if the function says 7500.0
// 3c  a new wording does not get a new permission
```

- example 4. checks and a case for v_4
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 7500.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "v_4", expect: 7500.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 4a  three checks around v_4
// 4b  expect 7500.0 only if the function says 7500.0
// 4c  a new wording does not get a new permission
```

- example 5. checks and a case for f_2
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 250.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "f_2", expect: 250.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 5a  three checks around f_2
// 5b  expect 250.0 only if the function says 250.0
// 5c  a new wording does not get a new permission
```

- example 6. checks and a case for u_3
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 7500.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "u_3", expect: 7500.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 6a  three checks around u_3
// 6b  expect 7500.0 only if the function says 7500.0
// 6c  a new wording does not get a new permission
```

- example 7. checks and a case for pay_8
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "pay_8", expect: 0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 7a  three checks around pay_8
// 7b  expect 0 only if the function says 0
// 7c  a new wording does not get a new permission
```

- example 8. checks and a case for room_2
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "room_2", expect: 0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 8a  three checks around room_2
// 8b  expect 0 only if the function says 0
// 8c  a new wording does not get a new permission
```

- example 9. checks and a case for vs_7
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 4000.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "vs_7", expect: 4000.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 9a  three checks around vs_7
// 9b  expect 4000.0 only if the function says 4000.0
// 9c  a new wording does not get a new permission
```

- example 10. checks and a case for sc_3
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 7500.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "sc_3", expect: 7500.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 10a  three checks around sc_3
// 10b  expect 7500.0 only if the function says 7500.0
// 10c  a new wording does not get a new permission
```

- example 11. checks and a case for tm_2
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 7500.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "tm_2", expect: 7500.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 11a  three checks around tm_2
// 11b  expect 7500.0 only if the function says 7500.0
// 11c  a new wording does not get a new permission
```

- example 12. checks and a case for up_6
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "up_6", expect: 0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 12a  three checks around up_6
// 12b  expect 0 only if the function says 0
// 12c  a new wording does not get a new permission
```

- example 13. checks and a case for st_1
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 125000.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "st_1", expect: 125000.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 13a  three checks around st_1
// 13b  expect 125000.0 only if the function says 125000.0
// 13c  a new wording does not get a new permission
```

- example 14. checks and a case for n_2
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 3000.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "n_2", expect: 3000.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 14a  three checks around n_2
// 14b  expect 3000.0 only if the function says 3000.0
// 14c  a new wording does not get a new permission
```

- example 15. checks and a case for b_3
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 7500.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "b_3", expect: 7500.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 15a  three checks around b_3
// 15b  expect 7500.0 only if the function says 7500.0
// 15c  a new wording does not get a new permission
```

- example 16. checks and a case for se_1
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "se_1", expect: 0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 16a  three checks around se_1
// 16b  expect 0 only if the function says 0
// 16c  a new wording does not get a new permission
```

- example 17. checks and a case for q_1
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 7500.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "q_1", expect: 7500.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 17a  three checks around q_1
// 17b  expect 7500.0 only if the function says 7500.0
// 17c  a new wording does not get a new permission
```

- example 18. checks and a case for r_1
- before: tenant. arguments: Zod. after: the number matches the tool
- eval case expect 7500.0 or "I do not know."
- fluent text is not the score

```ts
const cases = [
  { id: "r_1", expect: 7500.0 },
  { id: "missing", expect: "I do not know." },
];
```

- homework
```ts
// 18a  three checks around r_1
// 18b  expect 7500.0 only if the function says 7500.0
// 18c  a new wording does not get a new permission
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

- example 1. trace fields for pc_12
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees pc_12. a fine-tune does not

```text
requestId
sourceIds: ["pc_12"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 1a  four trace fields for pc_12
// 1b  leave the TOTP secret out
// 1c  a change to vesselName today is RAG, not LoRA
```

- example 2. trace fields for m_1
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees m_1. a fine-tune does not

```text
requestId
sourceIds: ["m_1"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 2a  four trace fields for m_1
// 2b  leave the TOTP secret out
// 2c  a change to home today is RAG, not LoRA
```

- example 3. trace fields for t_9
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees t_9. a fine-tune does not

```text
requestId
sourceIds: ["t_9"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 3a  four trace fields for t_9
// 3b  leave the TOTP secret out
// 3c  a change to name today is RAG, not LoRA
```

- example 4. trace fields for v_4
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees v_4. a fine-tune does not

```text
requestId
sourceIds: ["v_4"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 4a  four trace fields for v_4
// 4b  leave the TOTP secret out
// 4c  a change to title today is RAG, not LoRA
```

- example 5. trace fields for f_2
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees f_2. a fine-tune does not

```text
requestId
sourceIds: ["f_2"]
toolResult: 250.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 5a  four trace fields for f_2
// 5b  leave the TOTP secret out
// 5c  a change to kind today is RAG, not LoRA
```

- example 6. trace fields for u_3
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees u_3. a fine-tune does not

```text
requestId
sourceIds: ["u_3"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 6a  four trace fields for u_3
// 6b  leave the TOTP secret out
// 6c  a change to email today is RAG, not LoRA
```

- example 7. trace fields for pay_8
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees pay_8. a fine-tune does not

```text
requestId
sourceIds: ["pay_8"]
toolResult: 0
tokensIn tokensOut
parsed true
```

- homework
```text
// 7a  four trace fields for pay_8
// 7b  leave the TOTP secret out
// 7c  a change to eventId today is RAG, not LoRA
```

- example 8. trace fields for room_2
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees room_2. a fine-tune does not

```text
requestId
sourceIds: ["room_2"]
toolResult: 0
tokensIn tokensOut
parsed true
```

- homework
```text
// 8a  four trace fields for room_2
// 8b  leave the TOTP secret out
// 8c  a change to sessionId today is RAG, not LoRA
```

- example 9. trace fields for vs_7
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees vs_7. a fine-tune does not

```text
requestId
sourceIds: ["vs_7"]
toolResult: 4000.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 9a  four trace fields for vs_7
// 9b  leave the TOTP secret out
// 9c  a change to name today is RAG, not LoRA
```

- example 10. trace fields for sc_3
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees sc_3. a fine-tune does not

```text
requestId
sourceIds: ["sc_3"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 10a  four trace fields for sc_3
// 10b  leave the TOTP secret out
// 10c  a change to points today is RAG, not LoRA
```

- example 11. trace fields for tm_2
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees tm_2. a fine-tune does not

```text
requestId
sourceIds: ["tm_2"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 11a  four trace fields for tm_2
// 11b  leave the TOTP secret out
// 11c  a change to name today is RAG, not LoRA
```

- example 12. trace fields for up_6
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees up_6. a fine-tune does not

```text
requestId
sourceIds: ["up_6"]
toolResult: 0
tokensIn tokensOut
parsed true
```

- homework
```text
// 12a  four trace fields for up_6
// 12b  leave the TOTP secret out
// 12c  a change to key today is RAG, not LoRA
```

- example 13. trace fields for st_1
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees st_1. a fine-tune does not

```text
requestId
sourceIds: ["st_1"]
toolResult: 125000.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 13a  four trace fields for st_1
// 13b  leave the TOTP secret out
// 13c  a change to player today is RAG, not LoRA
```

- example 14. trace fields for n_2
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees n_2. a fine-tune does not

```text
requestId
sourceIds: ["n_2"]
toolResult: 3000.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 14a  four trace fields for n_2
// 14b  leave the TOTP secret out
// 14c  a change to port today is RAG, not LoRA
```

- example 15. trace fields for b_3
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees b_3. a fine-tune does not

```text
requestId
sourceIds: ["b_3"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 15a  four trace fields for b_3
// 15b  leave the TOTP secret out
// 15c  a change to round today is RAG, not LoRA
```

- example 16. trace fields for se_1
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees se_1. a fine-tune does not

```text
requestId
sourceIds: ["se_1"]
toolResult: 0
tokensIn tokensOut
parsed true
```

- homework
```text
// 16a  four trace fields for se_1
// 16b  leave the TOTP secret out
// 16c  a change to userId today is RAG, not LoRA
```

- example 17. trace fields for q_1
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees q_1. a fine-tune does not

```text
requestId
sourceIds: ["q_1"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 17a  four trace fields for q_1
// 17b  leave the TOTP secret out
// 17c  a change to name today is RAG, not LoRA
```

- example 18. trace fields for r_1
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees r_1. a fine-tune does not

```text
requestId
sourceIds: ["r_1"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 18a  four trace fields for r_1
// 18b  leave the TOTP secret out
// 18c  a change to name today is RAG, not LoRA
```

- example 19. trace fields for pc_12
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees pc_12. a fine-tune does not

```text
requestId
sourceIds: ["pc_12"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 19a  four trace fields for pc_12
// 19b  leave the TOTP secret out
// 19c  a change to vesselName today is RAG, not LoRA
```

- example 20. trace fields for m_1
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees m_1. a fine-tune does not

```text
requestId
sourceIds: ["m_1"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 20a  four trace fields for m_1
// 20b  leave the TOTP secret out
// 20c  a change to home today is RAG, not LoRA
```

- example 21. trace fields for t_9
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees t_9. a fine-tune does not

```text
requestId
sourceIds: ["t_9"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 21a  four trace fields for t_9
// 21b  leave the TOTP secret out
// 21c  a change to name today is RAG, not LoRA
```

- example 22. trace fields for v_4
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees v_4. a fine-tune does not

```text
requestId
sourceIds: ["v_4"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 22a  four trace fields for v_4
// 22b  leave the TOTP secret out
// 22c  a change to title today is RAG, not LoRA
```

- example 23. trace fields for f_2
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees f_2. a fine-tune does not

```text
requestId
sourceIds: ["f_2"]
toolResult: 250.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 23a  four trace fields for f_2
// 23b  leave the TOTP secret out
// 23c  a change to kind today is RAG, not LoRA
```

- example 24. trace fields for u_3
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees u_3. a fine-tune does not

```text
requestId
sourceIds: ["u_3"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 24a  four trace fields for u_3
// 24b  leave the TOTP secret out
// 24c  a change to email today is RAG, not LoRA
```

- example 25. trace fields for pay_8
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees pay_8. a fine-tune does not

```text
requestId
sourceIds: ["pay_8"]
toolResult: 0
tokensIn tokensOut
parsed true
```

- homework
```text
// 25a  four trace fields for pay_8
// 25b  leave the TOTP secret out
// 25c  a change to eventId today is RAG, not LoRA
```

- example 26. trace fields for room_2
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees room_2. a fine-tune does not

```text
requestId
sourceIds: ["room_2"]
toolResult: 0
tokensIn tokensOut
parsed true
```

- homework
```text
// 26a  four trace fields for room_2
// 26b  leave the TOTP secret out
// 26c  a change to sessionId today is RAG, not LoRA
```

- example 27. trace fields for vs_7
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees vs_7. a fine-tune does not

```text
requestId
sourceIds: ["vs_7"]
toolResult: 4000.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 27a  four trace fields for vs_7
// 27b  leave the TOTP secret out
// 27c  a change to name today is RAG, not LoRA
```

- example 28. trace fields for sc_3
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees sc_3. a fine-tune does not

```text
requestId
sourceIds: ["sc_3"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 28a  four trace fields for sc_3
// 28b  leave the TOTP secret out
// 28c  a change to points today is RAG, not LoRA
```

- example 29. trace fields for tm_2
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees tm_2. a fine-tune does not

```text
requestId
sourceIds: ["tm_2"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 29a  four trace fields for tm_2
// 29b  leave the TOTP secret out
// 29c  a change to name today is RAG, not LoRA
```

- example 30. trace fields for up_6
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees up_6. a fine-tune does not

```text
requestId
sourceIds: ["up_6"]
toolResult: 0
tokensIn tokensOut
parsed true
```

- homework
```text
// 30a  four trace fields for up_6
// 30b  leave the TOTP secret out
// 30c  a change to key today is RAG, not LoRA
```

- example 31. trace fields for st_1
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees st_1. a fine-tune does not

```text
requestId
sourceIds: ["st_1"]
toolResult: 125000.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 31a  four trace fields for st_1
// 31b  leave the TOTP secret out
// 31c  a change to player today is RAG, not LoRA
```

- example 32. trace fields for n_2
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees n_2. a fine-tune does not

```text
requestId
sourceIds: ["n_2"]
toolResult: 3000.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 32a  four trace fields for n_2
// 32b  leave the TOTP secret out
// 32c  a change to port today is RAG, not LoRA
```

- example 33. trace fields for b_3
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees b_3. a fine-tune does not

```text
requestId
sourceIds: ["b_3"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 33a  four trace fields for b_3
// 33b  leave the TOTP secret out
// 33c  a change to round today is RAG, not LoRA
```

- example 34. trace fields for se_1
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees se_1. a fine-tune does not

```text
requestId
sourceIds: ["se_1"]
toolResult: 0
tokensIn tokensOut
parsed true
```

- homework
```text
// 34a  four trace fields for se_1
// 34b  leave the TOTP secret out
// 34c  a change to userId today is RAG, not LoRA
```

- example 35. trace fields for q_1
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees q_1. a fine-tune does not

```text
requestId
sourceIds: ["q_1"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 35a  four trace fields for q_1
// 35b  leave the TOTP secret out
// 35c  a change to name today is RAG, not LoRA
```

- example 36. trace fields for r_1
- source ids, tool name, tokens, parsed true or false
- no password and no full contract in the log
- LoRA does not learn a row created this morning
- retrieval sees r_1. a fine-tune does not

```text
requestId
sourceIds: ["r_1"]
toolResult: 7500.0
tokensIn tokensOut
parsed true
```

- homework
```text
// 36a  four trace fields for r_1
// 36b  leave the TOTP secret out
// 36c  a change to name today is RAG, not LoRA
```
