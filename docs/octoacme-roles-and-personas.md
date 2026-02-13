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
- Hand off completed work to QA with clear testing instructions
- Support production incidents within their area of expertise

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed
- Handoff documentation for QA team

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
- Orchestrate handoffs between development, QA, and release phases
- Manage escalations and ensure appropriate decision-making authority

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## QA Engineers / Testers

### Role Summary
QA Engineers validate that deliverables meet acceptance criteria, quality standards, and user expectations. They work closely with developers and product managers to ensure high-quality releases.

### Responsibilities
- Review and validate acceptance criteria before testing begins
- Perform functional, regression, and exploratory testing
- Document and track defects with clear reproduction steps
- Verify bug fixes and sign off on feature completeness
- Participate in release readiness reviews
- Maintain test documentation and test data
- Provide feedback on testability during planning and design

### Goals
- Ensure software meets quality standards before release
- Catch defects early in the development cycle
- Maintain comprehensive test coverage
- Reduce production incidents through thorough validation

### Typical Communication
- Daily standups with development team
- Bug reports and test status updates
- Sign-off documentation for completed features
- Release readiness feedback

---

## Cross-Functional Handoffs

### Development → QA Handoff
- **Developer Responsibility**: Complete PR merge, update ticket with test instructions, demo feature functionality
- **QA Responsibility**: Review acceptance criteria, confirm test environment readiness, begin testing within 1 business day
- **Artifacts**: Test instructions, feature documentation, deployed environment details

### QA → Release Manager Handoff
- **QA Responsibility**: Complete test sign-off, document known issues, verify rollback procedures tested
- **Release Manager Responsibility**: Review deployment checklist, schedule release window, prepare monitoring
- **Artifacts**: Test results summary, release notes, deployment runbook

### Release Manager → Support Handoff
- **Release Manager Responsibility**: Communicate release details, provide support documentation, brief on known issues
- **Support Responsibility**: Acknowledge receipt, prepare for potential user questions, monitor feedback channels
- **Artifacts**: Release announcement, support runbook, escalation contacts

---

## Escalation Authority Matrix

### Decision Authority Levels

**Level 1 - Team Level (Developer, QA)**
- Technical implementation decisions within defined scope
- Bug priority assignment (Low/Medium)
- Test approach and coverage decisions
- Code review approval

**Level 2 - Lead Level (PM, Product Manager)**
- Scope change approval (minor adjustments)
- High-priority bug decisions
- Sprint goal adjustments
- Cross-team dependency resolution
- Release timing decisions (non-critical)

**Level 3 - Director Level (Product Lead, Engineering Director)**
- Major scope changes or feature cuts
- Critical bug vs. release timeline trade-offs
- Resource reallocation across teams
- Go/No-Go decisions for major releases
- Security incident response authorization

**Level 4 - Executive Level (Sponsor, VP)**
- Project cancellation or major pivots
- Budget increases or significant resource changes
- Strategic roadmap adjustments
- Customer-impacting incident communications
- Legal or compliance escalations

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

