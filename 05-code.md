# 05 Code - Checklist

- Design link: {{03-design file}}.
- Plan link: {{04-plan file}}.

## 1. Before editing

- Read the implementation you touch before using it.
- Grep callers of every function you change.

## 2. Rules

- No secrets in source.
- No weakened validation to make a test pass.
- No edits to generated files.
- Explain why in comments, not what.

## 3. Verification

- Command: {{e.g. bun test path/to/file}}.
- Result: {{pass output}}.
- Regression test added: {{yes/no, id}}.
