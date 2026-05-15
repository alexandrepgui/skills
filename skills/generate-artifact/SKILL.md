---
name: generate-artifact
description: Generate a rich local HTML artifact to explain complex findings, plans, or concepts. Use when the user asks for an artifact, HTML report, visual explanation, or shareable summary.
---

Generate a rich local HTML artifact that helps the user understand the current topic in the conversation. Include a TL;DR summary and, only if it makes sense, a gotchas section.

## Templates

Start from one concrete template `assets/classic-docs-template.html`.

Copy the template, replace the placeholder content, and keep its visual direction. Do not invent a new base shell.

## Guardrails

- Use the template's existing sections sidebar and theme toggle.
- Use the template's existing code-block setup. Format code as `<pre><code class="language-java">escaped code</code></pre>`.
- Always HTML-escape code content: replace `&`, `<`, and `>` with entities.
- Inline code must wrap safely. Do not add `white-space: nowrap` to inline `code`.
- In step/checklist content, wrap the text in a child element: `<div class="step"><div>...</div></div>`. This keeps the number marker separate from the text and prevents inline code from collapsing into vertical text.
- Do not put two long code blocks side by side. Use side-by-side code only for short excerpts; otherwise stack the blocks or summarize one side.
- Prefer HTML flow cards for process diagrams. Avoid SVG for flows with long labels, URLs, or endpoint names.
- For smoke tests and procedures, use the template's step/checklist markup. Do not invent custom numbered rows.
- Use tables, comparison cards, callouts, timelines, and flow cards only when they clarify the content.

Avoid flashy visuals. Strive for clarity, but let the chosen template carry a distinct visual style.

Write the artifact as a single HTML file in a temporary folder.

When done, open it in the user's browser automatically. If that fails, provide the file path.
