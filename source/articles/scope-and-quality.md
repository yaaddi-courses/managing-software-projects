# Protecting scope and quality

**Covers:** Scope creep, Change request, Backlog grooming, Definition of done, DoD, Quality gate

## Two things that quietly erode {#overview}
Projects rarely fail in one dramatic step. They erode. The list of things to build grows a little at a time, and the standard for calling something finished slips a little at a time. Both are easy to miss day to day and very expensive in total. In this article we will look at the tools that hold the line on what is being built and on how well it is done.

## Scope creep {#scope-creep}
"Could you also add a filter?" "While you are there, can you fix that page?" Each request looks harmless. Together they push the date and the budget, with no one having decided to accept the cost. That growth of a project beyond what was originally agreed, in small, easy-to-miss pieces, is scope creep.

The remedy is not to refuse everything. It is to make additions visible and to decide them on purpose.

## Change request {#change-request}
When someone asks to change the scope after work has started, you make the ask formal. That is a change request. Instead of quietly absorbing the new work, you write it down, estimate its effect on time, cost and risk, and let the person with authority decide: accept it and move the date, accept it and drop something else, or leave it for later.

The process need not be heavy. A form with five fields and a short review each week is enough for most teams. What matters is that nothing changes without a decision. Skipping this step is exactly how scope creep happens.

## Backlog grooming {#backlog-grooming}
Backlog grooming, also called refinement, is the regular review of the backlog to keep it ready for planning. The team and the Product Owner reorder items, split large ones, add detail to vague ones and delete those that no longer matter. A groomed backlog means the top items are small, clear and understood, so planning is quick.

An un-groomed backlog grows into a graveyard of hundreds of old ideas, and new work gets chosen by noise instead of value. Many teams spend about an hour a week on it.

## Definition of done {#definition-of-done}
What does "done" mean? Without an agreement, it means different things to different people. A definition of done is an explicit checklist, agreed by the whole team, that a piece of work must satisfy before it counts as finished. A typical list: code reviewed, automated tests pass, documentation updated, deployed to a test environment and accepted by the Product Owner.

Without one, unfinished work, such as untested code, accumulates under the label "done". It then shows up later as bugs and rework.

## DoD {#dod}
DoD is the standard abbreviation for the definition of done. You will see it on team boards and wiki pages. A team can have a DoD for a single item and another, stricter one for a release.

## Quality gate {#quality-gate}
A quality gate is a checkpoint that work must pass before it can move to the next stage, such as passing all automated tests before merging, or passing a security scan before release. Gates are often automated in the build pipeline: if the check fails, the work stops.

A gate should be objective (a number or a pass/fail), fast enough to run every time, and trusted. A gate that people routinely bypass is worse than none, because it hides the real state of the work.

## A worked example {#example}
A team is in the middle of a sprint when four things happen. Let's see how each tool answers.

| Event | Tool | Decision |
|---|---|---|
| A stakeholder asks for CSV export "while you are at it" | Change request | Estimate: 3 days. Sprint has no room. Product Owner puts it at the top of the next sprint |
| The backlog has 140 items; the top 5 are vague | Backlog grooming | A 1-hour session splits 2 items and clarifies 3. Now planning can start |
| A developer says "the report is done" but it has no tests | Definition of done | The DoD requires tests and a review, so the item stays in progress |
| The build shows 78 percent test coverage; the gate requires 80 | Quality gate | The merge is blocked until two missing tests are added |

Without the change request, the 3 days would have come from nowhere. Without the DoD, the report would be counted as finished, and its bugs would appear a month later. Each tool takes minutes and prevents days of rework.

## A common mistake {#mistake}
A common slip is using change requests to say no to everything, which makes people go around the process. Aim for a quick yes, a quick no or a clear "later".

A second slip is a definition of done that is too long to follow. Five to eight checks that everyone really does beat twenty that nobody reads.

## Key points {#key-points}
- Scope creep is growth through small additions that nobody decided on.
- A change request makes each addition visible and forces a decision.
- Backlog grooming keeps the next work small and clear.
- A definition of done and quality gates prevent unfinished work from passing as complete.
