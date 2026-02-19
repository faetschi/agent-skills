# Conventional Commits Quick Reference (v1.0.0)

Source: <https://www.conventionalcommits.org/en/v1.0.0/>

Use this structure:

```text
<type>[optional scope][optional !]: <description>

[optional body]

[optional footer(s)]
```

## Required Rules

1. Start with a `type`, followed by optional `(scope)`, optional `!`, then `:` and a short description.
2. Use `feat` for new features.
3. Use `fix` for bug fixes.
4. Put detailed context in an optional body, separated from the header by one blank line.
5. Put optional footer(s) after one blank line.
6. Footer format follows git trailer style (`Token: value` or `Token #value`).
7. Use `BREAKING CHANGE: <description>` footer for breaking changes, or mark with `!` before `:` in the header.

## Type Guidance

- SemVer intent:
  - `fix` -> PATCH
  - `feat` -> MINOR
  - any commit with breaking change (`!` or `BREAKING CHANGE:`) -> MAJOR
- Common additional types:
  - `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`, `revert`

## Quality Heuristics

- Keep the header specific and concise.
- Prefer imperative phrasing (for example `add`, `fix`, `remove`).
- Use scope only when it improves clarity.
- Split unrelated changes into separate commits when possible.
- Use footers for issue references and review metadata (for example `Refs: #123`, `Reviewed-by: Name`).

## Examples

```text
feat(auth): add OIDC callback validation
```

```text
fix(api): prevent null pointer in order mapper

Handle missing billing address by short-circuiting mapping.

Refs: #482
```

```text
feat(ui)!: replace legacy theme tokens

BREAKING CHANGE: remove deprecated color token names from public theme API.
```
