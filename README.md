# revise

An interactive skill that re-teaches concepts from your learning log, then asks thoughtful
questions that require application and reasoning.

## What it does

- Starts with your five most recently learned concepts.
- Lets you choose concepts by name and explore older entries.
- Re-teaches one concept at a time.
- Provides substantial explanations at your previous depth.
- Asks one application or reasoning question after each explanation.
- Lets you go deeper or continue to another concept.
- Never modifies your learning log or creates hidden review state.

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
