# OpenCode Skills

OpenCode skills for disciplined Rust/WebAssembly development. Compatible with both [OpenCode](https://opencode.ai) and [Claude Code](https://claude.ai/code).

## Installation

### Global Installation (All Projects)

```bash
# Clone the repository
git clone https://github.com/terraphim/opencode-skills.git

# Copy skills to global config
cp -r opencode-skills/skill/* ~/.config/opencode/skill/
```

### Per-Project Installation

```bash
# Copy to project's .opencode directory
mkdir -p .opencode/skill
cp -r opencode-skills/skill/* .opencode/skill/
```

### Claude Code Compatibility

OpenCode also supports Claude-compatible paths:

```bash
# Works with .claude/skills/ path
mkdir -p .claude/skills
cp -r opencode-skills/skill/* .claude/skills/
```

## Usage

Skills are automatically discovered and available to agents. The agent sees the skill name and description, and invokes them on-demand.

## Available Skills (28)

### Disciplined Development (V-Model)

| Skill | Phase | Description |
|-------|-------|-------------|
| `disciplined-research` | 1 | Deep problem understanding before design |
| `disciplined-design` | 2 | Create implementation plans from research |
| `disciplined-specification` | 2.5 | Probe specs through user interviews |
| `disciplined-implementation` | 3 | Execute plans step by step with tests |
| `disciplined-verification` | 4 | Unit/integration testing with traceability |
| `disciplined-validation` | 5 | UAT and stakeholder sign-off |

### Core Development

| Skill | Description |
|-------|-------------|
| `architecture` | System design, ADRs, API planning (no code) |
| `implementation` | Production-ready code with tests |
| `testing` | Unit, integration, property-based tests |
| `debugging` | Systematic root cause analysis |

### Rust Expertise

| Skill | Description |
|-------|-------------|
| `rust-development` | Idiomatic Rust patterns and ecosystem |
| `rust-performance` | Profiling, benchmarking, optimization |

### Quality & Security

| Skill | Description |
|-------|-------------|
| `code-review` | Bug, security, performance feedback |
| `security-audit` | Vulnerability assessment, unsafe code review |
| `quality-gate` | Orchestrates verification/validation |
| `requirements-traceability` | REQ to test traceability matrix |
| `acceptance-testing` | UAT plans and scenarios |
| `visual-testing` | Visual regression testing |

### Documentation & DevOps

| Skill | Description |
|-------|-------------|
| `documentation` | API docs, README, guides |
| `md-book` | MD-Book documentation sites |
| `devops` | CI/CD, Docker, GitHub Actions |

### Open Source

| Skill | Description |
|-------|-------------|
| `open-source-contribution` | Quality PRs, good issues |
| `community-engagement` | Release notes, contributor engagement |

### Terraphim Integration

| Skill | Description |
|-------|-------------|
| `terraphim-hooks` | Knowledge graph text replacement |
| `session-search` | AI session history search |
| `local-knowledge` | Personal notes search |

### Desktop UI

| Skill | Description |
|-------|-------------|
| `gpui-components` | GPUI components (Zed patterns) |

### Infrastructure

| Skill | Description |
|-------|-------------|
| `1password-secrets` | 1Password CLI secret management |
| `caddy` | Caddy server configuration |

## Related

- [terraphim/claude-skills](https://github.com/terraphim/claude-skills) - Claude Code plugin version

## License

Apache-2.0
