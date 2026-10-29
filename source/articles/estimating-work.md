# Breaking down and estimating work

**Covers:** Work breakdown structure, WBS, Story points, Planning poker

## Why estimates go wrong {#overview}
People are consistently over-optimistic about how long tasks take, and the bigger the task, the bigger the error. Two habits help: cut the work into pieces small enough to judge, and estimate as a group using a method that reduces bias. This article covers a way to split work and two ways to size it.

## Work breakdown structure {#work-breakdown-structure}
A work breakdown structure splits a large project into smaller and smaller pieces of work until each piece is small enough to estimate and assign to one person or small group. It is drawn as a tree: the project at the top, major parts on the next level and tasks at the bottom.

A useful rule is the 100 percent rule: the pieces under any item must add up to the whole of that item, with nothing missing and nothing extra. Missing pieces are a leading cause of late projects. A good bottom-level task takes between about half a day and two weeks.

## WBS {#wbs}
WBS is the common abbreviation for work breakdown structure. You will see it on plans and in tools, for example "see the WBS for the full list of tasks". The structure is also the base for later planning, such as scheduling and assigning people.

## Story points {#story-points}
A story point is a number a team gives to a task to describe its relative size compared with other tasks. Unlike a time estimate, it does not claim to know hours or days. It combines how much work, how complex and how uncertain the task is.

Teams often use a scale that grows quickly, like 1, 2, 3, 5, 8, 13, because bigger items are less certain, so false precision is avoided. A 5 is roughly more than a 3 and less than an 8. The unit is only meaningful within one team, which compares everything to a few known reference tasks.

Points help because people are better at comparing than predicting. It is easier to say "this is about twice as hard as the login page" than "this will take 11.5 hours".

## Planning poker {#planning-poker}
Planning poker is a technique in which the team estimates together. The steps are:

1. The Product Owner explains the task and answers questions.
2. Each person privately chooses a card with a story point value.
3. Everyone reveals their card at the same time.
4. If the numbers differ widely, the highest and the lowest explain their reasoning.
5. The team discusses and votes again until the estimates are close.

Revealing together prevents anchoring, where the first number said aloud pulls everyone toward it. The discussion is the real value, because a big disagreement often shows that someone knows about a hidden risk.

## A worked example {#example}
A team plans a "user profile" feature.

**Work breakdown structure:**

| Level | Item |
|---|---|
| 1 | User profile |
| 2 | Profile page |
| 3 | Show name and photo |
| 3 | Edit details |
| 2 | Photo upload |
| 3 | Choose and crop an image |
| 3 | Store and resize |
| 2 | Privacy settings |

**Planning poker on "Photo upload: store and resize":**

| Person | First vote |
|---|---|
| Ana | 3 |
| Ben | 3 |
| Chen | 13 |
| Dee | 5 |

Chen's 13 is far from the others. Chen explains that large photos on mobile networks need retries and a background queue. The others had not thought of that. After the discussion, the second round gives 8, 8, 8, 8, and the team records 8 points.

The disagreement was valuable: it revealed a risk worth 5 extra points before any code was written.

## A common mistake {#mistake}
Turning points into hours ("one point is one day"). Then they behave like poor time estimates, and managers compare teams by points. Another mistake is skipping the discussion and averaging the votes, which throws away the most useful part.

## Key points {#key-points}
- A work breakdown structure splits the project until each piece can be estimated, and the pieces must add up to the whole.
- Story points express relative size, not hours.
- Planning poker uses simultaneous voting to avoid anchoring.
- Big differences in votes reveal hidden risks, so discuss them.
