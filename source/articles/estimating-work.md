# Breaking down and estimating work

**Covers:** Work breakdown structure, WBS, Story points, Planning poker

## Why estimates go wrong {#overview}
Have you ever guessed how long a task would take, and been wrong by a lot? Almost everyone has. People are consistently over-optimistic, and the bigger the task, the bigger the error. Two habits help. First, cut the work into pieces small enough to judge. Second, estimate as a group, using a method that reduces bias. In this article we will look at a way to split work and two ways to size it.

## Work breakdown structure {#work-breakdown-structure}
The first habit is splitting. A work breakdown structure divides a large project into smaller and smaller pieces of work, until each piece is small enough to estimate and assign to one person or small group. You can draw it as a tree: the project at the top, major parts on the next level and tasks at the bottom.

A useful check is the 100 percent rule. The pieces under any item must add up to the whole of that item, with nothing missing and nothing extra. Missing pieces are a leading cause of late projects. A good bottom-level task takes between about half a day and two weeks.

## WBS {#wbs}
WBS is the common abbreviation for work breakdown structure. You will see it on plans and in tools, for example "see the WBS for the full list of tasks". The structure is also the base for later planning, such as scheduling and assigning people.

## Story points {#story-points}
Once the work is split, how do you size each piece? Many teams give each task a number called a story point, which describes its size relative to other tasks. Unlike a time estimate, it does not claim to know hours or days. It combines how much work there is, how complex it is and how uncertain it is.

Teams often use a scale that grows quickly, like 1, 2, 3, 5, 8, 13. Bigger items are less certain, so the widening gaps avoid false precision. A 5 is roughly more than a 3 and less than an 8. The unit is meaningful only within one team, which compares everything to a few known reference tasks.

Points help because people are better at comparing than predicting. It is easier to say "this is about twice as hard as the login page" than "this will take 11.5 hours".

## Planning poker {#planning-poker}
In planning poker, the team estimates together. The steps are:

1. The Product Owner explains the task and answers questions.
2. Each person privately chooses a card with a story point value.
3. Everyone reveals their card at the same time.
4. If the numbers differ widely, the highest and the lowest explain their reasoning.
5. The team discusses and votes again until the estimates are close.

Revealing together prevents anchoring, where the first number said aloud pulls everyone toward it. The discussion is the real value, because a big disagreement often shows that someone knows about a hidden risk.

## A worked example {#example}
A team plans a "user profile" feature. Let's start with the breakdown.

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

Now the team sizes one task.

**Planning poker on "Photo upload: store and resize":**

| Person | First vote |
|---|---|
| Ana | 3 |
| Ben | 3 |
| Chen | 13 |
| Dee | 5 |

Chen's 13 is far from the others. Chen explains that large photos on mobile networks need retries and a background queue. The others had not thought of that. After the discussion, the second round gives 8, 8, 8, 8, and the team records 8 points.

The disagreement was valuable. It revealed a risk worth 5 extra points before any code was written (the first votes of Ana and Ben were 3, and the team ended at 8).

## A common mistake {#mistake}
A common slip is turning points into hours ("one point is one day"). Then they behave like poor time estimates, and managers compare teams by points.

A second slip is skipping the discussion and averaging the votes, which throws away the most useful part.

## Key points {#key-points}
- A work breakdown structure splits the project until each piece can be estimated, and the pieces must add up to the whole.
- Story points express relative size, not hours.
- Planning poker uses simultaneous voting to avoid anchoring.
- Big differences in votes reveal hidden risks, so discuss them.
