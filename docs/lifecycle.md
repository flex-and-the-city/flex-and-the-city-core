\# Lifecycle \& Workflow: Flex and the City



\## 1. Project Methodology

This project follows a \*\*Phase-Gate Model\*\* divided into four quarters. Each quarter must meet its "Gate Criteria" before moving to the next phase to ensure architectural integrity and prevent technical debt.



\### Quarter Schedule (2026)

\* \*\*Q1: Pre-Work \& Strategy:\*\* Ideation, Architecture, and Risk Assessment.

\* \*\*Q2: Setup \& Standards:\*\* Project infrastructure, Backlog creation, and Linting.

\* \*\*Q3: Development:\*\* Sprint-based execution of the MVP.

\* \*\*Q4: Testing \& Iteration:\*\* QA, Refinement, and Final Polish.



---



\## 2. Git \& Branching Strategy

To simulate a professional environment, we will use a \*\*Feature Branch Workflow\*\*.



\* \*\*`main` Branch:\*\* Contains stable, production-ready code. No direct commits allowed.

\* \*\*`dev` Branch:\*\* (Starting Q3) The integration branch for features.

\* \*\*Feature Branches:\*\* Created from `dev` using the naming convention:

&nbsp;   \* `feat/feature-name` (New functionality)

&nbsp;   \* `fix/bug-name` (Bug fixes)

&nbsp;   \* `docs/doc-update` (Documentation changes)

&nbsp;   \* `refactor/improvement` (Code cleanup)



\### Commit Message Standard

We follow \[Conventional Commits](https://www.conventionalcommits.org/):

\* `feat: add unit conversion logic`

\* `fix: resolve crash on workout save`

\* `docs: update lifecycle strategy`



---



\## 3. Definition of Done (DoD)

A task/ticket is only considered "Done" when it meets the following criteria:



\### For Documentation (Q1-Q2):

\- \[ ] Content is reviewed for clarity.

\- \[ ] Markdown is correctly formatted.

\- \[ ] Linked to the main README roadmap.



\### For Development (Q3-Q4):

\- \[ ] Code follows established naming conventions.

\- \[ ] Feature functions as described in the User Story.

\- \[ ] No linting errors.

\- \[ ] (Q4) Unit tests pass.



---



\## 4. Quality Gates

Before moving to the next quarter, the following "Gates" must be passed:



| From | To | Requirement |

| :--- | :--- | :--- |

| \*\*Q1\*\* | \*\*Q2\*\* | Tech stack finalized and Architecture approved. |

| \*\*Q2\*\* | \*\*Q3\*\* | Backlog populated with at least 5 prioritized User Stories. |

| \*\*Q3\*\* | \*\*Q4\*\* | All "Must-Have" features functional in a local environment. |



---



\## 5. Change Management

If a new "uncontemplated" feature is identified during development:

1\.  Document the idea in the \*\*Backlog\*\*.

2\.  Assess if it fits the \*\*Vision\*\*.

3\.  Queue it for \*\*Q4 Improvements\*\* to avoid Q3 scope creep.

