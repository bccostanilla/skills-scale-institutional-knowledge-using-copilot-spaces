# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description; explicitly link each PR to the acceptance criteria it satisfies
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)
  - For cross-team work, reference the [Role & Responsibility Matrix](./role-responsibility-matrix.md) when assigning owners to issues and PRs to ensure clear accountability

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

### CI Gates — QA Automation Engineer & DevOps Engineer
- The **QA Automation Engineer** owns the automated test suite and is responsible for maintaining CI quality gates (test pass rate, coverage thresholds). No PR should be merged if it causes the CI gate to fail without explicit sign-off from the QA Automation Engineer.
- The **DevOps Engineer** owns the CI/CD pipeline configuration, environment consistency, and deployment automation. They are the escalation point for pipeline failures, flaky infrastructure, and deployment readiness questions.
- Deployment readiness is a joint check: QA Automation Engineer confirms tests pass; DevOps Engineer confirms the pipeline and environment are healthy. Both signals are required before the Release Manager can proceed with a production deployment.

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
