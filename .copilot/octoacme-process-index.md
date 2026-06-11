# OctoAcme Process Index

Quick reference for all key project management processes used at OctoAcme.

## Project Lifecycle Phases

### 1. **Project Initiation**
- **Purpose:** Validate business need, align stakeholders, decide go/no-go
- **Key Deliverables:** Project One-pager, Stakeholder list, Initial risk list
- **Decision Gate:** Success metrics clear, stakeholder alignment confirmed
- **Guide:** See `docs/octoacme-project-initiation.md`

### 2. **Project Planning**
- **Purpose:** Turn approved initiative into actionable plan with prioritized backlog
- **Key Deliverables:** Backlog items with acceptance criteria, Release plan, Definition of Done
- **Activities:** Kickoff meeting, estimate scope, identify dependencies, create release timeline
- **Guide:** See `docs/octoacme-project-planning.md`

### 3. **Execution & Tracking**
- **Purpose:** Manage day-to-day execution and progress toward milestones
- **Key Cadences:** Daily standups (15 min), Weekly delivery sync, Sprint demos
- **Workflows:** GitHub Projects board (Backlog → Ready → In Progress → In Review → QA → Done)
- **Quality Gates:** Unit tests, integration tests, CI security scans, manual QA
- **Guide:** See `docs/octoacme-execution-and-tracking.md`

### 4. **Release & Deployment**
- **Purpose:** Standardize release process to reduce risk and improve observability
- **Release Types:** Patch (hotfixes), Minor (incremental features), Major (breaking changes)
- **Pre-release:** All acceptance criteria met, CI/security pass, release notes drafted, rollback plan ready
- **Post-release:** Run smoke tests, announce to stakeholders and support
- **Guide:** See `docs/octoacme-release-and-deployment.md`

### 5. **Retrospective & Continuous Improvement**
- **Purpose:** Capture learnings and convert to actionable improvements
- **When:** After each sprint, release, or milestone; also after incidents
- **Structure:** What went well, what could improve, action items with owners
- **Duration:** 45-75 minutes depending on team size
- **Guide:** See `docs/octoacme-retrospective-and-continuous-improvement.md`

## Core Roles

| Role | Responsibility |
|------|-----------------|
| **Project Manager** | Coordinates delivery, manages schedule/risk/communications, facilitates meetings |
| **Product Manager** | Defines outcomes, prioritizes backlog, measures success, validates solutions |
| **Developer** | Implements features, writes/maintains tests, participates in design/code reviews |
| **QA/Testing** | Validates quality and acceptance criteria |

See `docs/octoacme-roles-and-personas.md` for detailed role definitions.

## Key Communication Cadences

- **Daily Standup** (15 min) — focus on progress, blockers, dependencies
- **Weekly PM Sync** — PM + PdM alignment
- **Twice-weekly Delivery Sync** — team standup for delivery team
- **Weekly Stakeholder Update** — status, risks, decisions needed
- **Monthly Stakeholder Update** — high-level progress and strategic updates
- **Ad-hoc Escalation** — for critical issues or blockers

## Risk Management Escalation

| Level | Owner | Action |
|-------|-------|--------|
| **Level 1** | Team | Daily standup triage |
| **Level 2** | PM | Escalate to Product Lead + dependent teams |
| **Level 3** | Sponsor | Business-impacting issues |

See `docs/octoacme-risks-and-communication.md` for complete risk management approach.

## Quality & Testing Standards

- **Unit tests** for new logic
- **Integration tests** where applicable
- **End-to-end smoke tests** for critical flows before release
- **Security scanning** in CI
- **Manual QA** for feature acceptance when needed

See `docs/octoacme-execution-and-tracking.md` for full quality practices.

## Pull Request Workflow

1. Create branch from latest `main`
2. Keep PR ≤ 400 lines when possible
3. Include issue link and acceptance criteria in PR description
4. Run automated tests and linting in CI
5. Require at least one approval before merge (or team-defined policy)
6. Merge and monitor for any issues

## Decision Gates

**Go/No-Go for Planning:** Success metrics clear, stakeholders agree on priority, team availability confirmed

**Ready for Release:** All acceptance criteria met, CI/security pass, release notes drafted, rollback plan ready

**Release Complete:** Smoke tests pass, post-deploy verifications pass, stakeholders and support notified

---

**For detailed guidance on any process, reference the corresponding document in `docs/`.**
