# Cursor Rules

Opinionated development rules for Cursor AI. Drop into `.cursor/rules/` and go.

## Rules

| Rule | Type | Description |
|------|------|-------------|
| `python-style.mdc` | File-scoped | Type hints, naming, structure, imports, docstrings |
| `python-uv.mdc` | File-scoped | Use `uv` for Python project setup and deps |
| `human-verifiable.mdc` | Agent-decided | Write code that can be read, run, and verified |
| `simplicity-first.mdc` | Agent-decided | Build only what's needed |

## Installation

```bash
# Copy to your project
cp -r rules/*.mdc /path/to/project/.cursor/rules/

# Or copy entire folder
cp -r rules/ ~/.cursor/rules/
```

## Rule Types

These rules use `.mdc` format with frontmatter:

- **File-scoped** (`globs`): Applied when editing matching files
- **Agent-decided** (`description`): Applied when Cursor decides it's relevant
- **Always apply** (`alwaysApply: true`): Every chat session

## Philosophy

These rules favor:
- **Clarity over cleverness** — code should be obvious
- **Small steps** — verify as you go
- **Minimal dependencies** — justify everything you add
- **Flat structure** — one file is often enough

## Customization

Edit frontmatter to change behavior:

```yaml
---
description: Your description for agent-decided rules
globs: ["**/*.py"]  # File patterns for scoped rules
alwaysApply: true   # Force always-on
---
```

## License

MIT
