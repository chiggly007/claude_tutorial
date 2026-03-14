# Testing Guide

This repo is tested through conversation playbooks inside Claude Code.

## Launch locally

```bash
cd /Users/chiragshah/PycharmProjects/claude_tutorial
/Users/chiragshah/Library/pnpm/claude
```

## Playbooks

### Playbook 1: Developer tutorial

| Step | You Say | Expected Behavior |
|------|---------|-------------------|
| 1 | `start tutorial` | Tutor asks Developer or Non-Developer |
| 2 | `Developer` | Starts shared lesson `S1` |
| 3 | `next lesson` | Progresses to `S2` or next incomplete lesson |
| 4 | `lesson D3` | Jumps to Planning / Plan Mode lesson |

### Playbook 2: Non-Developer tutorial

| Step | You Say | Expected Behavior |
|------|---------|-------------------|
| 1 | `/start-tutorial` | Tutor starts and asks for track |
| 2 | `Non-Developer` | Starts shared lesson `S1` |
| 3 | `next` | Continues through non-developer lessons |

### Playbook 3: Claude Code Q&A

| Step | You Say | Expected Behavior |
|------|---------|-------------------|
| 1 | `what does /compact do?` | Clear explanation of `/compact` |
| 2 | `how do I change models?` | Explains `/model` |
| 3 | `what does /doctor do?` | Explains installation health check |
| 4 | `what is MCP?` | Explains MCP accurately |
| 5 | `how do subagents work?` | Explains `.claude/agents/` and `/agents` |

### Playbook 4: Memory and instructions

| Step | You Say | Expected Behavior |
|------|---------|-------------------|
| 1 | `how do I customize Claude for this repo?` | Explains `CLAUDE.md` and `/memory` |
| 2 | `where do project commands live?` | Explains `.claude/commands/` |

### Playbook 5: Reset and track switch

| Step | You Say | Expected Behavior |
|------|---------|-------------------|
| 1 | `start tutorial` | Tutorial begins |
| 2 | `switch to non-developer` | Track changes cleanly |
| 3 | `reset tutorial` | Tutor restarts from the beginning |

## QA checklist

- tutorial starts from plain text and from `/start-tutorial`
- lessons refer to Claude Code commands, not Copilot CLI
- Plan Mode is described as a permission mode, not a `/plan` command
- memory is described through `CLAUDE.md` and `/memory`
- advanced topics use `/mcp`, `/agents`, and custom commands
- install/run instructions use Claude Code
