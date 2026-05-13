# Skills

Personal agent skills for Claude Code, Codex, Cursor, and other tools that support Agent Skills.

## Install

```bash
npx skills@latest add alexandrepgui/skills
```

To install every skill into every detected agent:

```bash
npx skills@latest add alexandrepgui/skills --all
```

## Skills

- `/teach-me` - learn a topic through an interactive explain-back loop.
- `/generate-artifact` - generate a rich local HTML artifact for complex explanations or summaries.

## Local Development

List skills:

```bash
./scripts/list-skills.sh
```

Link skills into Claude Code locally:

```bash
./scripts/link-skills.sh
```
