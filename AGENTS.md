# OpenCode Skills - Project Rules

Best practice engineering skills for open source Rust/WebAssembly development.

## Core Principles

1. **Correctness First**: Prove code works correctly before optimizing (run -> test -> benchmark)
2. **Safety First**: Leverage Rust's type system to prevent bugs at compile time
3. **Test Everything**: No code without corresponding tests
4. **Zero Warnings**: Code must compile without warnings or linting issues

## Development Workflow

Follow the disciplined V-model phases:

1. **Research** (`@disciplined-research`) - Understand before designing
2. **Design** (`@disciplined-design`) - Plan before coding
3. **Specification** (`@disciplined-specification`) - Clarify edge cases
4. **Implementation** (`@disciplined-implementation`) - Execute with tests
5. **Verification** (`@disciplined-verification`) - Unit/integration testing
6. **Validation** (`@disciplined-validation`) - UAT and sign-off

## Rust Conventions

- Use `cargo clippy` with no warnings
- Use `cargo fmt` for formatting
- Prefer `thiserror` for library errors, `anyhow` for applications
- Document all public items with rustdoc
- Add `# Examples`, `# Errors`, `# Panics` sections as needed

## Testing Requirements

- Unit tests for all public functions
- Integration tests for module interactions
- Property-based tests for complex logic (proptest)
- Regression tests BEFORE optimizations

## Commit Messages

Follow conventional commits:
- `feat:` New features
- `fix:` Bug fixes
- `docs:` Documentation
- `test:` Tests
- `refactor:` Code changes without feature/fix
- `perf:` Performance improvements
