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
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing

### Quality Gates by Phase
Each phase must meet specific quality gates before proceeding to the next:

**Development Phase → Code Review**
- Unit tests written and passing (minimum 80% coverage for new code)
- Code follows team style guidelines and linting rules
- Documentation updated (README, API docs, inline comments as needed)
- Self-review completed by developer

**Code Review → QA**
- At least one approval from peer reviewer
- All CI checks passing (tests, linting, security scans)
- Acceptance criteria clearly documented in PR
- No unresolved review comments

**QA → Ready for Release**
- All acceptance criteria verified and passing
- Regression testing completed (no new bugs introduced)
- Known issues documented and assessed
- QA sign-off provided by assigned QA engineer
- Performance testing completed (if applicable)
- Security scan results reviewed and approved

**Ready for Release → Production**
- Release readiness checklist completed (see [Release Readiness Checklist](release-readiness-checklist.md))
- Deployment runbook tested in staging
- Rollback procedure verified
- Monitoring and alerting configured
- Stakeholder communication prepared

### Testing Requirements
- **Unit tests** for new logic and business rules
- **Integration tests** where components interact
- **End-to-end smoke tests** for critical flows before release
- **Security scanning** in CI (automated)
- **Manual QA** for feature acceptance and exploratory testing
- **Performance testing** for high-traffic features or database changes

### QA Approval Workflow
1. **Developer** moves ticket to "Ready for QA" and assigns to QA engineer
2. **QA Engineer** reviews acceptance criteria and test environment within 1 business day
3. **QA Engineer** performs testing and documents results in ticket
4. **If bugs found**: QA creates bug tickets, assigns to developer, status returns to "In Progress"
5. **If tests pass**: QA provides sign-off comment and moves ticket to "Ready for Release"
6. **Release Manager** reviews QA sign-off before including in release

### QA Sign-off Template
```
✅ QA Sign-off for [Feature Name]
- All acceptance criteria verified: ✓
- Regression testing completed: ✓
- Performance acceptable: ✓
- Known issues: [None / List issues with ticket links]
- Tested by: [QA Engineer Name]
- Date: [Date]
```

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
