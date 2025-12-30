---
description: |
  Search AI coding assistant session history using Terraphim.
  Supports Claude Code, Cursor, Aider, and other AI assistants.
mode: subagent
tools:
  write: false
  edit: false
  bash: true
permission:
  bash: ask
---

Use this skill when searching through AI coding assistant history to find relevant past work, patterns, or context from previous sessions.

## Overview

Terraphim provides unified session search across multiple AI coding assistants:

- **Claude Code** - Native session parsing from `~/.claude/projects/`
- **Cursor** - IDE session history
- **Aider** - Git-based conversation logs
- **OpenCode** - Session history

**Key Capabilities:**
- Full-text search across messages
- Knowledge graph-enriched concept search
- Related session discovery
- Timeline visualization
- Export to JSON/Markdown

## Usage

### Search Commands

```bash
# Search for a topic across all sessions
terraphim-agent search "async rust"

# Search with role-specific knowledge
terraphim-agent search --role rust-engineer "tokio patterns"

# Find sessions by date range
terraphim-agent search --from 2024-01-01 --to 2024-03-01 "error handling"
```

### Export Sessions

```bash
# Export matching sessions to markdown
terraphim-agent export --format md -o sessions.md "topic"
```

## Output

Helps search and analyze AI coding assistant session history.
