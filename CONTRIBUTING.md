# Contributing to claude_tutorial

Contributions should keep the repo aligned with Claude Code, not Copilot CLI.

## Local setup

```bash
git clone https://github.com/chiggly007/claude_tutorial.git
cd claude_tutorial
/Users/chiragshah/Library/pnpm/claude
```

Claude Code should auto-load `CLAUDE.md` because you launched it from the repo root.

## What to test

- `start tutorial`
- `/start-tutorial`
- `what does /permissions do?`
- `how do I use Plan Mode?`
- `how do subagents work?`

Use the playbooks in `TESTING.md`.

## Contribution rules

- keep lesson content in `skills/claude_tutorial/SKILL.md` as the curriculum source of truth
- keep `.claude/agents/claude_tutorial.md` and `CLAUDE.md` aligned with that curriculum
- prefer Anthropic official docs when changing factual Claude Code behavior
- avoid reintroducing Copilot-specific commands or install instructions
