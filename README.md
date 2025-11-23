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

## Alternative Git Hook Managers

While this hook works with [pre-commit](https://pre-commit.com/), you might also consider:

- **[prek](https://github.com/j178/prek)** - Fast, pure Rust implementation with better performance
- **[lefthook](https://github.com/evilmartians/lefthook)** - Fast Git hooks manager written in Go

Both support the same `.pre-commit-config.yaml` format and are drop-in replacements with improved speed.

## License

MIT

## Author

Jacob Coffee ([@JacobCoffee](https://github.com/JacobCoffee))
