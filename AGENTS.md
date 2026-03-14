# Agents

## Overview

This repo now targets Claude Code rather than GitHub Copilot CLI.

It ships a beginner tutorial experience for Claude Code using:

- `CLAUDE.md` for project instructions
- `.claude/agents/claude_tutorial.md` for the tutor subagent
- `.claude/commands/start-tutorial.md` for a project slash command
- `skills/claude_tutorial/SKILL.md` as the canonical lesson source

## Available Agent

### claude_tutorial

- Purpose: interactive tutorial agent for Claude Code
- Usage: launch Claude Code from the repo root, then say `start tutorial` or run `/start-tutorial`
- Runtime file: `.claude/agents/claude_tutorial.md`
- Source docs: `agents/claude_tutorial.agent.md` and `skills/claude_tutorial/SKILL.md`

## Learning Tracks

| Track | Audience | Topics |
|-------|----------|--------|
| Developer | Engineers familiar with the terminal | Commands, file refs, Plan Mode, memory, MCP, subagents |
| Non-Developer | Anyone new to the terminal | Writing, task planning, code understanding, summaries |

## Configuration

- Launch from the repo root so Claude Code auto-loads `CLAUDE.md`
- If `claude` is not on your `PATH`, use `/Users/chiragshah/Library/pnpm/claude`
- Claude Code concepts in this repo are based on Anthropic official docs for overview, slash commands, memory, MCP, and subagents
