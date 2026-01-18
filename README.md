# Cursor Rules

Opinionated development rules for Cursor AI. Drop into `.cursor/rules/` and go.

## Rules

| Rule | Purpose |
|------|---------|
| `human-verifiable.md` | Write code that can be read, run, and verified in small steps |
| `python-style.md` | Type hints, naming, structure, imports, docstrings |
| `python-uv.md` | Use `uv` for all Python project setup and deps |
| `simplicity-first.md` | Build only what's needed — no premature abstraction |

## Installation

```bash
# Copy to your project
cp -r rules/ /path/to/project/.cursor/rules/

# Or symlink for global use
ln -s /path/to/cursor-rules/rules ~/.cursor/rules
```

## Philosophy

These rules favor:
- **Clarity over cleverness** — code should be obvious
- **Small steps** — verify as you go
- **Minimal dependencies** — justify everything you add
- **Flat structure** — one file is often enough

## License

MIT
