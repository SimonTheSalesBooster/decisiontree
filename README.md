# Grill Me — Decision Tree Skill

A Claude Code skill that interviews you relentlessly about every aspect of a plan or design until reaching shared understanding, resolving each branch of the decision tree before building anything.

## Why

Most artifacts fail because requirements weren't fully discovered upfront. This skill forces that discovery phase — like rubber ducking, but the duck talks back with recommended answers.

## The Skill

```markdown
---
name: grill-me
description: Interview the user relentlessly about a plan or design until reaching shared understanding, resolving each branch of the decision tree. Use when user wants to stress-test a plan, get grilled on their design, or mentions "grill me".
---

Interview me relentlessly about every aspect of this plan until
we reach a shared understanding. Walk down each branch of the design
tree resolving dependencies between decisions one by one.

If a question can be answered by exploring the codebase, explore
the codebase instead.

For each question, provide your recommended answer.
```

## Non-Coding Variant

For figuring out courses, strategies, business decisions — remove the codebase line:

```markdown
Interview me relentlessly about every aspect of this until
we reach a shared understanding. Walk down each branch of the design
tree resolving dependencies between decisions one by one.
For each question, provide your recommended answer.
```

## How It Works

1. You describe what you want to build or figure out (detailed or vague — both work)
2. The AI asks question after question, walking each branch of the decision tree
3. For each question, it provides a recommended answer — say "yes" to speed through obvious ones
4. Sessions typically last ~45 minutes
5. You end with a rich, fully-discovered set of requirements

## Installation

Copy `grill-me.md` to `~/.claude/commands/grill-me.md`, then use `/grill-me` in Claude Code.

## Built by

Strategy Sprints — [strategysprints.com](https://strategysprints.com)
