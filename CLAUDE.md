# Marcus retirement artifact

Build and ship an interactive "are we okay?" retirement-readiness tool for a financial planner's prospects, plus a 100-word writeup — Clief Notes Weekly Competition #2.

Built on ICM: folders carry sequencing, hierarchy carries context, files carry state. The structure is the documentation — if something needs explaining, the explanation goes in that folder's CONTEXT.md, not in your head.

## Where things live

| Folder | What it holds |
|---|---|
| `stages/` | the pipeline, in execution order |
| `_shared/` | factory: voice + design/brand guidelines |
| `_shared/source/` | the raw client brief (source of truth) that voice/brand guidelines were distilled from |
| `.claude/skills/icm-architect/` | the skill this workspace was scaffolded with |

## Route by what just happened

| If | Go to | Then stop at |
|---|---|---|
| starting fresh | `stages/01_objectives/CONTEXT.md` | human reads `output/requirements.md` |
| 01's output approved | `stages/02_design/CONTEXT.md` | human reads `output/design-spec.md` |
| 02's output approved | `stages/03_build/CONTEXT.md` | human reads `output/writeup.md` |
| asked for status | scan `stages/*/output/` | report what exists |

## The one rule

Nothing moves to the next stage until a person has read the output of the last one.
