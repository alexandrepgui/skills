---
name: generate-artifact
description: Generate a rich local HTML artifact to explain complex findings, plans, or concepts. Use when the user asks for an artifact, HTML report, visual explanation, or shareable summary.
user-invocable: true
---

Generate a rich local HTML artifact that helps the user understand the current topic in the conversation. Include a TL;DR summary and, if it makes sense, possible gotchas section.

Use clear structure, modern simple UI, and useful visuals: tables, code blocks with syntax highlighting, diagrams, timelines, or comparisons. Add visuals when they clarify the content.

Avoid flashy visuals. Strive for simplicity and clarity.

Write the artifact as a standalone HTML file in a temporary folder.

When done, open it in the user's browser automatically. If that fails, provide the file path.
