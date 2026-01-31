# True Sprint Velocity: Making Sprint Planning Predictable and Data-Driven

Most teams I have worked with were not *inefficient*. They were *exhausted*. Not because they couldn’t deliver—but because sprint after sprint, expectations were set using numbers that **looked scientific but behaved like guesswork**. Velocity was calculated, commitments were made, and then reality quietly broke the plan.

This article is not about Scrum theory. It’s about a **practical, numbers-driven framework** I designed and applied as a *part‑time Scrum Master and full‑time engineer* at Mentor Graphics to make sprint planning predictable, defensible, and humane.

If you struggle with missed sprint goals, constant carry‑over, or burnout masked as “under‑performance”, this framework is for you.

## Context: Scrum Without a Dedicated Scrum Army

At Mentor Graphics, there was no separate scrum masters organization.

Senior management trained engineering teams for two days on Scrum and asked each team to **self‑select a scrum master**, rotating the role periodically. I was chosen for my team and served in this role for about six months—**while continuing my regular development work**.

This constraint turned out to be a strength. Because I was still shipping code, I experienced scrum *from the inside*—not as a process enforcer, but as someone directly impacted by planning mistakes.

## The Problem: Velocity Without Context Is Just a Number

Our previous sprint velocity calculation was simple:

> *Completed story points = Sprint Velocity*

On paper, this is standard Scrum.
In reality, it was deeply misleading.

Why?

Because **no two sprints were comparable**.

- Engineers took planned and unplanned leaves
- Some team members were allocated 50% to other teams
- Production issues and support load varied wildly

Yet velocity numbers were compared as if all sprints were executed under identical conditions.

In classic scrum training, velocity is described as a simple sum of story points delivered in a sprint. It’s treated as a stable metric for forecasting. But in practice—in almost every company—circumstances are *never* uniform. Team members are pulled in different directions, availability shifts, and yet planning continues as if everyone is at 100%, all the time.

This is not a Mentor Graphics problem.

In practice, **uniform sprint circumstances almost never exist**—in large companies, small startups, product teams, platform teams, and everything in between. People take leave, context switches happen, priorities shift, and shared ownership is a reality.

This leads to two destructive outcomes:
1. **Unrealistic Sprint Commitments:** Teams over-commit, then miss goals, eroding trust with management.
2. **Chronic Burnout:** Engineers push to meet inflated plans, leading to stress and turnover.

Our team was trapped in this cycle. I realized that to break it, we needed to measure not just *output*, but *output relative to input*.

If velocity can’t be trusted, then:
- Sprint planning becomes fiction
- Missed goals feel personal
- Burnout becomes inevitable

So I treated this as an engineering problem.

Instead of asking:

> *How many story points did we deliver?*

I asked:

> **How productive were we *per unit of availability*?**

That single shift unlocked everything that follows.

## The Solution: Introducing "True Sprint Velocity"

The insight was simple: **Velocity should be normalized for availability.** If a team completes 40 story points but was only 80% available, their true performance isn’t 40—it’s 50 points per full capacity.

I defined **True Sprint Velocity (TSV)** as:

\[
\text{True Sprint Velocity} = \frac{\text{Completed Story Points}}{\text{Team Availability}}
\]

Where *Availability* is the net percentage of the team’s time dedicated to sprint work (after accounting for time off, meetings, support, and other commitments).

This became our normalized benchmark. For planning the next sprint, we reversed the formula:

\[
\text{Forecasted Capacity} = \text{True Sprint Velocity (avg)} \times \text{Upcoming Sprint Availability}
\]

This shifted our planning from guesswork to data-driven forecasting.

Because no sprint is identical, the framework explicitly adjusts for each team member’s availability, making planning resilient to the inherent variability of real-world work.

## The Framework: A Step-by-Step System for Realistic Planning

Here’s the exact system I implemented, which you can replicate using a simple Excel sheet.

### 1. Track Individual Availability Per Sprint
During sprint planning, document each member’s availability as a percentage. This includes planned leave, dedicated days to other projects, and known commitments.

| Engineer | Sprint Availability | Notes (Leave, Other Projects) |
|----------|---------------------|--------------------------------|
| Alex     | 80%                 | 1 day leave, 1 day ops support|
| Sam      | 100%                | Fully dedicated                |
| Jamie    | 50%                 | 50% allocation to Team B       |
| Taylor   | 90%                 | 0.5 day training               |
| **Team Total** | **80%**        | **Aggregated**                 |

### 2. Calculate True Sprint Velocity (Historical)
After each sprint, calculate TSV for the team and for each engineer (for personal performance insights).

| Engineer | Completed SP | Availability | **True Sprint Velocity** |
|----------|--------------|--------------|---------------------------|
| Alex     | 12           | 80%          | 15.0                      |
| Sam      | 14           | 100%         | 14.0                      |
| Jamie    | 8            | 50%          | 16.0                      |
| Taylor   | 10           | 90%          | 11.1                      |
| **Team** | **44**       | **80%**      | **55.0**                  |

