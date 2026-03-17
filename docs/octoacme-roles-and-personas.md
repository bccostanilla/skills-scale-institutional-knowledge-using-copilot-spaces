# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## Release Manager

### Role Summary
The Release Manager oversees release readiness and coordinates between development, QA, and operations to ensure safe, timely deployments. They own the release schedule, deployment runbooks, and rollback plans.

### Responsibilities
- Coordinate code freezes and release windows with Developers and QA
- Validate that all pre-release criteria are met (CI, acceptance tests, security scans)
- Maintain the deployment runbook and rollback playbook
- Communicate release status and timelines to stakeholders and support teams
- Own post-release verification and incident escalation if a deployment fails

### Goals
- Minimize deployment risk and unplanned downtime
- Ensure all release artifacts and documentation are complete before go-live
- Provide clear, timely communication to all affected parties

### Typical Communication
- Coordinates code freeze dates with Developers and PM
- Syncs with QA on acceptance validation and smoke test results
- Reports release status to PdM and Stakeholders
- Escalates incidents to Support / On-call Engineer and DevOps Engineer

---

## UX Designer

### Role Summary
The UX Designer owns the user experience across features and releases. They conduct user research, create prototypes and interaction specs, and validate that delivered features meet usability goals.

### Responsibilities
- Conduct user research and usability testing to inform feature design
- Create wireframes, prototypes, and interaction specifications
- Collaborate with PdM on user feedback and feature validation
- Review implemented features against design specs and flag discrepancies
- Contribute to acceptance criteria for user-facing changes

### Goals
- Deliver intuitive, accessible user experiences
- Reduce post-release usability issues through early validation
- Align design decisions with product strategy and user needs

### Typical Communication
- Design reviews with Developers and PdM during planning and execution
- Usability test readouts shared with PM and stakeholders
- Acceptance criteria contributions reviewed with QA

---

## QA Automation Engineer

### Role Summary
The QA Automation Engineer maintains automated test suites and CI/CD quality gates to prevent regressions and validate release readiness. They collaborate closely with Developers and the Release Manager on test coverage and deployment criteria.

### Responsibilities
- Build and maintain automated test suites (unit, integration, end-to-end)
- Define and enforce CI quality gates (test pass rate, coverage thresholds)
- Collaborate with Developers on testability and regression prevention
- Work with the Release Manager to define acceptance test criteria for each release
- Report test results and coverage metrics to PM and stakeholders

### Goals
- Ensure high test coverage and reliable CI pipelines
- Catch defects early to reduce cost of fixing issues in production
- Provide clear, actionable test reports to inform release decisions

### Typical Communication
- Daily sync with Developers on failing tests and coverage gaps
- Release readiness reports shared with Release Manager and PM
- CI gate status surfaced in PR reviews and project boards

---

## Business Analyst

### Role Summary
The Business Analyst translates business requirements into actionable tasks and acceptance criteria, bridging communication between PdM, PM, and technical teams. They ensure that what is built aligns with stakeholder needs and measurable outcomes.

### Responsibilities
- Elicit, document, and validate business requirements
- Author or co-author acceptance criteria with PdM and PM
- Facilitate requirement walkthroughs with Developers and QA
- Track requirement coverage and flag gaps or conflicts
- Support stakeholder sign-off by mapping features to business objectives

### Goals
- Reduce ambiguity in requirements to lower rework
- Ensure traceability from business need to delivered feature
- Improve alignment between technical teams and business stakeholders

### Typical Communication
- Requirement walkthroughs with Developers during planning
- Acceptance criteria reviews with QA and PdM
- Status updates to PM and Stakeholders on requirement sign-off

---

## DevOps Engineer

### Role Summary
The DevOps Engineer owns the CI/CD pipelines, infrastructure as code, environment management, and observability tooling that enable reliable, repeatable delivery. They work with Developers on code health and with PM on delivery velocity.

### Responsibilities
- Build and maintain CI/CD pipelines and deployment automation
- Manage infrastructure as code and environment configurations
- Instrument monitoring, alerting, and logging for production systems
- Collaborate with Developers to improve build times and deployment reliability
- Support the Release Manager during deployments and incident response

### Goals
- Enable fast, safe, and repeatable deployments
- Reduce environment inconsistencies and flaky pipelines
- Ensure production systems are observable and recoverable

### Typical Communication
- Pair with Developers on pipeline improvements and build failures
- Brief PM and Release Manager on deployment readiness and environment status
- On-call escalation with Support / On-call Engineer during incidents

---

## Support / On-call Engineer

### Role Summary
The Support / On-call Engineer is the first responder for production incidents and user-reported issues. They triage, escalate, and coordinate resolution while maintaining a feedback loop with the development team to prevent recurrence.

### Responsibilities
- Monitor production systems and respond to alerts and user reports
- Triage and classify incidents by severity and impact
- Escalate to Developers, DevOps Engineer, or Release Manager as appropriate
- Document incident timelines, root cause, and action items
- Provide feedback to PM and PdM on recurring issues affecting users

### Goals
- Minimize mean time to resolve (MTTR) for production incidents
- Provide a clear escalation path that reduces confusion during outages
- Surface user-impacting issues to the product and development team promptly

### Typical Communication
- Incident channels and runbooks shared with DevOps Engineer and Release Manager
- Post-incident summaries reported to PM and PdM
- Feature feedback loop with PdM for recurring support patterns

---

## Security Liaison

### Role Summary
The Security Liaison ensures that security requirements are incorporated throughout the project lifecycle, from design to deployment. They conduct security reviews, coordinate vulnerability assessments, and advise the team on risk mitigation.

### Responsibilities
- Review designs and PRs for security risks and compliance gaps
- Coordinate security scans (SAST, DAST, dependency checks) in CI
- Maintain a register of open security findings and remediation owners
- Advise PdM and PM on regulatory or compliance requirements
- Partner with the Release Manager on security sign-off before production releases

### Goals
- Integrate security early ("shift left") to reduce remediation cost
- Ensure all releases meet the organization's security and compliance standards
- Maintain clear visibility into the security posture of the product

### Typical Communication
- Security review sessions with Developers and DevOps Engineer during design and execution
- Pre-release security sign-off with Release Manager and PM
- Compliance status updates to PdM and Stakeholders

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- See [Role & Responsibility Matrix](./role-responsibility-matrix.md) for a cross-role ownership view across the project lifecycle.

