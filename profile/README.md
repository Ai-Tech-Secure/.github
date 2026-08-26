<div align="center">

<img src="https://raw.githubusercontent.com/Paylegit-LLC-in/.github/main/profile/banner.png" alt="PayLegit" width="480"/>

# PayLegit

**Payment-legitimacy-first merchant risk** for banks, PSPs, and acquirers.

We continuously verify whether merchants, their content, and their payment flows are real, compliant, and safe — before onboarding and after go-live.

[Website](https://paylegit.in) · [Products](https://paylegit.in/#products) · [Contact](mailto:contact@paylegit.in) · [Request a demo](https://paylegit.in/demo)

</div>

---

## What this organisation is

[Paylegit-LLC-in](https://github.com/Paylegit-LLC-in) is the GitHub home for **PayLegit** product modules.

PayLegit is built around a shift that traditional onboarding misses: today's fraud often looks like a legitimate merchant. Payments move through pay-by-link, UPI VPAs, messaging apps, crypto wallets, and off-platform checkout while the card-monitored storefront stays clean.

This org holds the source, issues, and delivery pipelines for the modules that inspect that real payment infrastructure — aligned with **BRAM**, **VIRP**, **AML**, and **FATF**.

Product repositories are **private**. If you are a PayLegit engineer, partner, or contracted analyst and cannot see a module, ask an org owner for access.

---

## Product modules

Live production modules. Product pages live on [paylegit.in](https://paylegit.in); GitHub repos in this org use the names in the **Repo** column.

| Module | What it does | Repo |
| --- | --- | --- |
| **[Content Compliance](https://paylegit.in/products/content-compliance)** | BRAM / VIRP screening of merchant sites with quoted evidence, not keyword-only flags | `content-compliance` |
| **[KYC & Payment Shield](https://paylegit.in/products/kyc-shield)** | Pre-onboarding KYC screening plus real-time checkout / pay-by-link fraud decisions | `kyc-payment-shield` |
| **[MCC Online](https://paylegit.in/products/online-mcc-intelligence)** | Automated digital MCC from live website evidence (primary / secondary / tertiary) | `automated-mcc-online` |
| **[Mule & Shell Analysis](https://paylegit.in/products/mule-shell-detection)** | OSINT + transaction correlation for mule pass-through, shells, and multi-MID funnels | `mule-shell-surveillance` |
| **[Offline MCC](https://paylegit.in/products/offline-mcc-intelligence)** | POS / brick-and-mortar MCC from directories, listings, and on-the-ground signals | `offline-mcc` |
| **[Onboarding Risk Analysis (70+ Check)](https://paylegit.in/products/merchant-risk-surveillance)** | Fast merchant onboarding screen: WHOIS, SSL, malware, domain, and payment-surface checks | `onboarding-risk-suite` |
| **[Payment Risk Scanner](https://paylegit.in/products/payment-risk)** | Live scan of who actually collects the money — hidden rails, QR, crypto, redirect chains | `paymentrisk-scanner` |
| **[Underwriting Reports](https://paylegit.in/products/underwriting-scoring)** | Nine-phase underwriting, 0–100 scoring, audit-ready PDF / Excel / JSON | `underwriting-reports` |
| **[Worldwide Crawler](https://paylegit.in/products/worldwide-threat-discovery)** | Geo-targeted discovery of illegal commerce and scheme-policy violations | `worldwide-crawler` |
| **Scheme Shield** | BRAM / VIRP OSINT: discover → crawl → evidence → risk → case → report | `scheme-shield` |

### Platform (how we run the modules)

| System | Role | Repo |
| --- | --- | --- |
| Live Server Monitor | Fleet health, flags, agents, access | `live-server-monitor` |
| Orchestrator & Connector | Cross-module jobs and tenant wiring | `orchestrator-connector` |
| Portal Builder | Tenant portals and site delivery | `portal-builder` |
| PayLegit website | Public site — [paylegit.in](https://paylegit.in) | `paylegit-website` |

Operations dashboard: [monitor.paylegit.in](https://monitor.paylegit.in)

---

## How the modules fit together

```text
Discovery          Classify            Screen             Decide
─────────          ────────            ──────             ──────
Worldwide Crawler  MCC Online          Content Compliance Underwriting Reports
Scheme Shield      Offline MCC         Payment Risk       Onboarding Risk (70+)
                                       KYC & Payment Shield
                                       Mule & Shell
```

1. **Find** high-risk merchants and URLs (Worldwide Crawler, Scheme Shield).
2. **Classify** what they actually sell (Online / Offline MCC).
3. **Screen** content, payments, identity, and mule/shell patterns.
4. **Decide** with a scored, evidence-backed underwriting pack.

Every risk decision is meant to ship with **quoted evidence** so compliance can act and regulators can see why.

---

## Start here

### Engineers joining a module

1. Ask an org owner (`paylegit-in`) for access to the repo you will work on.
2. Read **[CONTRIBUTING.md](https://github.com/Paylegit-LLC-in/.github/blob/main/CONTRIBUTING.md)** — branch names, PRs, secrets, Docker.
3. Clone the module, copy `.env.example` → `.env`, then `docker compose up -d --build`.
4. Confirm health on the module README before changing behaviour.
5. Open a PR against `main`. Do not push secrets, production dumps, or customer evidence.

### Product / compliance / analysts

- Product narrative and capabilities: [paylegit.in](https://paylegit.in)
- Demo: [paylegit.in/demo](https://paylegit.in/demo)
- Email: [contact@paylegit.in](mailto:contact@paylegit.in)
- Partners: [partner@paylegit.in](mailto:partner@paylegit.in)

### Org owners (finish GitHub setup)

Use the **Member** view of this Overview for the internal checklist (transfer repos, pin modules, teams, branch protection). Public visitors only see this page.

---

## Repository conventions

| Rule | Detail |
| --- | --- |
| One module, one repo | Do not combine unrelated products in a single repository |
| Names | lowercase kebab-case, matching the **Repo** column above |
| Visibility | Product code is **private**; this `.github` profile repo is **public** |
| Default branch | `main` |
| Delivery | GitHub Actions deploy workflows already used by each module |
| Secrets | GitHub Environments / Actions secrets only — never commit `.env` |

---

## Security

Report vulnerabilities privately to **[contact@paylegit.in](mailto:contact@paylegit.in)**. Do not open a public issue for a security finding.

See **[SECURITY.md](https://github.com/Paylegit-LLC-in/.github/blob/main/SECURITY.md)**.

---

<div align="center">

**PayLegit LLC (India)** · [paylegit.in](https://paylegit.in) · [contact@paylegit.in](mailto:contact@paylegit.in)

Find. Prove. Score. Escalate — without crossing the line.

</div>