*Team TSV = 44 / 0.80 = 55.0*

### 3. Maintain a Rolling Average
Use the average of the last 3 sprints’ TSV for forecasting. This smooths out anomalies.

| Sprint | Team TSV | 3-Sprint Avg TSV |
|--------|----------|-------------------|
| Sprint 3 | 52.0     | -                 |
| Sprint 4 | 55.0     | -                 |
| Sprint 5 | 58.0     | **55.0**          |

### 4. Forecast Next Sprint Capacity
Multiply the 3-sprint average TSV by the next sprint’s planned availability.

\[
\text{Forecasted Capacity} = 55.0 \times 0.85 \text{ (next sprint availability)} = 46.75 \text{ story points}
\]

This becomes your realistic sprint commitment.

## Step 5: Capacity‑Driven Sprint Planning

Now planning became mechanical—and accurate.

```
Planned Capacity = Average True Velocity × Planned Availability
```

### Planning Example

| Engineer | Planned Availability | Avg True Velocity | Capacity |
|--------|---------------------|------------------|----------|
| Alex  | 100% | 21 | 21 |
| Sam    | 50% | 18 | 9 |
| Jamie  | 80% | 22 | 17.6 |
| Taylor  | 70% | 20 | 14 |
| **Team Total** | ** 75% ** |  | **61.6 SP** |

Sprint commitments were now **defensible, repeatable, and calm**.

### 6. Visualize for Management
Managers love clear, actionable data. Present this in a dashboard-style table:

| Metric | This Sprint | Trend | Impact |
|--------|-------------|--------|---------|
| Team Availability | 85% | ↑ 5% | More capacity |
| Avg True Velocity | 55.0 | ↑ 2% | Improved efficiency |
| Forecasted Capacity | 46.75 SP | Reliable forecast | Realistic goals set |
| Sprint Goal Achievement | 100% | Consistent | Trust with stakeholders |

## What Changed (And Why Management Cared)

- Sprint goals were consistently met
- Planning meetings became shorter
- Engineers stopped feeling blamed for math errors
- Management saw *predictability*, not excuses

Most importantly:

> The data proved the team was efficient.

The problem had never been productivity. It was **planning under false assumptions**.

## Why This Works: The Human Element of Agile

What surprised me most was not the math — it was the *reaction*.

Managers often assume missed sprint goals indicate inefficiency. Engineers assume management expectations are unrealistic. Both sides feel justified, and neither side has hard evidence.

This framework quietly dissolves that tension by normalizing velocity against availability, the numbers start answering questions *before they are asked*:

- When velocity drops, the data shows whether productivity changed — or availability did.
- When expectations rise, capacity calculations show exactly what assumptions must also change.
- When teams deliver consistently, the evidence is visible without heroic explanations.

Instead of debating effort, the conversation shifts to constraints. Instead of defending people, the data defends reality. 

This is why the framework scales across teams and survives management scrutiny: it does not ask for trust — it shows its work.

This framework does more than improve numbers — it aligns planning with reality. It acknowledges that your engineers are humans, not machines with constant throughput. By making variability visible, it:

- **Prevents Burnout:** Stops the cycle of overcommitment.
- **Builds Trust with Management:** Data replaces debate. You can demonstrate why a goal was missed (e.g., “availability was 60% due to company-wide initiatives”) and show improving forecasting accuracy.
- **Empowers the Team:** Engineers feel their time is respected, and their performance is measured fairly.

In our case, within three sprints, our sprint goal achievement rate jumped to nearly 100%. Management could see the correlation between availability and delivery, and they began setting expectations based on data, not hope.

## A Call to Realistic Agility

Scrum’s power lies in its adaptability, not in rigid adherence to textbook definitions. The “uniform sprint” is a myth in the dynamic environment of modern tech companies. By adopting a **True Sprint Velocity** framework, you stop planning in a vacuum and start planning in the real world.

Try this framework in your next sprint. Track availability, calculate True Sprint Velocity, and plan using realistic capacity. You’ll be surprised at how planning becomes calmer, data-driven, and human-friendly.

## Final Thought

Over time, I realized this was not really about scrum. It was about a pattern I’ve followed throughout my career.

When a system behaves unpredictably, I don’t look for motivation fixes or process theater. I look for **hidden variables**, make them explicit, normalize the data, and then let the system explain itself.

That’s what this framework does.

As a tech lead or architect, my differentiator has never been blind optimism or heroic delivery. It has been the ability to:

- Turn vague pain into measurable signals
- Replace intuition-based planning with explainable math
- Protect teams from burnout by fixing the system, not pushing the people
- Give management numbers they can trust *without inflating expectations*

True Sprint Velocity is just one example of that approach.

Different problem. Same instinct. Make reality visible. Then design around it.