---
name: commit-message
description: Writes a clear Conventional Commits message from the staged diff. Use when the user asks for a commit message, says "commit this", or wants help splitting a large change into commits.
---

# Commit message

1. Run `git diff --staged --stat` and `git diff --staged`. If nothing is staged, tell the user and show `git status --short`.
2. If the diff mixes unrelated changes (for example a refactor plus a feature), suggest splitting it and list which files go in which commit.
3. Write the message:
   - Subject: `<type>(<optional scope>): <imperative summary>`, max 72 characters, no trailing period.
   - Types: feat, fix, refactor, perf, test, docs, build, ci, chore.
   - Body (wrap at 72): why the change was needed and anything surprising. Skip the body for trivial changes.
   - Footer: `BREAKING CHANGE: ...` when a public API, config key or schema changes; `Closes #123` when the user mentions an issue.
4. Show the message and ask before running `git commit`. Never use `--no-verify` and never amend pushed commits unless asked.
