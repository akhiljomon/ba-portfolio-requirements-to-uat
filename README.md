# Business Analysis Portfolio: From Requirements to UAT

A complete, end-to-end business analysis case study for a **fictional** café chain,
*BrewLine Cafés*, introducing **click-and-collect ordering** through its existing loyalty app.

It shows how I take a business problem through the full analysis lifecycle: scope,
stakeholders, requirements, user stories with acceptance criteria, as-is and to-be process
maps, data requirements, a UAT test plan with executed test cases, a defect log, and a
requirements traceability matrix that ties it all together.

> **Note:** BrewLine Cafés, its people, figures and systems are invented for this case study.
> Any resemblance to a real business is coincidental.

## Artefacts

| # | Artefact | What it shows |
|---|----------|---------------|
| 1 | [Problem statement and scope](01-problem-statement-and-scope.md) | Business problem, objectives, success measures, in/out of scope, assumptions and constraints |
| 2 | [Stakeholder analysis](02-stakeholder-analysis.md) | Stakeholder register, influence/interest grid, engagement plan, elicitation approach |
| 3 | [Business requirements](03-business-requirements.md) | Business, functional and non-functional requirements with IDs and MoSCoW priority |
| 4 | [User stories and acceptance criteria](04-user-stories.md) | INVEST user stories with Given/When/Then acceptance criteria |
| 5 | [Process maps](05-process-maps.md) | As-is and to-be process flows (Mermaid diagrams that render on GitHub) and the gap analysis |
| 6 | [Data requirements](06-data-requirements.md) | Entities, data dictionary, business rules, reporting needs |
| 7 | [UAT test plan](07-uat-test-plan.md) | UAT approach, entry/exit criteria, roles, schedule, results summary |
| 8 | [UAT test cases](uat-test-cases.csv) | Executed test cases with expected vs actual results |
| 9 | [Defect log](defect-log.csv) | Defects raised in UAT with severity, steps to reproduce and status |
| 10 | [Traceability matrix](08-traceability-matrix.md) | Every requirement traced to user stories, test cases and defects |

## How to read it

Start with the problem statement, then follow any requirement ID (for example `FR-03`) through
the user stories, test cases and defect log using the traceability matrix.

## About me

I'm Akhil Jomon, a UTS graduate (Master of Engineering Management and Master of Engineering,
Systems Software) moving into business and systems analysis. At Tata Elxsi I worked from client
requirements to define test scenarios, documented defects with clear steps to reproduce, and
supported client acceptance testing. This portfolio applies that requirements-to-test discipline
to the full BA lifecycle.

[LinkedIn](https://www.linkedin.com/in/akhil-j-964865254)

## How this was built

Drafted with the help of **Claude Code** (Anthropic's AI coding assistant), then reviewed and
edited by me.
