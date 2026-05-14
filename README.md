# Skills

Personal agent skills for Claude Code, Codex, Cursor, and other tools that support Agent Skills.

## Install

```bash
npx skills@latest add alexandrepgui/skills
```

You may choose individual skills during install, but `/teach-me --artifact` works best when `/generate-artifact` is installed alongside it. Feel free to remove the flag locally to save context if it doesn't work for you.

To install every skill into every detected agent:

```bash
npx skills@latest add alexandrepgui/skills --all
```

## Skills

- `/teach-me` - learn a topic through an interactive explain-back loop. Use `--artifact` for an optional first-explanation HTML artifact.
- `/generate-artifact` - generate a rich local HTML artifact for complex explanations or summaries. Uses the Classic Docs template by default; pass `--workbook` for a wider visual workbook style.

## Local Development

List skills:

```bash
./scripts/list-skills.sh
```

Link skills into Claude Code locally:

```bash
./scripts/link-skills.sh
```
