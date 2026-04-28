# OctoAcme — Roles RACI Matrix

## Purpose
Map common project lifecycle activities to roles using a RACI framework so responsibilities are unambiguous across the team.

> **RACI key:**
> - **R** = Responsible — does the work
> - **A** = Accountable — owns the outcome; approves/signs off
> - **C** = Consulted — provides input before action is taken
> - **I** = Informed — notified of decisions/outcomes

> **Role abbreviations used in this document:**
> - **PM** = Project Manager
> - **PdM** = Product Manager
> - **Dev** = Developer(s)
> - **SM** = Scrum Master / Delivery Lead
> - **UX** = UX Designer
> - **QA** = QA Lead / QA/Testing Lead
> - **SC** = Security Champion
> - **Ops** = Operations / DevOps Engineer

---

## RACI Matrix

| Lifecycle Activity | PM | PdM | Dev | SM | UX | QA | SC | Ops |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **Initiation** | | | | | | | | |
| Define problem statement & success metrics | C | A/R | I | I | C | I | I | I |
| Identify stakeholders & communication plan | A/R | C | I | C | I | I | I | I |
| Approve project go/no-go decision | A | R | I | I | I | I | C | C |
| **Planning** | | | | | | | | |
| Kickoff meeting facilitation | R | C | I | R | C | C | C | C |
| Backlog creation & prioritisation | C | A/R | C | R | C | C | C | I |
| Acceptance criteria definition | C | A | R | C | R | C | C | I |
| Test strategy & QA approach | C | C | C | C | I | A/R | C | C |
| Security threat modelling | C | C | C | I | I | C | A/R | C |
| Release plan & milestone map | A/R | C | C | C | I | C | I | C |
| **Execution** | | | | | | | | |
| Sprint/iteration facilitation | I | I | R | A/R | R | R | R | R |
| Feature implementation | I | C | A/R | I | C | C | C | I |
| UX design & prototyping | I | C | C | I | A/R | C | I | I |
| Code review & merge | I | I | A/R | I | I | C | C | I |
| Security review of PRs | I | I | C | I | I | I | A/R | I |
| Blocker escalation | A/R | C | C | R | I | C | C | C |
| **QA & Testing** | | | | | | | | |
| Test case creation & execution | I | C | C | I | C | A/R | C | I |
| Defect triage & prioritisation | C | C | R | C | I | A/R | C | I |
| Release-readiness sign-off | I | C | I | I | I | A/R | C | C |
| **Release & Deployment** | | | | | | | | |
| Deployment window scheduling | A/R | I | I | C | I | C | I | R |
| Staging deployment & smoke tests | C | I | C | I | I | R | C | A/R |
| Production deployment | C | I | C | I | I | C | C | A/R |
| Post-deploy verification | I | I | C | I | I | R | C | A/R |
| Release announcement | A/R | C | I | I | I | I | I | C |
| **Incident / Rollback** | | | | | | | | |
| Incident response triage | C | I | C | I | I | C | C | A/R |
| Rollback decision | A | I | C | I | I | C | C | R |
| Incident communication to stakeholders | A/R | C | I | I | I | I | C | C |
| Security incident escalation | C | I | C | I | I | I | A/R | C |
| Post-mortem facilitation | C | I | C | R | I | C | C | C |
| **Retrospective** | | | | | | | | |
| Retrospective facilitation | C | I | R | A/R | R | R | R | R |
| Action item ownership & tracking | A/R | C | R | R | R | R | R | R |
| Process improvement proposals | C | C | R | A/R | C | C | C | C |

---

## Notes
- An activity may have both an **A** and **R** assigned to the same person when they both own and perform the work.
- Where two or more roles share **R**, they collaborate; the **A** resolves tie-breaks.
- This matrix is a starting point — teams should adapt it to reflect actual headcount and structures.

## Related Documents
- [Roles and Personas](octoacme-roles-and-personas.md)
- [Cross-Functional Handoff Checklist](octoacme-cross-functional-handoff-checklist.md)
- [Project Initiation](octoacme-project-initiation.md)
- [Project Planning](octoacme-project-planning.md)
- [Execution and Tracking](octoacme-execution-and-tracking.md)
- [Release and Deployment](octoacme-release-and-deployment.md)
- [Retrospective and Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md)
