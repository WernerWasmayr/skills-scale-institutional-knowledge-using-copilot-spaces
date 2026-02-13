# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Maintain a simple table with:
- ID
- Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status
- Date identified
- Last reviewed date

## Risk Impact & Likelihood Definitions

### Impact Levels
- **High**: Could cause project failure, major delays (>2 weeks), significant cost overruns (>20%), or critical production outages
- **Medium**: Could cause moderate delays (1-2 weeks), budget impact (10-20%), or degraded service
- **Low**: Minor impact on timeline (<1 week), minimal budget impact (<10%), or cosmetic issues

### Likelihood Levels
- **High**: Probability >60% of occurring
- **Medium**: Probability 30-60% of occurring
- **Low**: Probability <30% of occurring

## Risk Tolerance & Acceptance Thresholds

### Automatic Escalation Required
- Any **High Impact + High Likelihood** risk → Escalate to Product Lead immediately
- Any risk blocking critical path → Escalate to PM within 24 hours
- Any security or compliance risk → Escalate to Security team immediately

### Risk Acceptance Authority
- **Low Impact + Low Likelihood**: Team can accept risk with PM approval
- **Medium risks**: Require PM and Product Manager approval to accept
- **High risks**: Require Product Lead or Director approval to accept

## Risk Lifecycle
- **Identify**: during planning and ongoing execution
- **Assess**: estimate impact and likelihood using definitions above
- **Mitigate**: reduce via actions, contingency plans, or risk acceptance
- **Monitor**: review at weekly syncs and update status
- **Close**: document resolution and lessons learned

## Risk Reporting Schedule
- **Daily**: Report newly identified High/High risks immediately
- **Weekly**: Review all active risks in PM sync, update status and mitigation progress
- **Monthly**: Present risk summary to stakeholders with trend analysis
- **Per Release**: Include open risks in release readiness review

## Stakeholder Communication

### Stakeholder Identification
Identify and document stakeholder groups and their communication needs:
- **Engineering Teams**: Technical updates, dependency information, API changes
- **Sales**: Feature availability, customer impact, release dates
- **Support**: Known issues, workarounds, escalation procedures
- **Executive Sponsors**: High-level progress, risks, budget status
- **Customers**: Feature announcements, maintenance windows, incident updates

### Communication Cadence
- **Daily**: Team standups, critical blocker notifications
- **Weekly**: PM status updates to leads, risk register reviews
- **Bi-weekly**: Sprint demos and reviews
- **Monthly**: Executive sponsor updates, stakeholder briefings
- **Milestone-based**: Release announcements, major feature launches
- **As-needed**: Incident communications, critical decision requests

### Single Source of Truth
Maintain project status in one of:
- Project README.md for ongoing projects
- GitHub Projects board for task tracking
- Release documentation for deployment status
- Risk register for risk management

## Communication Templates

### Weekly Status Template
**Week of [Date]**
- **Progress this week**: 
  - [Completed item 1]
  - [Completed item 2]
- **Next steps**: 
  - [Planned item 1]
  - [Planned item 2]
- **Risks & blockers**: 
  - [Risk ID]: [Brief description] - [Status]
- **Ask / decisions needed**: 
  - [Decision 1] - Owner: [Name], By: [Date]
- **Metrics update**: [Key metrics if applicable]

### Dependency Communication Template
When communicating cross-team dependencies:
- **Requesting Team**: [Team name]
- **Providing Team**: [Team name]
- **Dependency Description**: [What is needed]
- **Required By Date**: [Date]
- **Impact if Delayed**: [Impact level and description]
- **Point of Contact**: [Name and contact info]
- **Current Status**: [On track / At risk / Blocked]

### Incident Communication Workflow
See [Incident Response Template](incident-response-template.md) for detailed procedures.

**Initial Notification (within 15 minutes of detection)**
- **Incident Summary**: [Brief description]
- **Impact**: [Affected systems/users]
- **Severity**: [Critical/High/Medium/Low]
- **Incident Commander**: [Name]
- **Current Status**: [Investigating/Mitigating/Resolved]

**Progress Updates (every 30-60 minutes for Critical/High)**
- **Actions Taken**: [Steps completed]
- **Current Focus**: [What team is working on]
- **Expected Timeline**: [Estimated resolution or next update]

**Resolution Communication**
- **Resolution Summary**: [What was fixed]
- **Root Cause**: [Brief explanation]
- **Preventive Actions**: [Steps to prevent recurrence]
- **Post-Incident Review**: Scheduled for [Date/Time]

## Escalation Paths

### Standard Escalation Flow
**Level 1 - Team**: Developer/QA identifies issue → Discuss in standup → Team attempts resolution
**Level 2 - PM**: If unresolved after 24 hours → PM engages dependent teams and Product Manager
**Level 3 - Product Lead**: If blocking critical path or high impact → Product Lead coordinates cross-functional resolution
**Level 4 - Sponsor**: If business impact or requiring executive decision → Sponsor provides direction and resources

### Escalation Triggers
- **Immediate Escalation to Level 3**:
  - Production outage or critical bug affecting customers
  - Security vulnerability discovered in production
  - Major scope change request
  - Critical resource unavailable
- **Immediate Escalation to Level 4**:
  - Legal or compliance issues
  - Customer-facing crisis
  - Need for additional budget or significant resource changes

### Security Incident Escalation
- Follow the security incident runbook
- Notify Security on-call immediately via [primary contact method]
- Do not delay notification for investigation
- Security team will coordinate response and communications
- PM continues to track incident in risk register

### Escalation Communication Template
When escalating an issue:
- **Issue Description**: [Clear, concise description]
- **Impact**: [Who/what is affected and severity]
- **Actions Taken**: [What has been tried]
- **Requested Action**: [What decision or resource is needed]
- **Timeline**: [When decision is needed]
- **Escalated By**: [Name] on [Date/Time]
