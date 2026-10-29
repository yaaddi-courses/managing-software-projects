# Tracking progress: charts, velocity and status reports

**Covers:** Burndown chart, Burnup chart, Velocity, Status report

## Seeing where you are {#overview}
A project manager needs to answer three questions at any time: how much is done, how much is left, and when will it be finished? Feelings are unreliable, so teams use a few plain tools. Two charts show progress over time, one number shows how fast the team really works, and a short report turns all of it into something busy people can read.

## Burndown chart {#burndown-chart}
A burndown chart shows how much work remains over time. The vertical axis is the remaining work, in story points or tasks, and the horizontal axis is time, such as the days of a sprint. A line drawn from the starting amount down to zero at the end date shows the ideal pace. The real line shows what is actually left each day.

If the real line sits above the ideal, the team is behind. If it falls steeply, the team is ahead. The chart is easy to understand, but it has a blind spot. If new work is added, the line goes up or flat, and it is hard to tell whether the team slowed down or the scope grew.

## Burnup chart {#burnup-chart}
A burnup chart fixes that blind spot. It shows how much work has been completed over time, together with a second line for the total scope. The completed line goes up toward the scope line. When scope is added, the scope line jumps, and everyone can see that the goal moved.

That makes it better for projects where scope changes. It answers both "how much have we done" and "how much is there to do", and it shows when the team got faster and when the target got bigger.

## Velocity {#velocity}
Velocity is how much work a team typically completes in one sprint, usually measured in story points. You use it to forecast: if the team normally finishes about 20 points a sprint and 100 points remain, the work will take about five sprints.

Use the average of the last three to five sprints, since a single sprint is noisy. Velocity belongs to one team. Its size depends on how that team estimates, so comparing the velocities of two teams is meaningless and encourages inflated estimates.

## Status report {#status-report}
A status report is a short update, usually for executives or sponsors, that leads with the headline, such as the main risk or a decision needed, and gives the details after it. Busy readers should know the state of the project in ten seconds.

A common format is a traffic-light summary (green, amber, red) with three or four lines: what was done, what is next, the top risks and what help is needed. Put bad news first, with a proposed fix.

## A worked example {#example}
A team has 100 points of work and completed 21, 18, 24 and 20 points in its last four sprints. This program forecasts the end.

```python
import math

done = [21, 18, 24, 20]
velocity = sum(done) / len(done)
remaining = 100

print(velocity)
print(math.ceil(remaining / velocity))
# 20.75
# 5
```

The four sprints add up to 83 points, and 83 divided by 4 gives an average velocity of 20.75 points. At that rate, 100 points need 100 divided by 20.75, which is about 4.8, so the team rounds up to 5 sprints.

Now let's see what the two charts show for a 10-day plan of 100 points, where 10 points of new scope arrive on day 6.

| Day | Ideal remaining | Actual remaining | Total scope | Completed |
|---|---|---|---|---|
| 0 | 100 | 100 | 100 | 0 |
| 5 | 50 | 60 | 100 | 40 |
| 8 | 20 | 46 | 110 | 64 |

On day 8 the burndown line sits at 46 against an ideal of 20, a gap of 26 points. That looks like a very late team. The burnup chart splits the gap into its two causes. The team completed 64 points against 80 planned, so it is 16 points behind. The other 10 points are scope that was added, and 16 plus 10 is the 26 on the burndown. Without the scope line, the team would be blamed for the whole gap.

The status report for the sponsor would start: "Amber. 64 of 110 points are complete (58 percent). Scope grew by 10 points on day 6. Decision needed: drop the export feature or move the date by one day."

## A common mistake {#mistake}
A common slip is using velocity to compare or pressure teams. People respond by inflating estimates, and the number becomes useless.

A second slip is reporting only good news. Executives who hear about a problem late lose trust in the team.

## Key points {#key-points}
- A burndown chart shows remaining work. A burnup chart shows work done and the scope target.
- Use a burnup chart when scope changes.
- Velocity is a team's own average output per sprint, for forecasting only.
- A status report leads with the headline, bad news included.
