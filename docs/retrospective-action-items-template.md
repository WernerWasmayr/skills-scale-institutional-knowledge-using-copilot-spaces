# Retrospective Action Items Template

## Purpose
This template provides a structured format for capturing, tracking, and measuring the success of action items identified during sprint, release, or incident retrospectives.

---

## How to Use This Template

1. **During Retrospective**: Capture action items using the format below
2. **Prioritize**: Focus on 2-3 high-impact action items per retrospective
3. **Assign Ownership**: Each action must have a single, specific owner
4. **Set Success Criteria**: Define clear, measurable outcomes
5. **Track Progress**: Review in weekly PM syncs and team meetings
6. **Measure Impact**: Validate that changes achieve intended results
7. **Close Loop**: Update stakeholders on completion and learnings

---

## Action Item Format

### Action Item #[Number]

**Title**: [Brief, action-oriented title starting with a verb]

**Category**: [Select one]
- 🔧 Process Improvement
- 🛠️ Tooling & Automation
- 📚 Documentation
- 🎯 Quality & Testing
- 💬 Communication
- 🎓 Training & Onboarding
- ⚡ Performance
- 🔒 Security
- 🔍 Monitoring & Observability
- 👥 Team Culture

**Description**: 
[Detailed description of what needs to be done and why. Include context from the retrospective discussion.]

**Root Cause/Trigger**: 
[What problem or gap prompted this action? What went wrong or could be improved?]

**Owner**: [Single person responsible - use full name]

**Collaborators**: [Optional - others who will help]

**Priority**: [Select one]
- 🔴 High - Blocking or high-impact issue, must complete ASAP
- 🟡 Medium - Important improvement, complete within sprint/milestone
- 🟢 Low - Nice to have, complete when capacity allows

**Due Date**: [Specific date - YYYY-MM-DD]

**Estimated Effort**: [Select one]
- Small (< 4 hours)
- Medium (1-3 days)
- Large (> 3 days)

**Success Criteria**: 
[Clear, measurable outcomes that define "done". Be specific!]
1. [Criterion 1 - e.g., "95% of PRs reviewed within 24 hours"]
2. [Criterion 2 - e.g., "Zero incidents related to this issue in next sprint"]
3. [Criterion 3 - e.g., "Team survey shows 8/10 satisfaction with new process"]

**Measurement Method**:
[How will you measure success? What metrics, surveys, or observations?]
- Metric: [Name and source]
- Baseline: [Current state]
- Target: [Desired state]
- Review Date: [When to assess]

**Dependencies**: 
[List any blockers or prerequisites]
- [Dependency 1]
- [Dependency 2]

