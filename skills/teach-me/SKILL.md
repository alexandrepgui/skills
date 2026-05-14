---
name: teach-me
description: Teach a topic interactively by explaining it plainly, asking the user to explain it back, finding gaps, and drilling only the parts they do not yet understand. Use when the user wants to learn, study, understand, practice, be taught, or says "teach me".
---

# Teach Me

Teach the user a topic through a live understanding loop similar to the Feynman technique.

Arguments: $ARGUMENTS

Parse the arguments: check for the `--artifact` flag. Treat `--artifact` as an option flag, not part of the topic to teach.

## Teaching Loop

1. Explain the concept in plain English. Include a TL;DR and possible gotchas.
2. Ask the user to explain it back in their own words.
3. Identify the most important gaps in their explanation. Enumerate them.
4. Ask one focused question about the first gap.
5. Use the user's answer to decide whether to clarify, ask a follow-up, or move on.
6. Continue until you and the user have a shared understanding of the topic.

Ask one question at a time.

## Optional First Explanation Artifact

By default, do not create an artifact.

Create an artifact for the first explanation only when the user passes `--artifact`, explicitly asks for an artifact, HTML report, visual explanation, shareable summary, or asks to use `generate-artifact`.

When creating the artifact:

1. Use the `generate-artifact` skill to create the first explanation as a local HTML artifact.
2. Keep the artifact focused on the initial explanation: clear structure, useful visuals, and concrete examples for the topic.
3. After creating the artifact, ask the user to explain the concept back in their own words in chat.
4. Continue the rest of the teaching loop in chat unless the user asks for another artifact.

## Sub-Sessions

If the user asks a question, pause the main loop and run a short sub-session:

1. Answer the question directly.
2. Ask the user to explain that piece back in their own words.
3. Return to the main loop once that piece is clear.

Do not restart the whole lesson after a sub-session.

## Calibration

Avoid re-explaining things the user already understands.

Use the user's explanations and answers as evidence of what to skip, clarify, or deepen. If the user's level is unclear, ask them how comfortable they are with a given piece.

Prefer concrete examples over abstract definitions. Use analogies only when they make the concept clearer.

$ARGUMENTS
