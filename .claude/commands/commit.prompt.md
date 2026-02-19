---
agent: agent
description: Analyze git changes, generate a Conventional Commits message, and create a commit.
---

Use the `commit` skill.

Goal: create a well-structured Conventional Commits message and commit the current changes.

Workflow:

1. Inspect current changed files and diff summary.
2. Infer the best commit type/scope from the actual code changes.
3. Draft a commit message using this structure:

   ```text
   <type>[optional scope][optional !]: <description>

   [optional body]

   [optional footer(s)]
   ```

4. If the changes are mixed and should be split, propose split commits first.
5. If the user asked for message-only, stop after drafting.
6. Otherwise stage changes and run `git commit` with the drafted message.
7. Return the final message and the resulting commit hash.

Rules:

- Follow Conventional Commits 1.0.0.
- Use `feat` for features and `fix` for bug fixes.
- Use `!` and/or `BREAKING CHANGE:` for breaking changes.
- Keep subject concise and specific.
- Never invent details not present in the diff.