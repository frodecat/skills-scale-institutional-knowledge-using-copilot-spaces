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

## Scrum Master (Delivery Lead)

### Role Summary
The Scrum Master (or Delivery Lead) facilitates agile ceremonies, removes impediments, and coaches the team on agile practices. They work closely with the Project Manager (PM) to maintain delivery cadence and team health.

> **Abbreviation note:** SM = Scrum Master / Delivery Lead.

### Responsibilities
- Facilitate daily standups, sprint planning, sprint reviews, and retrospectives
- Identify and actively remove blockers that slow the team
- Coach the team on agile principles and continuous improvement
- Shield the team from unplanned interruptions during a sprint
- Track sprint progress and flag scope creep or capacity concerns to the PM

### Goals
- Maximise team throughput and predictability
- Foster psychological safety and a culture of continuous improvement
- Keep ceremonies productive and timeboxed

### Typical Communication
- Daily standup facilitation and impediment log
- Sprint planning and review meeting facilitation
- Async updates to PM on blockers and capacity changes

### Interaction Points
- **PM:** Closely aligned on delivery cadence, risk escalation, and resource constraints
- **PdM (Product Manager):** Collaborates on backlog readiness and acceptance-criteria clarity before sprint planning
- **Developers:** Day-to-day coaching, blocker removal, and adherence to Definition of Done
- **QA/Testing Lead:** Ensures QA capacity and test readiness are factored into sprint planning
- **Stakeholders:** Facilitates sprint demos and communicates velocity/progress

---

## UX Designer

### Role Summary
UX Designers own the user experience end-to-end: they research user needs, create wireframes/prototypes, and validate designs before and during development. They are the bridge between user value and technical implementation.

### Responsibilities
- Conduct user research and synthesise insights into design briefs
- Create wireframes, prototypes, and user-flow diagrams
- Define and communicate UX acceptance criteria alongside PdM
- Collaborate with Developers during implementation to ensure fidelity to design
- Run usability testing and iterate based on findings

### Goals
- Deliver intuitive, accessible, and consistent user experiences
- Reduce re-work by resolving UX ambiguity before development starts
- Validate assumptions with real users early and often

### Typical Communication
- Design briefs and annotated mockups shared before sprint planning
- Design-review sessions with Developers and PdM
- Usability testing reports shared with PdM and PM

### Interaction Points
- **PM:** Aligns on timeline for design deliverables and any scope impact
- **PdM (Product Manager):** Jointly defines user needs, acceptance criteria, and success metrics
- **Developers:** Hands off designs before a story enters "In Progress"; reviews implementation for UX fidelity
- **QA/Testing Lead:** Shares UX acceptance criteria to include in test cases
- **Stakeholders:** Presents prototypes and usability findings for early feedback

---

## QA Lead (QA/Testing Lead)

### Role Summary
The QA Lead (also referred to as QA/Testing Lead) defines and oversees the test strategy, coordinates test planning and execution, and acts as the quality gate before any release. They work across the team to ensure acceptance criteria are testable and met.

> **Abbreviation note:** QA = Quality Assurance.

### Responsibilities
- Define and maintain the overall test strategy (unit, integration, end-to-end, exploratory)
- Review acceptance criteria for testability during planning
- Coordinate test case creation and test-cycle execution
- Manage defect triage and ensure critical bugs are resolved before release
- Report test coverage, defect trends, and release readiness to PM and PdM

### Goals
- Prevent regressions and ensure high-quality releases
- Make quality a shared responsibility across the team
- Provide clear, timely release-readiness signals

### Typical Communication
- Test plans and coverage reports shared with PM and PdM
- Defect reports and triage notes in the issue tracker
- Release-readiness sign-off before each deployment

### Interaction Points
- **PM:** Reports on test coverage and release readiness; escalates blocking defects
- **PdM (Product Manager):** Reviews acceptance criteria to ensure they are verifiable
- **Developers:** Collaborates on testability, shares failing test cases, coordinates bug-fix priorities
- **UX Designer:** Incorporates UX acceptance criteria into test cases
- **Stakeholders:** Communicates known issues and risk posture before release

---

## Security Champion

### Role Summary
The Security Champion advocates for secure engineering practices within the team. They are a developer or engineer with additional security training who acts as the team's first line of security review, threat modelling, and policy compliance.

### Responsibilities
- Review features and design decisions for security risks during planning
- Lead threat-modelling sessions for significant changes
- Ensure security scanning is configured and results are actioned in CI
- Track and communicate security-relevant vulnerabilities or compliance requirements
- Serve as liaison to the central security team or CISO function

### Goals
- Prevent security vulnerabilities from reaching production
- Build security awareness across the team
- Reduce time-to-remediate for identified vulnerabilities

### Typical Communication
- Security review notes attached to feature specs or PRs
- Threat model documents for significant changes
- Escalation to PM and sponsor for high-severity findings

### Interaction Points
- **PM:** Notifies of security risks that may impact timelines or require sponsor escalation (see *Escalation Paths* in [Risks and Communication](octoacme-risks-and-communication.md))
- **PdM (Product Manager):** Flags security trade-offs in scope or design decisions
- **Developers:** Reviews PRs for security concerns; coaches on secure coding practices
- **QA/Testing Lead:** Aligns on security testing (SAST, DAST, penetration testing) as part of the test strategy
- **Stakeholders:** Reports compliance posture and security incident status

---

## Operations / DevOps Engineer

### Role Summary
Operations/DevOps Engineers own the deployment pipelines, infrastructure reliability, and operational readiness of delivered software. They enable smooth handoffs from development to production and lead incident response.

> **Abbreviation note:** DevOps = Development + Operations.

### Responsibilities
- Design, build, and maintain CI/CD pipelines and infrastructure-as-code
- Define and enforce deployment runbooks and rollback procedures
- Monitor production health (availability, latency, error rates) and on-call rotation
- Lead or support incident response: triage, mitigation, and post-mortems
- Collaborate with Developers to ensure services are designed for operability

### Goals
- Achieve high deployment frequency with low change-failure rate
- Minimise mean time to recovery (MTTR) for production incidents
- Eliminate manual, error-prone deployment steps

### Typical Communication
- Deployment runbooks and environment-readiness confirmations
- Incident notifications and post-mortem reports
- Pipeline status and on-call rotation updates shared with PM

### Interaction Points
- **PM:** Confirms deployment windows; escalates operational blockers or incidents
- **PdM (Product Manager):** Provides input on operational constraints affecting feature timelines
- **Developers:** Reviews services for operability, logging, and observability requirements; supports staging deployments
- **QA/Testing Lead:** Supports staging environment setup for test cycles; coordinates smoke-test execution post-deploy
- **Security Champion:** Collaborates on infrastructure security, secrets management, and vulnerability patching

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- For a visual overview of cross-role responsibilities, see [Roles RACI Matrix](octoacme-roles-raci-matrix.md).
- For handoff checklists between roles, see [Cross-Functional Handoff Checklist](octoacme-cross-functional-handoff-checklist.md).

