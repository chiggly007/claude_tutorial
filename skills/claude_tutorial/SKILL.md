---
name: claude_tutorial
description: >
  Use this tutorial when someone wants to learn Claude Code from scratch.
  It teaches Claude Code interactively through Developer and Non-Developer
  tracks, with guided lessons and direct Q&A.
---

# claude_tutorial

This file is the curriculum source of truth for the tutorial.

## Modes

### Tutorial mode

Triggered by:

- `start tutorial`
- `teach me`
- `next lesson`
- `lesson S1`
- `lesson D3`

### Q&A mode

Triggered by direct questions such as:

- `what does /permissions do?`
- `how do I use Plan Mode?`
- `what is CLAUDE.md?`
- `how do subagents work?`

### Reset mode

Triggered by:

- `reset tutorial`
- `start over`
- `restart`

## Audience detection

On the first tutorial interaction, ask:

- Developer
- Non-Developer

## Lesson map

### Shared lessons

| ID | Title |
|----|-------|
| `S1` | Welcome and verify setup |
| `S2` | Your first prompt |
| `S3` | Permissions and safety |

### Developer track

| ID | Title |
|----|-------|
| `D1` | Slash commands and modes |
| `D2` | File references with `@` |
| `D3` | Planning with Plan Mode |
| `D4` | Memory and project instructions |
| `D5` | Advanced: MCP, subagents, custom commands |

### Non-Developer track

| ID | Title |
|----|-------|
| `N1` | Writing and editing |
| `N2` | Task planning |
| `N3` | Understanding code without writing it |
| `N4` | Summaries and extraction |

## Lesson content

### `S1` Welcome and verify setup

Goal:

- confirm Claude Code is running
- orient the user to the terminal session

Teach:

- they are already inside Claude Code if they are reading the tutorial
- `/help` shows commands
- `/doctor` checks installation health
- `/login` can be used if authentication needs to be refreshed
- `ctrl+c` cancels, `ctrl+d` exits, `ctrl+l` clears the terminal

Exercise:

- run `/help`
- if anything looks wrong, run `/doctor`

### `S2` Your first prompt

Goal:

- show that plain English works

Teach:

- Claude Code can inspect the repo, explain files, edit files, and run commands
- user stays in control through permissions

Starter prompts:

- `what files are in this directory?`
- `summarize this project`
- `explain what this repo is doing`

### `S3` Permissions and safety

Goal:

- explain permission modes and approvals

Teach:

- Claude Code asks for approval before sensitive actions, depending on mode
- `/permissions` shows or updates permission settings
- Plan Mode is read-only analysis mode
- `Shift+Tab` can cycle modes in interactive use

### `D1` Slash commands and modes

Goal:

- introduce Claude Code’s built-in commands

Teach:

- `/help`
- `/clear`
- `/compact`
- `/doctor`
- `/model`
- `/review`
- `/permissions`

### `D2` File references with `@`

Goal:

- show how to focus Claude on specific files

Teach:

- use `@README.md`
- use `@./path/to/file`
- compare two files by referencing both in one prompt

### `D3` Planning with Plan Mode

Goal:

- teach safe analysis before edits

Teach:

- Plan Mode is a permission mode, not a slash command
- it is useful for repo exploration, implementation plans, and reviews
- users can switch modes during a session

Example prompt:

- `Review this repo in Plan Mode and tell me how the tutorial is wired together`

### `D4` Memory and project instructions

Goal:

- explain how Claude Code remembers project guidance

Teach:

- `CLAUDE.md` stores project instructions
- `/memory` helps edit memory files
- project settings can live in `.claude/`

### `D5` Advanced: MCP, subagents, custom commands

Goal:

- show how Claude Code can be extended

Teach:

- `/mcp` manages MCP connections
- `/agents` manages subagents
- project subagents live in `.claude/agents/`
- project slash commands live in `.claude/commands/`

### `N1` Writing and editing

Goal:

- use Claude Code as a writing assistant

Example prompts:

- `draft a release note from this changelog`
- `rewrite this paragraph to be shorter`
- `proofread @README.md`

### `N2` Task planning

Goal:

- break large tasks into smaller steps

Teach:

- ask Claude to create a plan before it edits anything
- Plan Mode is useful for safe planning and review

Example prompt:

- `Make a plan for improving the onboarding docs in this repo`

### `N3` Understanding code without writing it

Goal:

- help non-developers read technical projects

Example prompts:

- `explain @CLAUDE.md in plain English`
- `walk me through how this tutorial works`

### `N4` Summaries and extraction

Goal:

- summarize docs and pull out key details

Example prompts:

- `summarize the important setup steps from @README.md`
- `extract the main commands a beginner should know`

## Q&A rules

For factual questions, ground answers in Anthropic official docs whenever needed.

Prefer these topics:

- overview
- slash commands
- memory
- MCP
- subagents
- settings

## Guardrails

- do not teach GitHub Copilot CLI commands as if they are Claude Code features
- do not describe Plan Mode as `/plan`
- do not describe `copilot-instructions.md`; use `CLAUDE.md`
- if the local binary is needed, use `/Users/chiragshah/Library/pnpm/claude`
