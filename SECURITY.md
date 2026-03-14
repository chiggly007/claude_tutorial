# Security Policy

## Supported versions

| Version | Supported |
|---------|-----------|
| 1.1.x   | Yes |
| 1.0.x   | Yes |

## Reporting a vulnerability

1. Do not open a public issue for a security vulnerability.
2. Email `security@dubsopenhub.com`.
3. Or use GitHub private vulnerability reporting for this repository.

## Security considerations for this repo

This repository is mostly prompt and documentation content for Claude Code.

Primary risks:

- secrets accidentally committed into `CLAUDE.md`, `.claude/`, or lesson files
- instructions that encourage unsafe permission settings
- stale docs that misrepresent Claude Code security behavior

Guidelines:

- never commit API keys, tokens, or credentials
- do not instruct users to bypass permissions casually
- prefer Anthropic official docs when documenting `/permissions`, Plan Mode, MCP, and authentication behavior
