# The critical path, buffers and slack

**Covers:** Critical path, Buffer, Slack

## What really decides the end date {#overview}
A project schedule is a set of tasks, and some of them must wait for others. So you might ask: is the end date the sum of all the work? It is not. It is set by the longest chain of tasks that depend on each other. Knowing which chain that is tells you where delay hurts and where it does not. And since estimates are never perfect, you also need a plan for the surprises.

## Critical path {#critical-path}
The critical path is the longest chain of dependent tasks in a project. Each task on the chain waits for the one before it, so the length of the chain is the shortest possible duration of the whole project. If any task on it slips by a day, the whole project ends a day later, unless you make up the time elsewhere.

Tasks off the critical path have room to move. A delay in them does not change the end date until it uses up that room. That is why a project manager watches critical tasks most closely, and also looks for ways to shorten the path, for example by running two tasks in parallel or adding people to the longest one.

A project can have more than one critical path. And the critical path can change: if a task off the path slips far enough, it becomes critical.

## Slack {#slack}
Slack is the spare time that lets a task or a chain of tasks run late without delaying the end date. A task on the critical path has zero slack. A task off the path may have several days.

People also use the word loosely for any spare room in a plan, such as a team member's free time, and in everyday project talk they often use slack and buffer as if they meant the same. Formally, slack is the room that exists because of the shape of the plan, and buffer is room added deliberately.

## Buffer {#buffer}
Estimates are never exactly right, so planners add extra time on purpose to absorb surprises. That extra time is a buffer. If a task is likely to take 2 weeks, you may plan 2.5.

Where you put buffers matters. Padding every task invites people to use it all, since work expands to fill the time. A common better approach is to keep estimates honest, then add one shared buffer at the end of the critical chain, which the whole project draws on. The method is known as critical chain management and comes from Eliyahu Goldratt. Watch how quickly the buffer is consumed, because it is an early warning.

## A worked example {#example}
A small release has four tasks. Task A takes 3 days. B (2 days) and C (4 days) can start after A. Task D (1 day) needs both B and C. This program finds the earliest finish for each task.

```python
tasks = {
    "A": (3, []),
    "B": (2, ["A"]),
    "C": (4, ["A"]),
    "D": (1, ["B", "C"]),
}

finish = {}
for name, (days, needs) in tasks.items():
    start = max((finish[n] for n in needs), default=0)
    finish[name] = start + days

print(finish)
print(max(finish.values()))
# {'A': 3, 'B': 5, 'C': 7, 'D': 8}
# 8
```

Let's read the result:

1. A finishes on day 3. B and C start together on day 3.
2. B finishes on day 5 and C on day 7.
3. D must wait for both, so it starts on day 7 and finishes on day 8.
4. The critical path is A, then C, then D: 3 + 4 + 1 = 8 days.
5. B finishes on day 5, but D cannot start until day 7, so B has 2 days of slack.

If C slips by two days, the release moves from day 8 to day 10. If B slips by two days, nothing changes. Adding a shared buffer of one day at the end gives a plan of 9 days, and the team commits to day 9.

## A common mistake {#mistake}
A common slip is giving every task its own safety padding and then having people use it. The delay accumulates anyway, while the buffer disappears.

A second slip is not recomputing the critical path as the project changes. The tasks that matter most this month may not be the ones that mattered at the start.

## Key points {#key-points}
- The critical path is the longest chain of dependent tasks, and it sets the minimum project length.
- Slack is spare time off the critical path. Critical tasks have none.
- A buffer is extra time added on purpose, best held as one shared reserve.
- Recompute the critical path when the plan changes.
