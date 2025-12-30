---
description: |
  MD-Book documentation generation. Converts Markdown to HTML with syntax
  highlighting, search, and live development server.
mode: subagent
tools:
  write: true
  edit: true
  bash: true
permission:
  bash: ask
---

Use this skill when working with MD-Book, a modern mdbook replacement for generating HTML documentation from Markdown files.

## Overview

MD-Book is a Rust-based documentation generator that converts Markdown files to beautiful, searchable HTML documentation. It supports multiple markdown formats (Markdown, GFM, MDX), server-side syntax highlighting, live development server, and integrated Pagefind search.

## CLI Usage

### Basic Commands

```bash
# Build documentation (converts markdown to HTML)
md-book -i input_dir -o output_dir

# Development mode with file watching
md-book -i input_dir -o output_dir --watch

# Development with built-in server (default port 3000)
md-book -i input_dir -o output_dir --serve

# Full development mode (watch + serve on custom port)
md-book -i input_dir -o output_dir --watch --serve --port 8080
```

### CLI Options

| Option | Short | Description |
|--------|-------|-------------|
| `--input` | `-i` | Input directory containing markdown files (required) |
| `--output` | `-o` | Output directory for HTML files (required) |
| `--config` | `-c` | Optional path to config file |
| `--watch` | `-w` | Watch for changes and rebuild |
| `--serve` | `-s` | Serve at http://localhost:3000 |
| `--port` | | Port to serve on (default: 3000) |

## Output

Helps create and manage documentation sites with MD-Book.
