---
description: |
  Search personal notes and documentation through Terraphim's role-based
  search. Organized by domain (Rust, frontend, architecture).
mode: subagent
tools:
  write: false
  edit: false
  bash: true
permission:
  bash: ask
---

Use this skill when you need to search the developer's personal notes, documentation, or local knowledge base for context-specific information.

## Overview

Terraphim enables AI coding agents to search local knowledge through role-based haystacks. Different roles have access to different knowledge domains:

| Role | Knowledge Domain | Haystacks |
|------|------------------|-----------|
| Terraphim Engineer | Architecture, system design | Local docs + Knowledge Graph |
| Rust Engineer | Rust patterns, async, WASM | Local notes + Query.rs API |
| Frontend Engineer | JavaScript, TypeScript, React | GrepApp (GitHub code search) |

## When to Use This Agent

Search local knowledge when the user:
- Asks about topics in their personal notes ("in my notes", "my documentation")
- Needs domain-specific patterns they've documented before
- Asks "how do I usually do X" or "what's our pattern for Y"
- References previous solutions or bookmarked resources

**Trigger Phrases:**
- "check my notes about..."
- "search my documentation for..."
- "what do I have on..."
- "find my notes on..."
- Any domain-specific question (Rust async, frontend patterns, etc.)

## Usage

```bash
# Search with specific role
terraphim-agent search --role rust-engineer "async patterns"

# Search local documentation
terraphim-agent search --haystack local-docs "error handling"
```

## Output

Helps search local knowledge bases and personal documentation.
