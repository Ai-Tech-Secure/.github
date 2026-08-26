# Contributing to PayLegit modules

This guide applies to repositories under [Paylegit-LLC-in](https://github.com/Paylegit-LLC-in) unless a module README says otherwise.

## Before you start

- Confirm you can see the **private** module repo. If not, ask an org owner (`paylegit-in`) for access.
- Read that module's `README.md` and any `DEPLOYMENT.md` / `MODULE_GUIDE.md`.
- Copy `.env.example` to `.env`. Never commit `.env`, credentials, or customer evidence.

## Local run

Most modules are Docker-first:

```bash
docker compose up -d --build
```

Use the ports and health URLs in the module README. Do not change published host ports without checking Live Server Monitor and the reverse proxy.

## Branches

| Branch | Use |
| --- | --- |
| `main` | Production-track. Protected once branch rules are on. |
| `feat/<short-name>` | New behaviour |
| `fix/<short-name>` | Bug fix |
| `chore/<short-name>` | Deps, CI, docs-only |

Keep branches short-lived. Prefer one concern per PR.

## Pull requests

- Fill in the PR template: what changed, why, how you verified it.
- Include screenshots or API samples when the UI or a public endpoint changes.
- Do not include secrets, production database dumps, or raw merchant PII.
- CI / deploy workflows must stay green on `main`.

## What we do not merge

- Hard-coded production passwords, API keys, or tokens
- `node_modules`, Python venv, or build artefacts
- Changes that disable auth, RBAC, or tenant isolation "just for testing"
- Scraping or testing practices that violate the module's legal / ToS boundaries (especially Scheme Shield)

## Questions

- Engineering: open a discussion or issue on the relevant private repo
- Product / commercial: [contact@paylegit.in](mailto:contact@paylegit.in)
