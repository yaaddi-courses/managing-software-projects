# Projects, products, programs and the iron triangle

**Covers:** Project manager, Program, Product, Iron triangle

## What are you actually managing? {#overview}
Before you can manage software work, you need to know what kind of work it is and what pulls against it. Some work has an end date and some does not. Some work is a single effort and some is a group of efforts. And every effort faces the same tension between what you build, how fast and how much it costs. In this article we will name these ideas, together with the role of the person who keeps them in balance.

## Project manager {#project-manager}
Every project needs someone who keeps it moving. The project manager is the person responsible for planning a project, running it and delivering it. In practice that means keeping the scope, the schedule, the budget, the risks and the people all pointing in the same direction, so that the team ships instead of drifting.

It is a job of coordination more than control. A project manager clears obstacles, keeps people informed, negotiates trade-offs with those who pay and makes problems visible early. They usually do not write the code or decide how it is built. On small teams one person may do the job alongside other work, and on large projects it may be a full-time role.

## Program {#program}
A program is a group of related projects that are managed together, because coordinating them delivers more value than running each one alone. Imagine a company moving to a new payment system. One project builds the new checkout, another migrates old customer data and a third trains support staff. Each has its own manager, but one program manager makes sure that they finish in the right order and that the whole change lands smoothly.

## Product {#product}
A product is something that keeps being built, improved and supported over time, such as an app or an online service. Unlike a project, a product has no planned end date. It lives as long as it creates value.

The difference changes how you manage it. A project is judged by whether it finished on time and on budget. A product is judged by whether customers use it and value it. A single product may spawn many projects, such as a new search feature or a redesign.

## Iron triangle {#iron-triangle}
Every project pulls three ways at once. The iron triangle, also called the project management triangle, says that a project's scope, time and cost are linked. If you change one, at least one other must change too.

- Add features (more scope), and it will take longer or cost more.
- Cut the deadline (less time), and you must reduce the scope or add people, which raises the cost.
- Reduce the budget, and you must accept less scope or more time.

Many people add quality as the middle of the triangle. If you squeeze all three corners, quality is what silently drops. The practical lesson is to ask which corner is fixed, which is flexible and which one may be sacrificed, and to decide this early with the people paying for the work.

## A worked example {#example}
A team has 4 developers for 10 weeks to build an online booking feature. The plan is 4 x 10 = 40 person-weeks of work. A manager now asks for a payment option, which adds 8 person-weeks. Let's look at the options.

| Option | Scope | Time | Cost | Effect |
|---|---|---|---|---|
| Keep the team and the date | Add payments | 10 weeks | Same | Not possible: needs 48 person-weeks, but only 40 exist |
| Move the date | Add payments | 12 weeks | Same | 4 developers x 12 weeks = 48, so it fits |
| Add people | Add payments | 10 weeks | Higher | Need 4.8 developers, so hire 1 more (not fully efficient) |
| Cut other scope | Add payments, drop reports | 10 weeks | Same | Remove 8 person-weeks of other work |

The arithmetic: 40 person-weeks plus 8 is 48, and 48 divided by 4 developers is 12 weeks. For the third row, 48 divided by 10 weeks is 4.8 developers. The table makes the choice visible: something has to give. The project manager's job is to lay out these options and let the decision-makers choose.

## A common mistake {#mistake}
A common slip is promising to hold all three corners. "More features, by the same date, with the same team" is not a plan.

A second slip is treating a product like a project and declaring it finished at launch. A product needs ongoing work after release.

## Key points {#key-points}
- A project manager keeps scope, time, cost, risk and people aligned so the team can ship.
- A program coordinates related projects. A product continues indefinitely and spawns many projects.
- The iron triangle shows that scope, time and cost trade off against each other.
- Decide early which corner may flex.
