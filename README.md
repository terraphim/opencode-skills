# OpenCode Skills

OpenCode agents for disciplined Rust/WebAssembly development. A port of [terraphim-claude-skills](https://github.com/terraphim/claude-skills) for [OpenCode](https://opencode.ai).

## Installation

### Global Installation (All Projects)

```bash
# Clone the repository
git clone https://github.com/terraphim/opencode-skills.git

# Copy agents to global config
cp -r opencode-skills/agent/* ~/.config/opencode/agent/
```

### Per-Project Installation

```bash
# Clone into your project
git clone https://github.com/terraphim/opencode-skills.git

# Copy to project's .opencode directory
mkdir -p .opencode/agent
cp -r opencode-skills/agent/* .opencode/agent/
```

## Usage

Invoke agents using the `@` syntax:

```
@disciplined-research Help me understand this codebase
@code-review Review this pull request
@rust-performance Optimize this hot path
```

Switch between primary agents with `Tab`.

## Available Agents (27)

### Disciplined Development (V-Model)

| Agent | Phase | Description |
|-------|-------|-------------|
| `disciplined-research` | 1 | Deep problem understanding before design |
| `disciplined-design` | 2 | Create implementation plans from research |
| `disciplined-specification` | 2.5 | Probe specs through user interviews |
| `disciplined-implementation` | 3 | Execute plans step by step with tests |
| `disciplined-verification` | 4 | Unit/integration testing with traceability |
| `disciplined-validation` | 5 | UAT and stakeholder sign-off |

### Core Development

| Agent | Description |
|-------|-------------|
| `architecture` | System design, ADRs, API planning (no code) |
| `implementation` | Production-ready code with tests |
| `testing` | Unit, integration, property-based tests |
| `debugging` | Systematic root cause analysis |

### Rust Expertise

| Agent | Description |
|-------|-------------|
| `rust-development` | Idiomatic Rust patterns and ecosystem |
| `rust-performance` | Profiling, benchmarking, optimization |

### Quality & Security

| Agent | Description |
|-------|-------------|
| `code-review` | Bug, security, performance feedback |
| `security-audit` | Vulnerability assessment, unsafe code review |
| `quality-gate` | Orchestrates verification/validation |
| `requirements-traceability` | REQ to test traceability matrix |
| `acceptance-testing` | UAT plans and scenarios |
| `visual-testing` | Visual regression testing |

### Documentation & DevOps

| Agent | Description |
|-------|-------------|
| `documentation` | API docs, README, guides |
| `md-book` | MD-Book documentation sites |
| `devops` | CI/CD, Docker, GitHub Actions |

### Open Source

| Agent | Description |
|-------|-------------|
| `open-source-contribution` | Quality PRs, good issues |
| `community-engagement` | Release notes, contributor engagement |

### Terraphim Integration

| Agent | Description |
|-------|-------------|
| `terraphim-hooks` | Knowledge graph text replacement |
| `session-search` | AI session history search |
| `local-knowledge` | Personal notes search |

### Desktop UI

| Agent | Description |
|-------|-------------|
| `gpui-components` | GPUI components (Zed patterns) |

## License

Apache-2.0
