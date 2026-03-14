# claude_tutorial PRD

## Goal

Teach absolute beginners how to use Claude Code through an interactive tutorial that runs inside Claude Code itself.

## Product shape

This repo is a prompt product, not a software product.

Core runtime pieces:

- `CLAUDE.md`
- `.claude/agents/claude_tutorial.md`
- `.claude/commands/start-tutorial.md`

Reference/source pieces:

- `skills/claude_tutorial/SKILL.md`
- `agents/claude_tutorial.agent.md`

## User journeys

1. User launches Claude Code from the repo root.
2. Claude Code loads `CLAUDE.md`.
3. User says `start tutorial` or runs `/start-tutorial`.
4. Tutor asks whether they are a Developer or Non-Developer.
5. Tutor walks them through shared lessons, then track-specific lessons.
6. User can also ask direct Q&A questions at any time.

## Main lessons

Shared:

- Welcome and verify setup
- First prompt
- Permission model

Developer:

- Slash commands and modes
- `@` file references
- Plan Mode
- `CLAUDE.md` and memory
- MCP, subagents, project commands

Non-Developer:

- Writing and editing
- Task planning
- Understanding code
- Summaries and extraction

## Official functionality this design relies on

- Claude Code overview
- slash commands
- memory via `CLAUDE.md` and `/memory`
- MCP
- subagents in `.claude/agents/`
- project commands in `.claude/commands/`

## Success criteria

- beginner can launch Claude Code with `/Users/chiragshah/Library/pnpm/claude`
- beginner can start the tutorial without reading external docs
- lessons teach real Claude Code features rather than Copilot-specific ones
- tutorial stays useful for both developers and non-developers
