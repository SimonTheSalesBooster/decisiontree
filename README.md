# The reason most projects fail has nothing to do with execution.

It's that nobody asked the hard questions before building started.

The founder says "build me X." The team builds X. Three weeks later, everyone discovers that X required seven decisions nobody made.. and four of them contradict each other.

This skill eliminates that failure mode. It interviews you relentlessly — walking every branch of the decision tree, resolving dependencies one by one — until shared understanding is complete. Only then does building begin.

---

## What happens when you run it

You describe what you want to build or figure out. Detailed or vague — both work.

Then the grilling starts.

Question after question. Each one walks a branch of the decision tree. Each one comes with a **recommended answer** — say "yes" to speed through the obvious ones, push back on the ones that matter. Dependencies surface. Contradictions get caught. Assumptions get named.

Sessions typically run ~45 minutes. You end with a fully-discovered set of requirements that would have taken weeks of back-and-forth to uncover any other way.

<img width="964" height="535" alt="image" src="https://github.com/user-attachments/assets/136a66b0-8e21-42ff-9065-467474bb06df" />


**This works for code AND for business decisions.** Course design, pricing strategy, partnership terms, product architecture — any plan with branching decisions benefits from the same process.

---

## Real example: designing a video publishing pipeline

**Input:** "I want to automatically publish videos from Google Drive to YouTube"

**What the grilling uncovered in 45 minutes:**

- Should it publish immediately or wait for approval? *(approval — Michelle reviews first)*
- What metadata does each video need? *(title, description, tags, chapters, thumbnail)*
- Where does the metadata come from? *(Notion database, auto-generated from transcript)*
- What happens when a video has no transcript? *(generate one with Whisper, don't skip)*
- Unlisted or public? *(unlisted first, Michelle switches to public after review)*
- What about the podcast audio file? *(extract separately, upload to different Drive folder)*
- How do we track which videos have been processed? *(Notion status field: Recording → Rough Cut Ready → Published)*

Seven decisions. Each one would have surfaced as a bug, a misunderstanding, or a "wait, I didn't mean that" — three weeks into building. Instead, they surfaced in 45 minutes before a single line was written.

---

## The format

```
YOU: I want to build [thing] / figure out [decision]

CLAUDE: Question 1 — [specific question about a branch point]
        Recommended answer: [what I'd suggest, based on context]

YOU: Yes / No / Actually, here's what I'm thinking...

CLAUDE: Question 2 — [next branch, informed by your answer]
        Recommended answer: [...]

... 20-40 questions later ...

CLAUDE: I think we've resolved all branches. Here's the full picture:
        [Complete, structured summary of every decision made]
```

---

## Two variants

### For code and technical projects

The AI explores your codebase to answer its own questions where possible — so it only asks you what it can't figure out itself.

```
/decisiontree I want to add a webhook that triggers when a new member joins
```

### For business decisions

Courses, strategies, offers, partnerships, pricing — any plan with branching decisions.

```
/decisiontree I'm designing a 5-day workshop for enterprise clients
```

---

## When to use it

- Before building anything that takes more than a day
- Before designing a course, offer, or pricing structure
- When you have a vision but haven't mapped the details
- When two people disagree about scope — run it together, let the questions settle it
- When you keep starting and restarting because "it's not quite right"

## When NOT to use it

- When the task is simple and clear (just build it)
- When you need to ship now and refine later (speed matters more than completeness)
- As a substitute for customer research (the questions are internal — they don't replace talking to buyers)

---

## Installation

### Claude Code

```bash
cp grill-me.md ~/.claude/commands/decisiontree.md
```

Then run:

```
/decisiontree [describe what you want to build or figure out]
```

### As a system prompt

Paste the contents of `grill-me.md` into any frontier model conversation. Then describe your plan.

---

## The philosophy

David Ogilvy spent weeks researching a product before writing a single headline. He read every manual, visited every factory, interviewed every engineer. By the time he sat down to write, the ad was already half-done — because he understood what he was selling.

Most people skip that step. They sit down to build before they understand what they're building. The decision tree forces Ogilvy's discipline onto any project: discover everything first, then execute with clarity.

The questions ARE the work. The building is just the easy part that comes after.

---

## About Strategy Sprints

[Strategy Sprints](https://www.strategysprints.com) helps B2B founders close bigger deals, faster, without hiring more people. 90-day sprints. One constraint at a time. Added over $2 Billion in sales to clients in finance, software, and consulting.

**What we offer:**

- **Sprint Club** — 251 founders across 72 countries. $49/month. AI-powered sales skills, community, weekly content.
- **200K Club** — Weekly group coaching. 5 founders per group. Pipeline, deals, pricing. $900/month.
- **Private Implementation** — 90-day sprints with your team. $9,000/month. Best result: 144x ROI.
- **AI Operations Sprint** — Build your AI infrastructure in 5 days. $15,000.
- **One-on-One Coaching** — $30,000 per client.
- **Workshop** — $80,000. Full-day intensive for your leadership team.

**Book a free Strategy Sprint call:** [strategysprints.com](https://www.strategysprints.com)

---

*keep rolling, Simon & The Sprinters*
