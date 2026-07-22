# Agent instructions

## Project purpose

This project is both an AI medical scribe and a case study for learning strong software-engineering fundamentals.

## Learning principles

- Apply and briefly explain relevant engineering practices and trade-offs.
- Use Linear for planning and lifecycle tracking.
- Use GitHub deliberately for source control, branches, commits, pull requests, reviews, CI, and releases.
- Prefer disciplined, incremental workflows over shortcuts.
- Preserve important terminology and decisions so future sessions can continue consistently.
- Treat `AGENTS.md` as the canonical instruction file for all agents. Keep `CLAUDE.md` as a pointer to it, and make skills or setup workflows update `AGENTS.md` rather than duplicating instructions in `CLAUDE.md`.
- Treat `wt` as shorthand for the current worktree.

## Public repository and sensitive data

This repository is public. Never commit or push secrets, credentials, private keys, access tokens, personal data, patient information, protected health information (PHI), or confidential clinical content. Use synthetic or anonymized examples and keep local secrets in ignored environment files.

Before every commit and push:

- Inspect the staged diff and filenames for sensitive information.
- Run an appropriate secret scan; do not rely on filename checks alone.
- Stop the push if anything is uncertain. Remove the data from Git history and rotate or revoke exposed credentials before continuing.

## Agent skills

### Issue tracker

Issues and planning artifacts live in Linear. See `docs/agents/issue-tracker.md`.

### Triage labels

Triage uses the five canonical role names as its Linear label vocabulary. See `docs/agents/triage-labels.md`.

### Domain docs

This is a single-context repository. See `docs/agents/domain.md`.
