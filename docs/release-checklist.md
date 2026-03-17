# OctoAcme — Release Checklist

## Purpose
A concise, actionable checklist to guide the Release Manager and team through each production release. Derived from the [Release & Deployment Guide](./octoacme-release-and-deployment.md) and the Release Manager role responsibilities.

> **Owner:** Release Manager  
> **Consulted:** Developers, QA Automation Engineer, DevOps Engineer, Support / On-call Engineer  
> **Informed:** PM, PdM, Stakeholders

---

## Pre-Release

### Code & Requirements
- [ ] All acceptance criteria for in-scope items are met and verified by QA
- [ ] All feature PRs are merged to the release branch; no open PRs targeting this release
- [ ] Linked issues are closed or explicitly deferred (with documented justification)

### Quality Gates
- [ ] CI pipeline passes — all automated tests green (unit, integration, end-to-end)
- [ ] Code coverage meets or exceeds the agreed threshold
- [ ] Security scan (SAST / dependency checks) completed with no unresolved high/critical findings
- [ ] Performance / load tests reviewed if applicable to the release scope
- [ ] QA Automation Engineer sign-off on test suite results

### Documentation & Communication
- [ ] Release notes drafted and reviewed (use the [Release Notes Template](./octoacme-release-and-deployment.md#release-notes-template))
- [ ] Deployment runbook updated for this release (new env vars, migration steps, feature flags)
- [ ] Rollback plan documented and shared with DevOps Engineer and Support / On-call Engineer
- [ ] Deployment window scheduled and communicated to all affected teams

### Final Approvals
- [ ] Release Manager go/no-go decision recorded
- [ ] Security Liaison sign-off obtained (if security-sensitive changes are included)
- [ ] PM and PdM notified of planned release time

---

## Deployment

### Staging Validation
- [ ] Deployed to staging environment using the production deployment pipeline
- [ ] Smoke tests executed in staging — all critical paths pass
- [ ] Any required database migrations or data backups completed in staging first

### Production Deployment
- [ ] Deployment window is active (off-peak if required by release type)
- [ ] Backup or snapshot taken (if applicable to the release type)
- [ ] Feature flags or dark-launch configuration set as intended
- [ ] Deploy to production via automated pipeline (avoid manual steps)
- [ ] Deployment logs reviewed for errors immediately after deploy

---

## Post-Deployment Verification

### System Health
- [ ] Error rates and latency are within baseline thresholds (check dashboards)
- [ ] Key user flows verified manually or via automated synthetic monitoring
- [ ] No new alerts triggered in monitoring / on-call tooling
- [ ] DevOps Engineer confirms infrastructure health

### Feature Validation
- [ ] In-scope features verified in production (spot-check by QA or Release Manager)
- [ ] Acceptance criteria validated against the live environment where feasible
- [ ] Support / On-call Engineer briefed on new behaviors and potential edge cases

---

## Communication

- [ ] Release announcement sent to Stakeholders and Support team (include release notes link)
- [ ] Internal changelog or project board updated to reflect shipped items
- [ ] PM and PdM notified that release is complete
- [ ] Any customer-facing communication (email, in-app, docs) published if required

---

## Rollback (if needed)

- [ ] Incident triggered and on-call notified per [Rollback & Incident Playbook](./octoacme-release-and-deployment.md#rollback--incident-playbook)
- [ ] Rollback decision made by Release Manager in coordination with PM and DevOps Engineer
- [ ] Rolled back to last known-good release using automated pipeline
- [ ] Post-rollback verification: error rates and user flows confirmed stable
- [ ] Stakeholders and Support informed of rollback and estimated resolution timeline
- [ ] Incident post-mortem scheduled; root cause and action items captured

---

## Related Documents
- [Release & Deployment Guide](./octoacme-release-and-deployment.md)
- [Role & Responsibility Matrix](./role-responsibility-matrix.md)
- [Roles & Personas](./octoacme-roles-and-personas.md)
- [Execution & Tracking](./octoacme-execution-and-tracking.md)
