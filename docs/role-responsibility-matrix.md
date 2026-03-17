# OctoAcme — Role & Responsibility Matrix

## Purpose
Provide a clear, at-a-glance view of who owns, contributes to, and needs to be kept informed of key activities across the OctoAcme project lifecycle.

## How to Use This Matrix

Each cell contains one of the following RACI codes:

| Code | Meaning |
|------|---------|
| **R** | **Responsible** — does the work to complete the activity |
| **A** | **Accountable** — ultimately answerable for the outcome; approves the result |
| **C** | **Consulted** — provides input and expertise; two-way communication |
| **I** | **Informed** — kept up to date on progress or decisions; one-way communication |

**Rules:**
- Every activity must have exactly **one A** (accountable owner).
- Activities can have multiple R, C, and I entries.
- When assigning owners for cross-team work, reference this matrix and add the owning role to the relevant GitHub issue or PR.

**Example row:** For *Initiation*, the Project Manager is accountable (A) and does the primary work (R). The Product Manager is consulted (C) on scope and goals, while Stakeholders are consulted (C) on business objectives and Developers are informed (I) so they can begin thinking about feasibility.

---

## RACI Matrix

| Lifecycle Activity | PM (Project Mgr) | PdM (Product Mgr) | Developer | QA Automation Engineer | Release Manager | UX Designer | Business Analyst | DevOps Engineer | Support / On-call | Security Liaison | Stakeholders |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **Initiation** — problem statement, charter, stakeholder alignment | R/A | C | I | I | I | C | C | I | I | C | C |
| **Planning** — scope, milestones, resource plan, risk register | R/A | C | C | C | C | C | R | I | I | C | I |
| **Execution** — build, code review, test, iterate | I | I | R/A | R | I | C | C | C | I | C | I |
| **QA / Testing** — automated tests, CI gates, acceptance validation | C | C | R | R/A | C | I | C | C | I | C | I |
| **Release / Deployment** — deployment, smoke tests, go/no-go | C | I | C | C | R/A | I | I | R | C | C | I |
| **Post-release Verification** — monitor, validate, verify features live | I | I | C | C | R/A | I | I | R | R | I | I |
| **Stakeholder Communication** — status updates, release notes, demos | R/A | C | I | I | C | I | I | I | I | I | I |
| **Retrospective** — learnings, action items, process improvement | R/A | C | R | R | C | C | C | C | C | C | I |
| **Risk Management** — identify, track, mitigate risks | R/A | C | C | C | C | I | C | C | C | R | I |
| **Incident Response** — triage, escalation, resolution, post-mortem | C | I | R | C | C | I | I | R | R/A | C | I |
| **Security Review** — code review, scan results, compliance sign-off | C | I | C | C | C | I | I | C | I | R/A | I |

---

## Role Abbreviations

| Short Name | Full Role |
|---|---|
| PM | Project Manager |
| PdM | Product Manager |
| Developer | Developer / Engineer |
| QA Automation Engineer | QA Automation Engineer |
| Release Manager | Release Manager |
| UX | UX Designer |
| BA | Business Analyst |
| DevOps Engineer | DevOps Engineer |
| Support / On-call | Support / On-call Engineer |
| Security Liaison | Security Liaison |

---

## Related Documents
- [Roles & Personas](./octoacme-roles-and-personas.md)
- [Release Checklist](./release-checklist.md)
- [Execution & Tracking](./octoacme-execution-and-tracking.md)
- [Risks & Communication](./octoacme-risks-and-communication.md)
