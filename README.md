# Claude Commit Message Skill

One free [Claude Code](https://docs.claude.com/en/docs/claude-code) skill that writes Conventional Commits messages from your staged diff.

## Install

Copy the skill folder into your project or your home skills directory:

```bash
# project (share with the team via git)
mkdir -p .claude/skills
cp -R skills/commit-message .claude/skills/

# or personal (every project on this machine)
mkdir -p ~/.claude/skills
cp -R skills/commit-message ~/.claude/skills/
```

In Claude Code, run `/commit-message` or ask it to write a commit message.

## What you get

- Conventional Commits subject + optional body/footer
- Suggests splitting mixed diffs
- Asks before running `git commit` (never `--no-verify`)

## Full pack

This is **one free sample**. The [Claude Code Skills Pack](https://shipreadyagents.com/templates/claude-code-skills-pack) includes 8 skills (review, tests, debug, refactor, security, commits, PRs, docs) plus an installer.

Guide: [Claude Code Skills Examples](https://shipreadyagents.com/blog/claude-code-skills-examples)

## License

MIT
