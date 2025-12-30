---
description: |
  Knowledge graph-based text replacement using Terraphim hooks.
  Works with PreToolUse hooks and Git prepare-commit-msg hooks.
mode: subagent
tools:
  write: true
  edit: true
  bash: true
permission:
  bash: ask
---

Use this skill when setting up or using Terraphim's knowledge graph-based text replacement capabilities through hooks.

## Overview

Terraphim hooks intercept text at key points (CLI commands, commit messages) and apply transformations using Aho-Corasick automata built from knowledge graph definitions.

**Key Components:**
- `terraphim-agent replace` - CLI command for text replacement
- PreToolUse hooks - Intercept Claude Code tool calls before execution
- Git hooks - Transform commit messages using prepare-commit-msg

## Architecture

```
Knowledge Graph (docs/src/kg/)
  - bun.md (synonyms: npm, yarn, pnpm, npx)
  - terraphim_ai.md (synonyms: Claude Code, Claude Opus...)
         |
         v
   Aho-Corasick Automata (LeftmostLongest matching)
         |
         v
   Text Replacement (canonical terms)
```

## Usage

### CLI Text Replacement

```bash
# Replace text using default profile
echo "npm install" | terraphim-agent replace

# Replace with specific role
terraphim-agent replace --role "rust-engineer" < input.txt
```

### Git Hook Setup

```bash
# Install prepare-commit-msg hook
terraphim-agent install-hook --git
```

## Output

Helps configure and use knowledge graph-based text replacement hooks.
