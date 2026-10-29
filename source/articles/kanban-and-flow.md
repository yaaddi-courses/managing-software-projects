# Kanban, work in progress and Scrumban

**Covers:** Kanban, Work in progress, WIP, Scrumban

## Managing flow instead of cycles {#overview}
Scrum organizes work into fixed-length cycles. Another family of methods treats work as a continuous flow, where tasks move from left to right across a board and new work starts only when there is room. This suits teams whose work arrives unpredictably, such as support or maintenance. In this article we will look at the board, the limit that makes it work, and the hybrid that combines it with Scrum.

## Kanban {#kanban}
Imagine a board with columns, and a card for every task. As work moves forward, the card moves from one column to the next. That is Kanban: tasks shown as cards moving through columns, with a limit on how many can be in progress at one time. The word is Japanese for "signboard". The method began in Toyota's factories in the 1940s and 1950s, and software teams adopted it in the 2000s.

A basic board has columns such as To do, Doing, Review and Done. Everyone can see at a glance where each piece of work is, where it is stuck and who is overloaded. Unlike Scrum, there are no fixed sprints. New work is pulled in whenever capacity opens up, and improvements are made continuously.

## Work in progress {#work-in-progress}
Work in progress means the tasks a team has started but not yet finished, as opposed to what is waiting or already done. Having a lot of it carries a hidden cost. Every started task ties up attention, switching between tasks wastes time, and each item takes longer to reach the finish.

A relationship called Little's Law makes this precise. On average, the time a task takes from start to finish equals the number of tasks in progress divided by the number finished per day. If throughput stays the same, doubling the tasks in progress doubles the waiting time for each.

## WIP {#wip}
WIP is the short form of work in progress. Teams talk about a "WIP limit", a fixed maximum for a column, such as at most three cards in Doing. When the column is full, nobody starts new work. Instead, they help finish something. The limit exposes bottlenecks: if Review is always full, the real problem is review capacity, not a lack of developers.

## Scrumban {#scrumban}
Some teams want a bit of both worlds. Scrumban is a hybrid that blends Scrum's structure, such as defined roles and regular planning, with Kanban's flow and limits. A team might keep a short planning meeting and a retrospective, but drop fixed sprints and use a board with WIP limits.

Teams often reach Scrumban when pure Scrum feels too rigid, for example when urgent bug reports keep arriving in the middle of a sprint, but pure Kanban feels too loose for planning and review.

## A worked example {#example}
A team of 4 finishes 3 tasks a day on average. Let's compare two ways of working.

| | No WIP limit | WIP limit of 6 |
|---|---|---|
| Tasks in progress | 24 | 6 |
| Throughput | 3 per day | 3 per day |
| Average time to finish one task | 24 / 3 = 8 days | 6 / 3 = 2 days |

Without a limit, each person works on six tasks at once (24 divided by 4). With the limit, there are 6 tasks for 4 people, and anyone who finishes a task helps another one before starting a new one. The time for one task to reach users falls from 8 days to 2, and the total work done per day stays the same.

Now look at the board. If the Review column holds 4 cards while its limit is 3, the team stops writing new code and reviews instead. The bottleneck is fixed within hours, not after a month of growing queues.

## A common mistake {#mistake}
A common slip is putting a Kanban board on the wall without limits. It becomes a task list, and the main benefit is lost. Setting the limit very high has the same effect.

A second slip is raising the limit whenever the column fills, instead of asking why work is stuck.

## Key points {#key-points}
- Kanban shows work on a board and limits how much is in progress.
- Time to finish a task equals work in progress divided by throughput.
- A WIP limit exposes bottlenecks and encourages finishing before starting.
- Scrumban mixes Scrum's structure with Kanban's flow.
