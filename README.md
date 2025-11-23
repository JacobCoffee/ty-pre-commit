# ty-pre-commit

Official pre-commit hook for [ty](https://github.com/astral-sh/ty) type checker.

## Usage

Add this to your `.pre-commit-config.yaml`:

```yaml
repos:
  - repo: https://github.com/JacobCoffee/ty-pre-commit
    rev: v0.0.1
    hooks:
      - id: ty
```

## Configuration

The hook respects your project's `pyproject.toml` configuration:

```toml
[tool.ty]

[tool.ty.environment]
extra-paths = ["src/"]

[tool.ty.src]
exclude = ["tests/**/*.py"]
```

## Custom Arguments

Pass additional arguments:

```yaml
- id: ty
  args: ["check", "--strict"]
```

## Requirements

- Python 3.8+
- ty type checker (installed automatically as dependency)

## License

MIT

## Author

Jacob Coffee ([@JacobCoffee](https://github.com/JacobCoffee))
