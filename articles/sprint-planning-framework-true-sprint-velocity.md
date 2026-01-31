# True Sprint Velocity: Making Sprint Planning Predictable and Data‑Driven

Most teams I’ve worked with were not *inefficient*. They were *exhausted*.

Not because they couldn’t deliver—but because sprint after sprint, expectations were set using numbers that **looked scientific but behaved like guesswork**. Velocity was calculated, commitments were made, and then reality quietly broke the plan.

This article is not about Scrum theory. It’s about a **practical, numbers‑driven framework** I designed and applied as a *part‑time Scrum Master and full‑time engineer* at Mentor Graphics to make sprint planning predictable, defensible, and humane.

If you struggle with missed sprint goals, constant carry‑over, or burnout disguised as “under‑performance”, this framework is for you.

## Context: Scrum Without a Dedicated Scrum Army

At Mentor Graphics, there was no separate Scrum‑Master organization.

Senior management trained engineering teams for two days on Scrum and asked each team to **self‑select a Scrum Master**, rotating the role periodically. I was chosen for my team and served in this role for about six months—**while continuing my regular development work**.

This mattered.

Because I was still shipping code, I experienced Scrum from the inside—not as a process custodian, but as someone directly impacted by planning mistakes.

## The Core Problem

Our sprint velocity calculation was simple:

```
Completed story points = Sprint velocity
```

On paper, this is standard Scrum.

In practice, it failed us.

Why?

Because **no two sprints ever run under identical conditions**.

Engineers take leave. Some split time across teams. Production issues appear. Support load fluctuates.

Yet velocity numbers were compared as if all sprints were executed with everyone at 100% availability.

This is not a Mentor Graphics problem. It is a near‑universal reality in modern engineering teams.

When velocity ignores availability:

* Planning becomes optimistic fiction
* Missed goals feel personal
* Burnout becomes structural

The real issue wasn’t output. It was **missing context**.

So I reframed the question.

Instead of:

> How many story points did we deliver?

I asked:

> **How much did we deliver per unit of availability?**

That single shift unlocked everything.

## The Insight: Normalize Velocity by Availability

Velocity only becomes meaningful when it is normalized against input.

In our case, input was **availability**.

```
True Sprint Velocity = Completed Story Points / Team Availability
```

Availability is treated as a *person‑equivalent unit*:

* 100% availability → 1.0
* 50% availability → 0.5

Availability is **additive across the team**, just like person‑days or person‑hours.

Once normalized, velocity becomes comparable across sprints—even when conditions change.

## The Framework (Minimal, Mechanical, Repeatable)

### Step 1: Capture Availability During Sprint Planning

Availability is recorded *up front*, before commitments are made.

| Engineer        | Available Working Days | Availability (fraction) |
| --------------- | ---------------------- | ----------------------- |
| Asad            | 14                     | 0.93                    |
| Adil            | 15                     | 1.00                    |
| Amjad           | 14                     | 0.93                    |
| Usman           | 13                     | 0.87                    |
| Naeem           | 14                     | 0.93                    |
| Noor            | 15                     | 1.00                    |
| Talha           | 11                     | 0.73                    |
| **Team Total**  | **96 days**            | **6.39**                |

This makes constraints explicit before planning begins.

### Step 2: Plan Sprint Capacity (Before the Sprint Starts)

Using each engineer’s historical *average* True Sprint Velocity:

| Engineer        | Avg True Velocity | Planned Availability | Planned Capacity (SP) |
| --------------- | ----------------- | -------------------- | --------------------- |
| Asad            | 7.0               | 0.93                 | 6.5                   |
| Adil            | 8.0               | 1.00                 | 8.0                   |
| Amjad           | 8.5               | 0.93                 | 7.9                   |
| Usman           | 13.5              | 0.87                 | 11.7                  |
| Naeem           | 5.0               | 0.93                 | 4.7                   |
| Noor            | 3.3               | 1.00                 | 3.3                   |
| Talha           | 7.1               | 0.73                 | 5.2                   |
| **Team**        |                   |                      | **47.3 SP**           |

This number—not hope—became the sprint commitment.

### Step 3: Track Planned vs Actual Work

We tracked **product work** and **support work** separately.

| Category     | Planned SP | Completed SP |
| ------------ | ---------- | ------------ |
| Product Work | 42.5       | 46.0         |
| Support Work | 9.0        | 11.0         |
| **Total**    | **51.5**   | **57.0**     |

This made scope drift and unplanned work visible *without blame*.

### Step 4: Compute True Sprint Velocity (After the Sprint)

| Engineer        | Completed SP | Availability | True Sprint Velocity |
| --------------- | ------------ | ------------ | -------------------- |
| Asad            | 6.0          | 0.93         | 6.4                  |
| Adil            | 6.0          | 1.00         | 6.0                  |
| Amjad           | 11.0         | 0.93         | 11.8                 |
| Usman           | 16.5         | 0.87         | 19.0                 |
| Naeem           | 7.0          | 0.93         | 7.5                  |
| Noor            | 4.0          | 1.00         | 4.0                  |
| Talha           | 6.5          | 0.73         | 8.9                  |
| **Team**        | **57.0**     | **6.39**     | **8.9**              |

This team TSV fed into a rolling average used for the *next* sprint.

## What Changed (Without Drama)

* Sprint commitments became defensible
* Planning meetings became shorter
* Missed goals became explainable
* Burnout signals became visible early

Most importantly:

> The data showed the team was already efficient.

The problem had never been productivity. It was **planning under false assumptions**.

## Why This Works

This framework does not motivate people harder.

It fixes the math.

By normalizing output against availability:

* Effort debates disappear
* Constraints replace excuses
* Planning conversations calm down

Instead of defending people, the numbers defend reality.

## Final Thought

This was never really about Scrum.

It was about a pattern I’ve followed throughout my career:

When a system behaves unpredictably, I look for **hidden variables**, make them explicit, normalize the data, and let the system explain itself.

True Sprint Velocity is just one instance of that instinct.

Different problem. Same approach.

Make reality visible.
Then design around it.
