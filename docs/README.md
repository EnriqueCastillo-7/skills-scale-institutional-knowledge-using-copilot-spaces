# OctoAcme Project Management Documentation

Welcome to the OctoAcme project management documentation. This folder contains comprehensive guides for running projects at OctoAcme, including best practices for initiation, planning, execution, release, and continuous improvement.

## Quick Start

- **New to OctoAcme?** Start with [OctoAcme Project Management Overview](./octoacme-project-management-overview.md)
- **Starting a new project?** Follow the [Project Initiation Guide](./octoacme-project-initiation.md)
- **Planning your work?** Check out [Project Planning](./octoacme-project-planning.md)
- **In delivery mode?** See [Execution & Tracking](./octoacme-execution-and-tracking.md)
- **Ready to release?** Review [Release & Deployment Guide](./octoacme-release-and-deployment.md)
- **Wrapping up?** Learn about [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md)

## OctoAcme Project Management Process Overview

### Core Approach

OctoAcme follows a structured, lifecycle-based approach to project management that emphasizes customer value, iterative delivery, clear ownership, and data-driven decisions. The framework encompasses five key phases: Initiation, Planning, Execution, Release, and Retrospective & Continuous Improvement. At its core, OctoAcme operates on principles of psychological safety and transparency, with each project assigned a named Project Manager (PM) and Product Manager (PdM) to ensure clear accountability. The organization maintains a lightweight documentation approach, using key artifacts such as Project Charters, Risk Registers, and Acceptance Criteria to align stakeholders and guide execution.

### Roles & Communication Cadence

OctoAcme defines three primary delivery personas: **Developers** who design, build, and test software while participating in planning and code reviews; **Product Managers** who define what should be built, prioritize the backlog, and measure outcomes; and **Project Managers** who coordinate delivery activities, manage risks, and maintain stakeholder alignment. Communication is structured around multiple rhythms: daily standups (15 minutes focused on progress and blockers), weekly delivery syncs between PM and PdM, twice-weekly team standups, and monthly stakeholder updates. Escalation is handled in three levels—team-level triage, PM escalation to Product Lead and dependent teams, and sponsor-level escalation for business-impacting issues.

### Execution & Quality Assurance

During the Execution phase, teams leverage GitHub Projects with standardized columns (Backlog, Ready, In Progress, In Review, QA, Done) and follow a disciplined Pull Request workflow requiring small PRs (≤400 lines when possible), automated testing and linting in CI, and at least one approval before merging. Quality practices include unit tests for new logic, integration tests where applicable, end-to-end smoke tests for critical flows, security scanning in CI, and manual QA for feature acceptance. The team tracks velocity, burndown, and key success metrics identified in the Project One-pager, using dashboards to monitor errors, latency, and usage signals.

### Release & Continuous Improvement

Releases are standardized by type (Patch, Minor, Major) and require completion of all acceptance criteria, passing CI and security scans, documented release notes, and a prepared rollback plan before deployment. The Release & Deployment phase includes pre-release requirements, a deployment checklist, and an incident playbook for quick response and rollback if needed. Finally, OctoAcme institutionalizes learning through retrospectives held after each sprint, release, or milestone, where teams capture what went well, identify improvements, assign action items with clear owners and due dates, and review outstanding actions in weekly syncs to drive continuous improvement.

## Documentation Structure

Each guide in this folder covers a specific phase or aspect of project management:

- **octoacme-project-management-overview.md** — High-level introduction to OctoAcme principles, roles, artifacts, and lifecycle
- **octoacme-project-initiation.md** — Steps to validate work, align stakeholders, and decide go/no-go
- **octoacme-project-planning.md** — Breaking work into shippable increments and creating an actionable plan
- **octoacme-execution-and-tracking.md** — Day-to-day execution, team rhythm, quality practices, and blocker escalation
- **octoacme-risks-and-communication.md** — Risk management, stakeholder communication, and escalation paths
- **octoacme-release-and-deployment.md** — Release types, pre-release requirements, deployment checklist, and rollback procedures
- **octoacme-retrospective-and-continuous-improvement.md** — Running retrospectives and converting learnings into actionable improvements
- **octoacme-roles-and-personas.md** — Detailed definitions of Developers, Product Managers, and Project Managers

## How to Use These Docs

1. **Project Kick-off:** Reference the overview and initiation guide to get started
2. **Planning:** Use the planning guide and role definitions to structure your approach
3. **During Execution:** Refer to execution & tracking, and risks & communication guides
4. **Pre-Release:** Check the release & deployment guide for requirements and checklists
5. **Post-Release:** Use the retrospective guide to capture learnings

## Adding to This Documentation

To request updates or add new content to these process documents, use the [Add Content to Project Management Process Docs](../.github/ISSUE_TEMPLATE/add-update-content-to-process-docs.yml) issue template.

---

**Last updated:** June 2026  
**Maintained by:** OctoAcme Team
