# mirror-sql-formatter
Mirror of sql-formatter for pre-commit.

For pre-commit: see https://github.com/pre-commit/pre-commit

For sql-formatter: see https://github.com/zeroturnaround/sql-formatter

### Using sql-formatter with pre-commit

Add this to your `.pre-commit-config.yaml`:

```yaml
    -   repo: https://github.com/ammarshadiq/mirror-sql-formatter
        rev: ''  # Use the sha / tag you want to point at
        hooks:
        -   id: sql-formatter-dsi
```

### overriding `args`

note that implementation sets `args: [-w]` by default, if you are configuring sql-formatter-dsi
using `args` you'll want to include either `-w` (`--overwrite`), or
`-i` (`--file`) to only see the file affected.

