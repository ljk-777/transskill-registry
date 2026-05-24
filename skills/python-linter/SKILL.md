---
name: python-linter
description: Python code style guide with ruff and mypy configuration
tags: [python, linter, ruff, mypy]
---

# Python Linter Configuration

Follow these rules when writing Python code:

## Code Style

- Use **ruff** for linting and formatting
- Line length: 88 characters (ruff default)
- Use type hints for all function signatures and public APIs
- Prefer pathlib over os.path for file operations

## Import Order

1. Standard library (`os`, `sys`, `pathlib`)
2. Third-party (`ruff`, `requests`, `numpy`)
3. Local application (`from myapp import ...`)

## Type Checking

- Use `mypy --strict` for type checking
- Use `dataclasses` for data containers
- Use `TypedDict` for dictionary types
- Avoid `Any` unless absolutely necessary

## Common Patterns

```python
# ✅ Prefer pathlib
from pathlib import Path
config = Path("config.toml")

# ✅ Use type hints
def greet(name: str, age: int) -> str:
    return f"{name} is {age} years old"
```

## Prohibited Patterns

- No wildcard imports (`from module import *`)
- No bare `except:` clauses
- No mutable default arguments
