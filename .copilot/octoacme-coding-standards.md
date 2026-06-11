# OctoAcme Development Standards & Best Practices

Guidelines for writing code, documentation, and processes that align with OctoAcme standards.

## Code Quality Standards

### Testing Requirements
- ✅ Write unit tests for all new business logic
- ✅ Aim for >80% code coverage on new code
- ✅ Include integration tests for cross-component interactions
- ✅ Add end-to-end tests for critical user flows
- ✅ Run security scanning on all code changes

### Pull Request Standards
- **Size:** Keep PRs ≤ 400 lines when possible for easier review
- **Description:** Always include:
  - Link to the related issue (e.g., `Closes #123`)
  - Summary of changes
  - Acceptance criteria
- **Testing:** Verify CI passes and all automated tests succeed
- **Reviews:** Require at least one approval before merging
- **Branch:** Create from latest `main`

### Code Review Checklist
- [ ] Code follows OctoAcme naming conventions
- [ ] All tests pass and coverage maintained/improved
- [ ] Documentation updated if needed
- [ ] Security review completed (if applicable)
- [ ] Performance implications considered
- [ ] Backward compatibility maintained or breaking changes documented

## Documentation Standards

### README Files
- Include clear overview and quick-start guide
- List main features and key sections
- Provide links to detailed documentation
- Include examples when helpful

### Process Documentation
- Use clear headings and numbered steps
- Include purpose, objectives, and deliverables
- Add checklists for key activities
- Link to related processes and templates
- Keep content current and version-controlled

### Issue Templates
- Use consistent structure across all issues
- Include description fields for context
- Add fields for acceptance criteria
- Use labels for categorization
- Link related issues and documentation

## Architecture & Design Principles

### Customer-First Design
- Prioritize customer value and usability
- Validate assumptions through user research
- Measure impact of features against success metrics

### Iterative Delivery
- Break work into shippable increments
- Deploy frequently (at least weekly or per sprint)
- Gather feedback early and often
- Iterate based on data and user feedback

### Clear Ownership
- Each project has named PM and Product Lead
- Each task has clear owner and due date
- Decisions are documented with rationale
- Escalation paths are clear

### Data-Informed Decisions
- Measure all feature impact
- Track key metrics (velocity, quality, customer satisfaction)
- Use dashboards for visibility
- Retrospectives focus on metrics

## Performance & Reliability

### Monitoring & Observability
- Add logging and metrics to critical flows
- Use structured logging (JSON format preferred)
- Include traceability (request IDs, correlation IDs)
- Set up alerts for error spikes or performance degradation

### Release Readiness
- All acceptance criteria must be met
- CI/CD pipeline must pass (tests, linting, security)
- Release notes must be drafted with clear descriptions
- Rollback plan must be documented and tested
- Smoke tests prepared and ready to run

### Post-Release
- Run smoke tests in production
- Monitor error rates and performance metrics
- Verify stakeholder and support notifications sent
- Be ready to rollback if critical issues found

## Naming Conventions

### Branch Names
- Feature: `feature/short-description`
- Bugfix: `bugfix/short-description`
- Hotfix: `hotfix/short-description`
- Example: `feature/add-project-dashboard`

### Commit Messages
- Use imperative mood: "Add feature" not "Added feature"
- Start with verb: Add, Fix, Update, Remove, Refactor
- Include ticket number: "Add dashboard (#123)"
- Keep first line ≤ 50 characters
- Add detailed description if needed (separated by blank line)

### File Naming
- Use kebab-case for files: `process-initiation.md`
- Use camelCase for variables and functions
- Use UPPER_CASE for constants
- Use PascalCase for classes and components

## Collaboration & Communication

### Standups
- Daily 15-minute synchronization
- Focus on progress, blockers, and dependencies
- Surface risks early
- Keep it brief and actionable

### Code Review Process
- Review PRs within 24 hours when possible
- Leave constructive feedback
- Ask questions if something is unclear
- Approve when satisfied with quality

### Issue Templates
- Use provided issue templates consistently
- Fill in all required fields
- Link related issues and PRs
- Keep issues updated as they progress

### Escalation
- Level 1: Team triage in daily standup
- Level 2: PM escalates to Product Lead + dependent teams
- Level 3: Sponsor escalation for business-impacting issues
- Follow communication plan for severity levels

---

**Questions?** Reference the main process docs in `docs/` or ask your team lead.
