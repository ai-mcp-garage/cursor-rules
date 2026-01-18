# Python Code Style

## Type Hints

Always annotate function signatures:

```python
def fetch_user(user_id: str) -> dict:
    ...

async def get_data(url: str) -> dict | None:
    ...
```

## Naming

| Thing | Style | Example |
|-------|-------|---------|
| Functions | `snake_case`, verb | `fetch_user()` |
| Variables | `snake_case`, noun | `user_email` |
| Constants | `UPPER_SNAKE` | `MAX_RETRIES` |
| Classes | `PascalCase` | `UserManager` |

## Structure

- Small functions that do one thing
- Early returns over nested conditionals
- 10-20 lines target; 50+ is a smell

```python
# Good
def process(data: dict) -> dict | None:
    if not data:
        return None
    if not data.get("valid"):
        return None
    return transform(data)
```

## Imports

Standard order:

```python
# Standard library
import os
from pathlib import Path

# Third party
import requests

# Local
from .utils import helper
```

## Docstrings

Brief, what not how:

```python
def calculate_average(numbers: list[float]) -> float:
    """Calculate the arithmetic mean of a list of numbers."""
    return sum(numbers) / len(numbers)
```
