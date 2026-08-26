<div align="center">

<img src="https://raw.githubusercontent.com/Ai-Tech-Secure/.github/main/profile/banner.png" alt="Ai Tech Secure" width="440"/>

# Ai Tech Secure

**Platform engineering** for [PayLegit](https://github.com/Paylegit-LLC-in) — fleet monitoring, identity, and production delivery.

This organisation runs the systems that keep PayLegit modules online, authenticated, and deployable. Product source lives in **[Paylegit-LLC-in](https://github.com/Paylegit-LLC-in)**.

[monitor.paylegit.in](https://monitor.paylegit.in) · [iga.aitechsecure.com](https://iga.aitechsecure.com) · [contact@paylegit.in](mailto:contact@paylegit.in)

</div>

---

## What we operate

| System | Purpose | Production | Repository |
| --- | --- | --- | --- |
| **Live Server Monitor** | Fleet health, open flags, agents, access, and module status across VPS hosts | [monitor.paylegit.in](https://monitor.paylegit.in) | [Live-Server-Monitor](https://github.com/Ai-Tech-Secure/Live-Server-Monitor) |
| **Orchestrator & Connector** | Identity (Zitadel / IGA), SSO, and tenant wiring used by PayLegit apps | [iga.aitechsecure.com](https://iga.aitechsecure.com) | [Orchestrator-Connector](https://github.com/Ai-Tech-Secure/Orchestrator-Connector) |

Repositories are **private**. Ask an organisation owner (`paylegit-in`) for access.

Caddy for `monitor.paylegit.in` and `iga.aitechsecure.com` is deployed from [Paylegit-LLC-in/Portal-Builder](https://github.com/Paylegit-LLC-in/Portal-Builder) (`vps0.Caddyfile` on VPS-0).

---

## How delivery works

| Step | Detail |
| --- | --- |
| Default branch | `main` |
| Deploy | Push or merge to `main` runs GitHub Actions |
| Runner | Self-hosted `paylegit-vps-0` on VPS-0 (`paylegit-vps-0-ats` in this org) |
| Live Server Monitor path | `/opt/Live-Server-Monitor` → UI `:3210`, API `:8210` |
| Orchestrator path | `/opt/orchestrator-connector` → IGA `:9443` |
| Secrets | GitHub Actions repository secrets (never commit `.env`) |

Work on a feature branch does **not** deploy. Production updates only after `main` is updated.

PayLegit **product** modules deploy from [Paylegit-LLC-in](https://github.com/Paylegit-LLC-in) on a separate runner (`paylegit-vps-0-runner`). Do not register this org’s runner onto that organisation.

---

## Working here

1. Request access to [Live-Server-Monitor](https://github.com/Ai-Tech-Secure/Live-Server-Monitor) or [Orchestrator-Connector](https://github.com/Ai-Tech-Secure/Orchestrator-Connector).
2. Read [CONTRIBUTING.md](https://github.com/Ai-Tech-Secure/.github/blob/main/CONTRIBUTING.md).
3. Clone, copy `.env.example` → `.env`, bring the stack up with Docker Compose as documented in the repo.
4. Open a pull request against `main`. Confirm health locally before merge.
5. After merge, confirm [monitor.paylegit.in](https://monitor.paylegit.in) or [iga.aitechsecure.com](https://iga.aitechsecure.com) as appropriate.

---

## Sister organisation

| Organisation | Role |
| --- | --- |
| **[Paylegit-LLC-in](https://github.com/Paylegit-LLC-in)** | PayLegit product modules (MCC, KYC, Scheme Shield, crawlers, website, portals) |
| **[Ai-Tech-Secure](https://github.com/Ai-Tech-Secure)** | Platform: monitoring, identity, deploy runners for the two repos above |

---

## Security

Report vulnerabilities to **[contact@paylegit.in](mailto:contact@paylegit.in)**. Do not open a public issue.

See [SECURITY.md](https://github.com/Ai-Tech-Secure/.github/blob/main/SECURITY.md).

---

<div align="center">

**Ai Tech Secure** · platform for [PayLegit](https://paylegit.in) · [contact@paylegit.in](mailto:contact@paylegit.in)

</div>
