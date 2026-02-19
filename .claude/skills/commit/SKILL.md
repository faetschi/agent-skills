---
name: commit
description: Create structured Git commit messages and execute commits. Use when users ask to draft commit messages, choose commit type/scope, generate commit body/footers, map changes to SemVer intent, or run git commits with clear and consistent formatting.
---

# Commit Skill

Create high-quality commit messages and run commits with Conventional Commits.

## Workflow

1. Inspect current repository changes with Git tools before writing a message.
2. Read `references/conventional-commits.md` and follow its required structure.
3. Infer the best commit type from actual code changes.
4. Use this header format: `<type>[optional scope][optional !]: <description>`.
5. Keep the description short, specific, and in imperative mood.
6. Add a body only when extra context helps reviewers.
7. Add footers for issue links, reviewers, or metadata when useful.
8. Mark breaking changes using `!` and/or a `BREAKING CHANGE:` footer.
9. If changes mix unrelated intent, recommend splitting into multiple commits.
10. Execute commit commands only when the user asks to commit (or explicitly invokes a commit command/flow).

## Commit Construction Rules

- Prefer `feat` for new features and `fix` for bug fixes.
- Use other conventional types when appropriate (`docs`, `refactor`, `test`, `chore`, `ci`, `build`, `perf`, `style`, `revert`).
- Use an optional scope for subsystem context (for example `api`, `ui`, `deps`).
- Use lower-case type and scope for consistency.
- Keep the first line concise and avoid trailing punctuation.
- When using multiple paragraphs, separate header, body, and footers with blank lines.

## Execution Rules

When committing:

1. Confirm there are changes to commit.
2. Stage intended files (default to all tracked/untracked changes unless user specifies a subset).
3. Create the commit using a properly formatted multi-line message.
4. Show the resulting commit hash and subject line.

If commit fails, surface the exact error and propose the smallest corrective action.

## Required Reference

Always follow:

- `references/conventional-commits.md`