# Decision Tree — AI Interviews You Relentlessly Before You Build Anything

**The reason most projects fail has nothing to do with execution.** It is that nobody asked the hard questions before building started. This Claude Code skill walks every branch of the decision tree, resolves dependencies, and produces a complete set of requirements in ~45 minutes — before a single line of code or copy is written.

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/works_with-Claude_Code-orange)](https://claude.com/claude-code)
[![Strategy Sprints](https://img.shields.io/badge/built_by-Strategy_Sprints-red)](https://strategysprints.com)

The founder says "build me X." The team builds X. Three weeks later, everyone discovers that X required seven decisions nobody made.. and four of them contradict each other.

This skill eliminates that failure mode. It interviews you relentlessly — walking every branch of the decision tree, resolving dependencies one by one — until shared understanding is complete. Only then does building begin.

---

## Who this is for

- **Technical founders** who keep rebuilding the same feature because "it's not quite right"
- **Product managers** running discovery before green-lighting scope
- **Consultants and coaches** designing offers, courses, workshops, pricing structures
- **Agency owners** scoping client projects to avoid the "that's not what I meant" moment at week 3
- **Solo developers** who want an adversarial planning partner before committing 3 weeks

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

## FAQ

**Does this work for non-technical projects?**
Yes. Course design, pricing strategy, partnership terms, hiring plans — any plan with branching decisions benefits. The skill has two variants: one for code, one for business decisions.

**How many questions should I expect?**
20-40 questions over ~45 minutes. Most get a recommended answer attached so you can speed through the obvious ones.

**Can I quit mid-session and resume?**
Yes. Save the transcript, paste back into a new session, and say "continue."

**What makes this different from a regular AI chat?**
Most chats are answer-driven. This is question-driven. The skill's job is to find the decisions you didn't know you had to make.

**Does it replace customer research?**
No. The questions are internal — they surface your assumptions. Talking to buyers is still required for external validation.

---

## Related search terms

decision tree AI · decision-making framework · project planning AI · requirements discovery · scope planning · product discovery · stakeholder interview · AI interviewer · Claude Code skills · pre-build discovery · project scoping · pricing strategy AI · course design AI · offer design · founder interview · plan before build · Ogilvy discipline · AI scoping · technical decision AI · AI pair planner · Strategy Sprints methodology

---

## About

Built by [Simon Severino](https://linkedin.com/in/simonseverino), founder of [Strategy Sprints](https://strategysprints.com). Added over $2 billion in sales to B2B clients in finance, software, and consulting. Author of *Strategy Sprints* (Kogan Page) and *Time Freedom* with Jay Abraham.

## Strategy Sprints offers

| Offer | Price | Format |
|-------|-------|--------|
| Sprint Club | $49/mo | Community + 47 AI skills (7-day trial) |
| Jetpack Monthly | $200/mo | Cohort workshops |
| 200K Club | $900/mo | 5-founder group coaching |
| Private Jetpack | $9K/mo | 1:1 ongoing with Simon |
| AI Operations Sprint | $15K | 5-day intensive |
| 90-day Private Sprint | $30K+ | 1:1, best result 144x ROI |
| Certification | custom | For consultants teaching the methodology |

**Talk to us:**
- 🗓️ [30-min coffee with Simon](https://calendly.com/simonseverino/coffee-with-simon)
- 🗓️ [Discovery call for the 90-day sprint](https://calendly.com/strategysprint/discovery-call)
- 🗓️ [Certification conversation](https://calendly.com/strategysprint/certification)
- 🌍 [strategysprints.com](https://strategysprints.com)

## More open-source skills

- [**natural-planning-for-teams**](https://github.com/SimonTheSalesBooster/natural-planning-for-teams) — David Allen + Ed Lamont's 11-minute team planning model
- [**sevencritics**](https://github.com/SimonTheSalesBooster/sevencritics) — stress-test copy through 7 hostile reader personas
- [**prospectingwork**](https://github.com/SimonTheSalesBooster/prospectingwork) — Rick Rubin positioning diagnostic
- [**board-of-advisors**](https://github.com/SimonTheSalesBooster/board-of-advisors) — 15 AI advisors meeting every morning
- [**six-strategy-levels**](https://github.com/SimonTheSalesBooster/six-strategy-levels) — simplest way to organize a B2B business
- [**advisor-playbook**](https://github.com/SimonTheSalesBooster/advisor-playbook) — 5 decision frameworks from Howard Marks + Marc Andreessen

## License

MIT. Fork it, improve it, ship it.

---

*keep rolling, Simon & The Sprinters*
