# Incident Response Template & Playbook

## Purpose
This template provides a structured approach to managing production incidents, ensuring quick resolution, clear communication, and thorough post-incident analysis.

---

## Incident Severity Definitions

### Critical (P0)
- **Impact**: Complete service outage or major functionality broken for all users
- **Response Time**: Immediate (24/7)
- **Update Frequency**: Every 15-30 minutes
- **Escalation**: Immediately to Product Lead and on-call
- **Examples**: API down, database failure, security breach, data loss

### High (P1)
- **Impact**: Significant degradation affecting many users or critical workflows
- **Response Time**: Within 1 hour during business hours
- **Update Frequency**: Every 30-60 minutes
- **Escalation**: To PM and Product Manager within 1 hour
- **Examples**: Key feature broken, severe performance degradation, payment processing issues

### Medium (P2)
- **Impact**: Moderate issues affecting some users or non-critical features
- **Response Time**: Within 4 hours during business hours
- **Update Frequency**: Daily until resolved
- **Escalation**: To PM if not resolved within 8 hours
- **Examples**: Minor feature bugs, cosmetic issues affecting UX, non-critical integrations down

### Low (P3)
- **Impact**: Minor issues with minimal user impact
- **Response Time**: Within 1 business day
- **Update Frequency**: As needed
- **Escalation**: Standard bug triage process
- **Examples**: Typos, minor UI inconsistencies, documentation errors

---

## Incident Response Workflow

