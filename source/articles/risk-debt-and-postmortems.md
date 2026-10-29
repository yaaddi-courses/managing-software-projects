# Risk, technical debt and postmortems

**Covers:** Risk management, Mitigation, Technical debt, Postmortem

## Looking ahead and looking back {#overview}
Good project managers spend time on two things that feel less urgent than shipping: thinking about what could go wrong before it does, and learning honestly from what did. Between them sits a risk that many teams underrate, which is the shortcut taken today that must be paid for later. Let's take these in order.

## Risk management {#risk-management}
Waiting until a problem has happened narrows your options. Risk management means spotting potential problems early and acting on them before they happen. A risk is something that might happen. An issue is something that has already happened.

A plain process has four steps:
1. **Identify:** list what could go wrong. Ask the team, since they know the weak spots.
2. **Assess:** rate the probability and the impact, for example from 1 to 5 each, and multiply for a score.
3. **Respond:** choose an action for the highest scores.
4. **Review:** keep checking, because risks change.

A written list, called a risk register, with an owner for each item, is enough for most projects.

## Mitigation {#mitigation}
Spotting a risk is not enough. Mitigation is taking action to reduce or handle a risk once you have spotted it, instead of noting it and hoping. The usual options are:
- **Avoid:** change the plan so the risk disappears.
- **Mitigate:** lower the probability or the impact.
- **Transfer:** pass the risk to someone else, such as through insurance or a supplier contract.
- **Accept:** decide to live with it, and have a fallback if it happens.

A good mitigation is specific, has an owner and a date. "Be careful with the new library" is not a mitigation. "Build a two-day prototype with the library by Friday" is.

## Technical debt {#technical-debt}
Shortcuts in code feel free at the time. Technical debt is the name for their cost: the extra effort that will be needed later to clean them up. Ward Cunningham used the money metaphor in 1992. A shortcut is like a loan. You get speed now and pay interest later, every time the messy code slows someone down, and the debt may grow.

Not all debt is bad. Taking a shortcut to meet a real deadline, with a plan to repay it, can be a good choice. The danger is debt that nobody tracks. It is a risk for the whole project plan, not only a complaint from engineers, since it slows every future feature.

Make it visible. List the shortcuts, give each an estimated cost to fix and an estimated cost of living with it, and set aside a fixed share of each sprint to repay the most expensive items.

## Postmortem {#postmortem}
After a project or a serious problem ends, a good team looks back honestly at what really happened, including the failures, so that the next one goes better. That review is a postmortem. The best ones are blameless: they ask how the process allowed a mistake, not who made it. People who fear blame hide problems.

A good format covers what happened and when, what went well, what went wrong, why it went wrong and what specific actions will change the outcome, each with an owner and a date.

## A worked example {#example}
A team plans a launch in 6 weeks. Let's follow the steps.

| Step | Detail |
|---|---|
| Risk identified | The payment provider's test system is unreliable |
| Assessment | Probability 4, impact 5, score 20 (the highest on the register) |
| Mitigation | Build a switch to a second provider; owner Ana; due week 3. This is a "mitigate" response |
| Technical debt | To save a week, the team hardcodes tax rates. Cost to fix later: about 3 days. Recorded on the debt list and scheduled for the first sprint after launch |
| Outcome | The launch is on time. The provider fails in week 5, but the switch works |
| Postmortem | Held a week after launch. Action: add a second-provider check to every future payment project |

The numbers show why the debt list matters. Three days of cleanup was the cost of saving 5 working days (a week). That was a fair trade, but only because it was written down and scheduled. If it had been forgotten, the hardcoded rates would have surprised everyone in the next tax change.

## A common mistake {#mistake}
A common slip is keeping a risk list that nobody reads or updates. A list made at the start and never reviewed gives false comfort.

A second slip is skipping the postmortem when the project went well. Successful projects teach as much as failed ones.

## Key points {#key-points}
- Risk management identifies, rates and responds to risks before they happen.
- Mitigation reduces a risk with a specific action, an owner and a date.
- Technical debt is a trackable loan: make it visible and repay it on schedule.
- A blameless postmortem turns experience into actions.
