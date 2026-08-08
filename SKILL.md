---
name: revise
description: >
  Re-teach concepts from a learning log through interactive, one-concept-at-a-time
  revision. Use when the user asks to revise, review, relearn, or practise concepts
  they previously learned, including requests scoped by topic, project, date, or
  concept. Teach before questioning by default, then use thoughtful application
  questions to strengthen understanding.
---

# Revise

Restore and strengthen concepts captured in a learning log. Work through one concept at a
time. Re-teach before asking questions unless the user explicitly requests active recall.

## Find the learning log

Use a path supplied by the user.

Otherwise, inspect an installed `learning-log` skill for its configured log path. If that is
unavailable, check:

1. `~/learned-log.md`
2. `~/.codex/learned-log.md`
3. `~/.claude/learned-log.md`

If no learning log exists, ask the user for its location. Never invent entries or create an
empty log.

Parse entries shaped like:

    - [x] **{concept}** | {project} | {date} | {one-line explanation}

Treat the learning log as read-only.

## Let the user choose

Honor any concept, topic, project, date range, or count specified by the user.

If no scope is given:

1. Find the five most recent distinct concepts.
2. List each concept by name.
3. Ask which concept the user wants to revise.

Do not identify concepts only by numbers. Use their names throughout the conversation.

The initial five concepts are a starting menu, not a permanent limit. After revision begins,
continue offering other concepts from the log. Let the user request older concepts, another
project, a topic, a date range, or more choices.

Collapse exact duplicates, but keep distinct concepts separate.

## Re-teach one concept

Teach only the selected concept before moving to another.

Give an explanation substantial enough to restore the mental model, not merely a rewritten
version of the one-line log entry. Include:

1. The core idea in plain language.
2. The mechanism or causal intuition.
3. A useful example, contrast, limitation, or consequence.

Use the logged explanation as evidence of the user’s previous depth. Aim slightly beyond that
summary so the revision is worthwhile, without turning it into an unrelated expert lecture.

When the original conversation or linked notes are available, use them to recover more
context. A one-line entry cannot reproduce the exact original explanation. Never claim exact
fidelity when the original context is unavailable.

If the user asks to go deeper, add the next useful layer of mechanism, limitation, or
application instead of repeating the first explanation.

## Ask a thoughtful question

After re-teaching a concept, ask exactly one question and wait for the user’s answer.

The question must be answerable or derivable from the explanation, but it must not merely ask
the user to repeat a sentence they just read. Require at least one step of reasoning.

Prefer questions that ask the user to:

- Apply the concept to a new situation.
- Predict an outcome.
- Diagnose a failure.
- Compare two approaches.
- Explain why a mechanism produces a consequence.
- Connect the concept to a realistic example.

Do not ask the same or a highly similar question again during the session. When revisiting a
concept at greater depth, test the new layer rather than repeating the earlier question.

Keep the experience conversational and engaging. Do not add points, streaks, levels, or
artificial rewards unless the user requests them.

## Respond to the answer

Mark the answer as `correct`, `partial`, or `missed`.

Give a brief, concrete explanation of what was right and what needs correction. For a
`partial` or `missed` answer, re-teach the missing part and offer one retry.

Do not shame weak answers or soften incorrect ones.

After resolving the question, ask whether the user wants to:

- Go deeper into the current concept, using its name.
- Continue with another named concept.
- See more concepts from the learning log.

If the user wants to skip a question or change concepts, continue without treating revision
as a gate.

## Active recall

If the user explicitly asks to be tested before re-teaching, reverse the order:

1. Ask one thoughtful question about the selected concept.
2. Wait for the answer.
3. Mark it `correct`, `partial`, or `missed`.
4. Re-teach the concept, focusing on any missing understanding.
5. Offer a new question only if the user wants one.

Do not use question-first recall as the default revision flow.

## Finish the session

When the user stops, briefly name:

- Concepts revised.
- Concepts understood well.
- Concepts worth revisiting, based only on their answers.

Do not create scores, review-history files, or persistent state.

## Boundaries

- Never modify the source learning log.
- Never invent concepts absent from the log.
- Do not dump every explanation or question at once.
- Do not confuse immediate repetition with durable recall.
- Do not gate code merges, releases, or shipping.
- Do not depend on another skill.
