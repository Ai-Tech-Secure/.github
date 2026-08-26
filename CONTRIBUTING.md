# Contributing (Ai Tech Secure)

Applies to [Live-Server-Monitor](https://github.com/Ai-Tech-Secure/Live-Server-Monitor) and [Orchestrator-Connector](https://github.com/Ai-Tech-Secure/Orchestrator-Connector).

## Rules

- Default branch is `main`. Merge to `main` deploys to VPS-0.
- Copy `.env.example` → `.env`. Never commit secrets.
- Do not change published host ports without checking Caddy (`monitor.paylegit.in`, `iga.aitechsecure.com`) and Live Server Monitor.
- Do not disable auth or SSO “just for testing” on `main`.
- Prefer `feat/` and `fix/` branches; keep pull requests focused.

## Verify before merge

- Stack starts (`docker compose` or the repo’s documented command).
- Health / login path works.
- Diff contains no `.env` or customer data.

Questions: org owner `paylegit-in`, or [contact@paylegit.in](mailto:contact@paylegit.in).
