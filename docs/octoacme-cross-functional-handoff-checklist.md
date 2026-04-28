# OctoAcme — Cross-Functional Handoff Checklist

## Purpose
Provide lightweight, reusable checklists for the most common cross-role handoff points so that context, quality signals, and accountability are never lost between phases.

> **Role abbreviations:** PM = Project Manager · PdM = Product Manager · UX = UX Designer · Dev = Developer · QA = QA Lead · SC = Security Champion · Ops = Operations/DevOps Engineer · SM = Scrum Master/Delivery Lead

---

## 1. Design → Development Handoff

**Trigger:** A design-ready story is about to enter the sprint "In Progress" column.  
**Owner:** UX Designer hands off to the Developer(s) assigned to the story.

### Checklist
- [ ] Annotated wireframes or prototypes shared in the story/PR (link added to issue)
- [ ] UX acceptance criteria documented and agreed with PdM
- [ ] Accessibility requirements noted (colour contrast, keyboard navigation, ARIA labels where applicable)
- [ ] Design assets (icons, images, tokens) exported and accessible to Developers
- [ ] Edge cases and error states included in designs
- [ ] Developer has reviewed design and raised any feasibility concerns
- [ ] QA informed of UX acceptance criteria so test cases can be prepared

---

## 2. Development → QA Handoff

**Trigger:** A story/feature is code-complete and merged; ready for formal QA validation.  
**Owner:** Developer notifies QA Lead when the build is deployed to the QA/staging environment.

### Checklist
- [ ] All acceptance criteria implemented (link to relevant PRs in the issue)
- [ ] CI pipeline is green (tests, lint, security scan)
- [ ] Build deployed to QA/staging environment and smoke-tested by Developer
- [ ] Known limitations or deferred items documented in the issue
- [ ] Test data or environment prerequisites communicated to QA
- [ ] UX acceptance criteria included alongside functional acceptance criteria
- [ ] Security Champion notified if the change touches auth, data handling, or infrastructure

---

## 3. Release Readiness Check

**Trigger:** End of a sprint/cycle; team is preparing to ship to production.  
**Owner:** PM coordinates; QA Lead and Ops Engineer confirm readiness.

### Checklist
- [ ] **Quality gate:** QA Lead has signed off release readiness (all critical/high defects resolved or risk-accepted by PdM)
- [ ] **Security gate:** Security Champion confirms no unmitigated high/critical vulnerabilities
- [ ] **CI/CD:** Pipeline is green on the release branch (tests, lint, security scan)
- [ ] **Release notes:** Drafted and reviewed by PM and PdM (use [Release Notes Template](octoacme-release-and-deployment.md))
- [ ] **Rollback plan:** Documented and reviewed by Ops Engineer
- [ ] **Deployment window:** Scheduled and communicated to stakeholders by PM
- [ ] **Smoke test suite:** Prepared by QA; Ops confirms staging results
- [ ] **Stakeholder sign-off:** PdM and relevant stakeholders have approved scope shipped
- [ ] **Support / comms:** Support team briefed; release announcement drafted

---

## 4. Post-Release Verification

**Trigger:** Production deployment complete.  
**Owner:** Ops Engineer leads verification; PM confirms stakeholder communication.

### Checklist
- [ ] Post-deploy smoke tests run and passing (Ops + QA)
- [ ] Key success metrics baseline captured (error rate, latency, usage — see Project One-pager)
- [ ] Monitoring dashboards and alerts confirmed active
- [ ] Release announcement sent to stakeholders by PM
- [ ] Any post-deploy defects logged in the issue tracker with severity and owner
- [ ] On-call rotation notified and monitoring scheduled for first 24–48 hours
- [ ] Rollback window communicated to team (how long before rollback is off the table)

---

## 5. Incident / Rollback Handoff

**Trigger:** A production incident is declared or a rollback decision is made.  
**Owner:** Ops Engineer leads response; PM owns stakeholder communication.

### Checklist — Incident Declaration
- [ ] Incident severity assessed (use Escalation Paths in [Risks and Communication](octoacme-risks-and-communication.md))
- [ ] On-call Ops Engineer and PM notified
- [ ] Incident channel / bridge opened
- [ ] Security Champion looped in if incident has a security dimension

### Checklist — Rollback Decision
- [ ] Rollback decision made by PM (with input from Ops and PdM)
- [ ] Rollback steps executed by Ops Engineer per documented runbook
- [ ] Stakeholders notified of rollback by PM
- [ ] Root cause investigation initiated; post-mortem scheduled

---

## Related Documents
- [Roles and Personas](octoacme-roles-and-personas.md)
- [Roles RACI Matrix](octoacme-roles-raci-matrix.md)
- [Project Planning](octoacme-project-planning.md)
- [Execution and Tracking](octoacme-execution-and-tracking.md)
- [Release and Deployment](octoacme-release-and-deployment.md)
- [Risks and Communication](octoacme-risks-and-communication.md)
- [Retrospective and Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md)
