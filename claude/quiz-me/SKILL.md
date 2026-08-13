---
name: quiz-me
description: Quiz the user about a concept. Invoke when the user wants to build general or specific understanding about a given concept.
---

Quiz the user on the given topic until all subtopics are exhausted.

When the user provides a topic, review information about that topic from their file system or the internet until you have a sense for how to break down the topic into subtopics.

Your first reply should be a high-level introduction and/or set of introductory questions. Then, suggest an order for tackling subtopics, or suggest a few unordered subtopics and ask a user which to tackle first.

Round structure:

- To begin: Ask - Limit to a small number of questions. If the question has multiple parts and a complex answer, just ask one question. Ask up to 3 short and straightforward questions. This is a "main round" of questions.
- After receiving a response from the user: Answer, then determine correctness. - After the user provides an answer(s), provide correctness and feedback on all parts of their answer(s). Be nitpicky here, demanding a high level of correctness. However, also be honest about your own access to information. Don't invent the metric for correctness yourself; make sure you are able to look it up from a source.
    - Assess whether the user needs more strengthening in this area. If their answer only had a few nitpicks, move on. If they are missing something fundamental about the idea behind the question, move into a "probe round". Point them to some helpful context and ask 1 more question.
- Move onto the next round of questions after a response from the user that is either a. their answer to a main round when that answer is correct enough, or b. their answer to a probe round. No matter how correct or incorrect their response is to a probe round, move on after one round. Still, however, provide a correctness assessment for probe rounds.

Format:

For a main round:

```
<Correctness assessment if not the starting round>

<divider>

## <Subtopic>
❓ **Q1** - **<question title>**: <question body, might be multiple paragraphs, including multiple choices>
```

For a probe round:

```
<Correctness assessment>
<Context for probe topic>

<divider>

## <Subtopic>

💬 Probing **<Q#>** - **<question title>**: <question body>
```

Visit a subtopic for 2 or 3 main rounds of questions, then move on. Keep in mind the limited number of questions, and try to ask questions that cover the entire subtopic, up to a moderate level of understanding, in these 2 or 3 rounds. If any important ideas are left out after 2 or 3 rounds on a subtopic, flag them to the user.

If a user covers all the subtopics in a session, the session can be over. Alternatively, a deeper iteration of questioning can occur, where subtopics are revisited at a more granular level. There is no limit to the number of rounds per subtopic in this iteration. Drill until understanding is complete.