### Phase 1: Detection & Triage (0-15 minutes)
**Actions:**
1. ✅ Acknowledge the incident (alert, ticket, report)
2. ✅ Assign Incident Commander (on-call engineer or first responder)
3. ✅ Determine severity using definitions above
4. ✅ Create incident channel/room (e.g., #incident-[ID])
5. ✅ Send initial notification (see Communication Templates below)
6. ✅ Begin incident log (timeline of actions)

**Roles:**
- **Incident Commander**: Coordinates response, makes decisions, owns communication
- **First Responders**: Engineers investigating and implementing fixes
- **Communication Lead**: Updates stakeholders (PM or designated person)

### Phase 2: Investigation (15 minutes - 2 hours)
**Actions:**
1. ✅ Gather symptoms and user reports
2. ✅ Review recent changes (deployments, config changes, PRs merged)
3. ✅ Check monitoring dashboards, logs, and error tracking
4. ✅ Identify affected systems and scope of impact
5. ✅ Form initial hypothesis about root cause
6. ✅ Send progress updates per severity schedule
7. ✅ Escalate if needed (see Escalation section)

**Investigation Checklist:**
- [ ] Recent deployments reviewed (last 24-48 hours)
- [ ] Error logs analyzed for patterns
- [ ] Database performance and queries checked
- [ ] External dependencies status verified (APIs, services)
- [ ] Resource utilization reviewed (CPU, memory, disk)
- [ ] User reports summarized for common patterns

### Phase 3: Mitigation (2 hours - resolution)
**Actions:**
1. ✅ Implement immediate mitigation (rollback, hotfix, feature flag)
2. ✅ Test mitigation in staging if possible
3. ✅ Deploy mitigation to production
4. ✅ Verify issue is resolved (smoke tests, user reports)
5. ✅ Monitor for 30-60 minutes post-mitigation
6. ✅ Send resolution communication
7. ✅ Document temporary workarounds if needed

**Mitigation Options:**
- **Rollback**: Revert to last known-good version (fastest, preferred for P0)
- **Hotfix**: Quick code fix deployed immediately
- **Feature Flag**: Disable problematic feature
- **Config Change**: Adjust settings or environment variables
- **Scale Resources**: Add capacity if resource-related
- **Traffic Routing**: Redirect to backup systems

### Phase 4: Resolution & Verification
**Actions:**
1. ✅ Confirm all systems operational
2. ✅ Verify user functionality restored
3. ✅ Review monitoring for anomalies
4. ✅ Document incident timeline and actions taken
5. ✅ Schedule post-incident review (within 48 hours)
6. ✅ Close incident channel/ticket
7. ✅ Send final resolution communication

---

## Communication Templates

### Initial Incident Notification
**Subject**: [P0/P1/P2] Incident Notification - [Brief Description]

**Message:**
```
🚨 INCIDENT DETECTED

Severity: [P0/P1/P2/P3]
Incident ID: [INC-YYYY-MM-DD-###]
Incident Commander: [Name]

Summary: [1-2 sentence description of the issue]

Impact:
- Affected Users: [All / Subset / Internal only]
- Affected Systems: [List key systems/features]
- Started: [Timestamp]

Current Status: [Investigating / Mitigating / Monitoring]

Response Team: [Names of engineers responding]

Next Update: [Expected time]

Incident Channel: [#incident-XXX or link]
```

### Progress Update Template
```
📊 INCIDENT UPDATE - [Incident ID]

Time: [Timestamp]

Actions Completed:
- [Action 1]
- [Action 2]

Current Focus:
- [What we're working on now]

Findings So Far:
- [Key discoveries]

Expected Next Steps:
- [Action 1] - ETA [time]
- [Action 2] - ETA [time]

Next Update: [Time]
```

### Resolution Notification Template
```
✅ INCIDENT RESOLVED - [Incident ID]

Resolution Time: [Timestamp]
Duration: [Total time from detection to resolution]

Summary: [Brief description of what happened]

Root Cause: [Brief explanation]

Resolution Actions Taken:
- [Action 1]
- [Action 2]

Impact Summary:
- Users Affected: [Estimated number or percentage]
- Duration of Impact: [Time period]
- Data Loss: [None / Description if applicable]

Preventive Actions:
- [Action item 1] - Owner: [Name], Due: [Date]
- [Action item 2] - Owner: [Name], Due: [Date]

Post-Incident Review: Scheduled for [Date/Time]

Thank you to the response team: [Names]
```

---

## Escalation Guidelines

### When to Escalate

**Immediate Escalation Required:**
- All P0 incidents → Product Lead and on-call immediately
- Any security or data breach → Security team immediately
- Cannot identify root cause within 1 hour (P0) or 4 hours (P1)
- Mitigation attempts failing repeatedly
- External communication to customers needed
- Legal or compliance implications
- Need additional resources or expertise

**Escalation Path:**
1. **First Responder** → **Incident Commander** (if different)
2. **Incident Commander** → **PM** and **Product Manager**
3. **PM/Product Manager** → **Product Lead** / **Engineering Director**
4. **Leadership** → **Sponsor** / **Executive Team** (for business impact)

**External Escalation:**
- **Security Team**: For any security-related incidents
- **Legal**: For data breaches, compliance issues, or customer contract impacts
- **PR/Communications**: For public-facing communications or media inquiries
- **Vendor Support**: For third-party service issues

---

## Post-Incident Review Process

### Scheduling
- Schedule within 24-48 hours of resolution while details are fresh
- Duration: 60-90 minutes
- Required attendees: Incident Commander, key responders, PM, relevant stakeholders
- Optional: Representatives from affected teams

### Review Structure

**1. Timeline Review (15 minutes)**
- Walk through the incident timeline from detection to resolution
- Note key decision points and actions taken
- Identify any gaps in the timeline

**2. Root Cause Analysis (20 minutes)**
- Use "5 Whys" or similar technique
- Distinguish between immediate cause and underlying systemic issues
- Avoid blame - focus on systems and processes

**3. What Went Well (10 minutes)**
- What worked effectively in the response?
- What processes or tools helped?
- Which communications were effective?

**4. What Could Be Improved (20 minutes)**
- What slowed down the response?
- What information was missing or hard to find?
- What processes or tools need improvement?
- Were there early warning signs we missed?

**5. Action Items (15 minutes)**
- Preventive actions to avoid recurrence
- Process improvements for faster detection/response
- Documentation or tooling needs
- Assign owners and due dates
- Define success criteria for each action

**6. Close Out (5 minutes)**
- Schedule follow-up to review action item progress
- Document the review and share with stakeholders
- Thank the team for their response

### Post-Incident Review Template
```markdown
# Post-Incident Review - [Incident ID]

**Date**: [Date]
**Attendees**: [Names]
**Incident**: [Brief description]
**Severity**: [P0/P1/P2/P3]
**Duration**: [Total duration]

## Timeline
[Detailed timeline of events from detection through resolution]

## Root Cause
[Explanation of the root cause using 5 Whys or similar analysis]

## Impact
- Users affected: [Number/percentage]
- Systems affected: [List]
- Revenue impact: [If applicable]
- Data impact: [None / Description]

## What Went Well
1. [Item 1]
2. [Item 2]
3. [Item 3]

## What Could Be Improved
1. [Item 1]
2. [Item 2]
3. [Item 3]

## Action Items
| Action | Owner | Due Date | Success Criteria | Status |
|--------|-------|----------|------------------|--------|
| [Action 1] | [Name] | [Date] | [Criteria] | Not Started |
| [Action 2] | [Name] | [Date] | [Criteria] | Not Started |

## Lessons Learned
[Key takeaways for the team and organization]

## Follow-up Review
Scheduled for: [Date] to review action item progress
```

---

## Incident Response Checklist

### Pre-Incident Preparation
- [ ] On-call rotation established and documented
- [ ] Incident response contacts list maintained
- [ ] Monitoring and alerting configured
- [ ] Rollback procedures documented and tested
- [ ] Incident communication channels set up
- [ ] Team trained on incident response procedures

### During Incident
- [ ] Incident detected and acknowledged
- [ ] Incident Commander assigned
- [ ] Severity determined
- [ ] Incident channel/room created
- [ ] Initial notification sent
- [ ] Incident log started
- [ ] Investigation underway
- [ ] Progress updates sent per schedule
- [ ] Escalation done if needed
- [ ] Mitigation deployed
- [ ] Resolution verified
- [ ] Monitoring continued post-mitigation

### Post-Incident
- [ ] Final resolution communication sent
- [ ] Incident timeline documented
- [ ] Post-incident review scheduled
- [ ] Root cause analysis completed
- [ ] Action items identified and assigned
- [ ] Lessons learned shared with team
- [ ] Processes and documentation updated
- [ ] Follow-up review scheduled

---

## Best Practices

1. **Communicate Early and Often**: Over-communication is better than under-communication during incidents
2. **Focus on Mitigation First**: Resolve the incident, then investigate root cause
3. **Blameless Culture**: Focus on systems, not individuals
4. **Document Everything**: Maintain detailed incident logs for later analysis
5. **Test Rollback Procedures**: Regularly verify that rollback processes work
6. **Learn and Improve**: Every incident is an opportunity to improve systems and processes
7. **Prepare for Incidents**: Assume incidents will happen and prepare accordingly

---

## Additional Resources

- [OctoAcme Roles and Personas](octoacme-roles-and-personas.md) - Escalation authority matrix
- [OctoAcme Risks and Communication](octoacme-risks-and-communication.md) - Communication templates
- [OctoAcme Retrospective and Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md) - Action item tracking

---

*Last Updated: 2026-02-13*
*Review and update this template quarterly or after major incidents*
