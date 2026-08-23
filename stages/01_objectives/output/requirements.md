---
type: product
stage: 01_objectives
source: ../../../_shared/source/marcus-client-brief.md
---

# Requirements — extracted from the brief

## Who it's for
A prospect of Marcus's — dual-income, 35–55, usually with kids — before their first meeting with him.

## The question it must answer
"Are we okay?" — specifically: on track / behind / ahead for retirement, and **by how much**. Not a vague reassurance; a real answer.

## Inputs (hard cap: 5 fields)
1. Age
2. Income
3. Current savings
4. Monthly savings rate
5. Target retirement age

No sixth field without a strong reason. Marcus's own line: *"If you find yourself adding a twelfth input field, you've gone too far."*

## Methodology
Default: the **25x rule** — 25× annual expenses needed at retirement, savings rate backed into from current age, current savings, target retirement age, assuming a **7% average return**.

A different methodology (4% rule, replacement ratio, 10x salary, etc.) is allowed, but only if it's named and explained in the final writeup — Marcus wants to know what he's looking at.

## Behavior when the news is bad
Non-negotiable. The tool must not show a gap and stop. When someone is behind, it must also show at least one path to closing the gap, e.g.:
- how much more per month would close it
- what retiring ~2 years later does
- what holding the current savings rate but working longer does

"Give them a path, not a verdict."

## Output format
Unconstrained by the brief — number, paragraph, chart, traffic light, conversation, or a mix. The only test: **would Marcus actually send this to a prospect?**

## Voice requirement
Must sound like Marcus: honest when the news is good, direct when it isn't, like a real human walking someone through their numbers — not a sterile bank calculator. The brief itself is the voice reference.

## Simplicity requirement
A prospect finishes in under 3 minutes and walks away with a real answer. This is explicitly a design/voice challenge, not a finance challenge.

## Deliverable
1. An interactive tool, built with Claude.
2. A 100-word writeup: who it's for, what it does, and one design choice made and why.

## Delivery & hosting (workspace decision, not from the brief)
The built tool is deployed to GitHub Pages, same pattern as the sibling `competition-1` workspace: the final build stage's output is published via a GitHub Actions Pages workflow, and this workspace itself is pushed to a new GitHub repo. This is a delivery decision for this exercise, not a client requirement — kept separate from the brief-derived requirements above.

## Judging criteria, in stated order
1. Does it solve Marcus's actual problem — can a prospect use it before a call and show up better prepared?
2. Does it sound like Marcus?
3. Is it simple enough that a real person would actually finish it?

Explicitly **not** judged: financial accuracy, modeling complexity, feature count.

## Explicitly out of scope
Anything not stated above — extra input fields, compliance/disclaimer content, precise financial modeling, feature additions in the name of completeness. None of this is in the brief; none of it belongs in the build.