**Related Issues/Tickets**: 
[Link to GitHub issues, Jira tickets, or other tracking systems]
- [Issue #123]
- [Ticket-456]

**Status**: [Select one]
- 📋 Not Started
- 🏗️ In Progress
- ⏸️ Blocked
- ✅ Completed
- ❌ Cancelled

**Status Notes**:
[Updates on progress, blockers, or changes]
- [Date]: [Update note]
- [Date]: [Update note]

**Completion Evidence**:
[When completed, provide proof of completion - links, screenshots, metrics]
- [Evidence 1]
- [Evidence 2]

**Impact Assessment**:
[After implementation, assess actual impact vs. expected]
- Did this achieve the intended outcome? Yes/No
- What was the measured impact? [Data/metrics]
- What did we learn?
- Should we adjust or iterate further?

---

## Example Action Items

### Example 1: Process Improvement

**Action Item #1**

**Title**: Establish PR size guidelines and automated checks

**Category**: 🔧 Process Improvement

**Description**: 
During retrospective, team noted that large PRs (>500 lines) take 3-5 days to review, creating bottlenecks. We will establish guidelines limiting PRs to 400 lines and add automated PR checks to warn reviewers about oversized PRs.

**Root Cause/Trigger**: 
3 features in last sprint had PRs >1000 lines, causing review delays and missed deadlines. Team consensus that smaller PRs would improve velocity and code quality.

**Owner**: Jordan Smith (Engineering Lead)

**Collaborators**: DevOps team for CI configuration

**Priority**: 🟡 Medium

**Due Date**: 2026-02-28

**Estimated Effort**: Medium (2 days)

**Success Criteria**: 
1. PR guidelines document published and shared with team
2. Automated PR size check configured in CI (warning at 400 lines, error at 600 lines)
3. 80% of PRs in next sprint are ≤400 lines
4. Average PR review time reduced from 3 days to 1.5 days

**Measurement Method**:
- Metric: GitHub PR analytics and review time
- Baseline: Average 3 days review time, 40% of PRs >400 lines
- Target: Average 1.5 days review time, 80% of PRs ≤400 lines
- Review Date: 2026-03-15

**Dependencies**: 
- None

**Related Issues/Tickets**: 
- Issue #234: Document PR process improvements

**Status**: 🏗️ In Progress

**Status Notes**:
- 2026-02-15: Guidelines drafted, under team review
- 2026-02-20: CI check implemented in dev environment
- 2026-02-25: Tested and deployed to production

**Completion Evidence**:
- Guidelines: [Link to doc]
- CI configuration: [Link to PR]
- Metrics dashboard: [Link showing improvement]

**Impact Assessment**:
- Achieved target: Yes, average review time now 1.4 days
- Measured impact: 85% of PRs now ≤400 lines, reviews 54% faster
- Learning: Team initially resistant but quickly saw benefits
- Iteration: Will add exception process for necessary large PRs

---

### Example 2: Tooling & Automation

**Action Item #2**

**Title**: Automate staging environment refresh from production data

**Category**: 🛠️ Tooling & Automation

**Description**: 
QA frequently encounters issues where staging environment has stale or incomplete data, leading to test failures and wasted time. Implement automated daily refresh of staging database from sanitized production snapshot.

**Root Cause/Trigger**: 
5 bugs in last sprint were found in production but not caught in QA because staging data didn't reflect production state. QA team spent 4 hours weekly manually refreshing data.

**Owner**: Alex Chen (DevOps Engineer)

**Collaborators**: Database team for sanitization script

**Priority**: 🔴 High

**Due Date**: 2026-02-22

**Estimated Effort**: Large (4 days)

**Success Criteria**: 
1. Automated job runs daily at 2 AM to refresh staging database
2. PII is properly sanitized in automated process
3. Staging refresh completes in <2 hours
4. Zero QA test failures due to stale data in next sprint
5. QA team saves 4 hours/week on manual data management

**Measurement Method**:
- Metric: Staging environment freshness and QA time savings
- Baseline: Manual weekly refreshes, 2-3 day lag, 4 hrs/week QA effort
- Target: Automated daily refreshes, <1 day lag, 0 hrs/week QA effort
- Review Date: 2026-03-08

**Dependencies**: 
- Database team to provide PII sanitization rules
- Security approval for automated data access

**Related Issues/Tickets**: 
- Issue #456: Staging environment improvements
- Security review ticket: SEC-789

**Status**: ✅ Completed

**Status Notes**:
- 2026-02-16: Design approved by security team
- 2026-02-18: Sanitization script created and tested
- 2026-02-21: Automation deployed and first successful run
- 2026-02-22: Monitoring confirms daily runs successful

**Completion Evidence**:
- Automation script: [Link to repo]
- Security approval: [Link to review]
- Monitoring dashboard: [Link showing daily runs]
- QA feedback: "Game changer - saving huge amount of time"

**Impact Assessment**:
- Achieved target: Yes, all success criteria met
- Measured impact: QA reports 5 hours/week saved, 100% data freshness, zero stale-data bugs in subsequent sprint
- Learning: Should have done this sooner - ROI was immediate
- Iteration: Will expand to other test environments

---

### Example 3: Communication

**Action Item #3**

**Title**: Create weekly engineering newsletter for cross-team visibility

**Category**: 💬 Communication

**Description**: 
Teams working on different components lack visibility into each other's work, leading to duplicate efforts and missed opportunities for collaboration. Start a weekly engineering newsletter highlighting completed work, upcoming changes, and learning opportunities.

**Root Cause/Trigger**: 
Two teams independently built similar caching solutions. Also, breaking API changes surprised downstream consumers twice in last month.

**Owner**: Sam Johnson (PM)

**Collaborators**: Team leads contribute content weekly

**Priority**: 🟡 Medium

**Due Date**: 2026-03-01 (first newsletter published)

**Estimated Effort**: Small (2 hours setup + 1 hour/week ongoing)

**Success Criteria**: 
1. Newsletter template created and approved
2. Weekly newsletter published every Friday for 4 consecutive weeks
3. At least 80% of engineering team opens newsletter
4. At least 2 collaboration opportunities identified through newsletter visibility
5. Survey shows 70% of engineers find newsletter valuable

**Measurement Method**:
- Metric: Email open rates and team survey
- Baseline: No formal cross-team communication mechanism
- Target: 80% open rate, positive survey results
- Review Date: 2026-04-01

**Dependencies**: 
- None

**Related Issues/Tickets**: 
- None

**Status**: 📋 Not Started

**Status Notes**:
- Will begin after sprint planning

---

## Action Item Tracking Board

Use this table to track multiple action items from a retrospective:

| # | Title | Owner | Priority | Due Date | Status | Success Metric |
|---|-------|-------|----------|----------|--------|----------------|
| 1 | [Action 1] | [Name] | 🔴 High | 2026-02-28 | 🏗️ In Progress | [Metric] |
| 2 | [Action 2] | [Name] | 🟡 Medium | 2026-03-15 | 📋 Not Started | [Metric] |
| 3 | [Action 3] | [Name] | 🟢 Low | 2026-03-31 | 📋 Not Started | [Metric] |

---

## Action Item Review Cadence

### Weekly PM Sync
- **Review**: Status updates for all in-progress action items
- **Focus**: Identify and unblock any blockers
- **Duration**: 10-15 minutes

### Sprint Retrospective
- **Review**: Completion status of previous action items
- **Assess**: Impact of completed actions
- **Create**: New action items for next sprint

### Monthly Leadership Review
- **Review**: Trends across multiple retrospectives
- **Assess**: Overall improvement trajectory
- **Adjust**: Strategy for continuous improvement

---

## Success Criteria Best Practices

### Good Success Criteria (Specific, Measurable, Achievable)
✅ "Reduce average PR review time from 3 days to 1.5 days"
✅ "Achieve 95% test coverage for payment processing module"
✅ "Zero production incidents related to deployment process in next quarter"
✅ "100% of team members complete security training by end of month"
✅ "Decrease page load time from 3s to 1.5s for dashboard"

### Poor Success Criteria (Vague, Not Measurable)
❌ "Improve code review process"
❌ "Better test coverage"
❌ "Fewer bugs"
❌ "Be more proactive"
❌ "Faster deployments"

### Converting Poor to Good Criteria
- "Improve code review process" → "Establish PR guidelines and reduce review time from 3 days to 1.5 days"
- "Better test coverage" → "Increase unit test coverage from 65% to 85% for API layer"
- "Fewer bugs" → "Reduce P1/P0 production bugs from 8/month to <3/month"
- "Be more proactive" → "Identify and document 100% of sprint dependencies in planning"
- "Faster deployments" → "Reduce deployment time from 45 minutes to 15 minutes"

---

## Common Action Item Categories & Examples

### 🔧 Process Improvement
- Streamline standup format
- Improve sprint planning efficiency
- Establish code review guidelines
- Define done criteria

### 🛠️ Tooling & Automation
- Automate manual deployment steps
- Implement automated testing
- Set up CI/CD pipeline improvements
- Configure better development tools

### 📚 Documentation
- Update outdated API documentation
- Create onboarding guide for new developers
- Document architectural decisions
- Write troubleshooting guides

### 🎯 Quality & Testing
- Increase test coverage
- Implement integration testing
- Add performance testing
- Improve QA processes

### 💬 Communication
- Improve stakeholder updates
- Establish cross-team sync meetings
- Create better status reporting
- Enhance incident communication

### 🎓 Training & Onboarding
- Create learning resources
- Conduct knowledge sharing sessions
- Improve onboarding process
- Skill development programs

### ⚡ Performance
- Optimize slow database queries
- Improve page load times
- Reduce memory usage
- Scale infrastructure

### 🔒 Security
- Address security vulnerabilities
- Implement security best practices
- Improve access controls
- Enhance security monitoring

### 🔍 Monitoring & Observability
- Add better logging
- Create dashboards
- Implement alerting
- Improve error tracking

### 👥 Team Culture
- Improve work-life balance
- Increase psychological safety
- Foster innovation time
- Celebrate team wins

---

## Retrospective Action Item Archive

Keep completed action items in an archive for reference and pattern analysis:

### Sprint 10 Retrospective - 2026-01-15
- ✅ Action 1: [Title] - Impact: [Summary]
- ✅ Action 2: [Title] - Impact: [Summary]
- ❌ Action 3: [Title] - Cancelled: [Reason]

### Release 2.0 Retrospective - 2026-01-20
- ✅ Action 1: [Title] - Impact: [Summary]
- ✅ Action 2: [Title] - Impact: [Summary]

### Incident INC-2026-01-25 Retrospective
- ✅ Action 1: [Title] - Impact: [Summary]

---

## Integration with Other Processes

This template integrates with:
- [OctoAcme Retrospective and Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md) - Overall retrospective process
- [OctoAcme Execution and Tracking](octoacme-execution-and-tracking.md) - Track action items in project board
- [Incident Response Template](incident-response-template.md) - Post-incident action items
- [Release Readiness Checklist](release-readiness-checklist.md) - Release retrospective actions

---

*Last Updated: 2026-02-13*
*Review and update this template based on team feedback and evolving needs*
