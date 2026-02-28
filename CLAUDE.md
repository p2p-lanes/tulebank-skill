# TuleBank Skill — Developer Context

## What This Repo Is
- Public repo (`p2p-lanes/tulebank-skill`) containing the Claude Code skill for TuleBank
- Single source of truth for SKILL.md distribution via ClawHub
- External install: `npx skills add p2p-lanes/tulebank-skill` or via ClawHub registry

## Key Files
- `skills/tulebank/SKILL.md` — the skill definition (frontmatter + instructions for Claude Code)

## Editing Workflow
1. Edit `skills/tulebank/SKILL.md` in this repo
2. Commit and push: `git add -A && git commit -m "..." && git push origin main`
3. Publish: `clawhub publish skills/tulebank --version <semver> --changelog "..."`

## Relationship to CLI
- The sibling `../tulebank-cli/` repo has the actual CLI implementation
- SKILL.md references CLI commands — when CLI commands change, update SKILL.md to match
- `../tulebank-cli/test/skill.test.js` validates SKILL.md content (commands match help output, no stale references)
- SKILL.md is NOT included in the npm package (not in `package.json` `files` array)

## Rules
- SKILL.md must not hardcode local paths (e.g., `/bin/tulebank.js` or `node /...`)
- SKILL.md must not reference removed commands or direct API credentials
- All CLI commands mentioned in SKILL.md must exist in `tulebank help` output
