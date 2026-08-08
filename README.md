# revise

We learn more concepts and get more done than ever. But I rarely return to older conversations
to revise what I learned.

That breaks the repetition needed for long-term retention and intuition. It can create an
exaggerated illusion of learning: you recognize more ideas and produce more work, but much of
the understanding fades before it becomes something you can confidently use.

`revise` turns your learning log into an interactive revision session you can invoke anytime.
It does more than select a topic and show a definition. It restores the mental model, checks
whether you can reason with it, and lets you decide where to go next.

## How a session works

1. Invoke `revise` whenever you want to review.
2. Choose from your five most recent concepts, or explore older concepts by topic, project,
   or date.
3. Re-learn one concept through a substantial explanation matched to your previous depth.
4. Answer one question that requires application, prediction, comparison, or diagnosis.
5. Go deeper into that concept or choose another one by name.

The initial five concepts are only a starting menu. The session can keep moving through your
learning log for as long as it remains useful.

## Built to feel like revision, not a test

- Teaching comes before questioning unless you explicitly request active recall.
- Questions are derivable from the explanation but require an actual step of reasoning.
- Questions do not simply repeat the sentence you just read.
- Explanations become deeper when you ask, rather than repeating the same summary.
- There are no forced scores, streaks, merge gates, or hidden review files.
- The learning log remains read-only.

The fun comes from choosing your own path, solving varied questions, and seeing whether an old
idea has become usable intuition instead of a familiar phrase.

## Invoke it anytime

Try:

```text
Revise what I learned recently.
Revise concepts from my robotics project.
Show me older concepts about neural networks.
Test me on this concept before re-teaching it.
```

## Install

```bash
npx skills add AdiBira/revise
```

## Learning log format

```markdown
- [x] **{concept}** | {project} | {date} | {one-line explanation}
```

## Pairs with learning-log

Use [learning-log](https://github.com/AdiBira/learning-log) to capture concepts as you learn
them, then use `revise` to revisit and strengthen them.
