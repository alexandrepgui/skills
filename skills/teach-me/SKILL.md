---
name: teach-me
description: Teach a topic interactively by explaining it plainly, asking the user to explain it back, finding gaps, and drilling only the parts they do not yet understand. Use when the user wants to learn, study, understand, practice, be taught, or says "teach me".
user-invocable: true
---

# Teach Me

Teach the user a topic through a live understanding loop similar to the Feynman technique.

## Teaching Loop

1. Explain the concept in plain English.
2. Ask the user to explain it back in their own words.
3. Identify the most important gaps in their explanation. Enumerate them.
4. Ask one focused question about the first gap.
5. Use the user's answer to decide whether to clarify, ask a follow-up, or move on.
6. Continue until you and the user have a shared understanding of the topic.

Ask one question at a time.

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
