# TuleBank Skill — AGENTS Context

## Purpose

Public source of truth for TuleBank agent instructions in `skills/tulebank/SKILL.md`.

The product depends on this skill being public and usable by agents together with the CLI.

## Key File

- `skills/tulebank/SKILL.md` — canonical skill definition and behavior rules

## Publishing Workflow

1. Update `skills/tulebank/SKILL.md`
2. Commit + push to the public repository
3. Publish via:
   - `clawhub publish skills/tulebank --version <semver> --changelog "..."`

## Contract with CLI

- `SKILL.md` must reflect actual CLI commands and flags from `tulebank-cli`.
- Keep `tulebank-cli/test/skill.test.js` passing after any skill or CLI change.
- Do not hardcode local absolute paths in `SKILL.md`.
- Do not include direct API credentials or secret material in skill content.

## Sensitive Operational Notes

If you need temporary account-specific examples while authoring the skill, store them in repo-root `.local/ops-runbook.md` (gitignored), not in tracked skill docs.

