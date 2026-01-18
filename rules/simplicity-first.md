# Simplicity First

Build only what's needed.

## Testing

- No test frameworks unless requested
- Verify by running and checking output
- Use `assert` or `if __name__ == "__main__"` blocks

## Dependencies

- Prefer standard library
- Every dependency is a liability — justify it

## Error Handling

- Don't add try/except "just in case"
- Let errors bubble up during development
- Handle only at boundaries where needed

## Logging

- Use `print()` for debugging, remove when done
- Add logging frameworks only for production

## CLI Arguments

- Use `os.getenv("VAR", "default")` over argparse
- Hardcode values that won't change

## Project Structure

- Keep it flat
- One file is often enough
- Add folders only when you have real organization needs
