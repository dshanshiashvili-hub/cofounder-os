---
name: prd-writer
description: Write a lean PRD for the minimum artifact an experiment needs. Use only after an experiment card exists; refuses to spec features with no card.
---

# Lean PRD

A PRD here exists to serve an experiment, not a roadmap. Keep it to one page.

## Preconditions
- An experiment card exists. Link it. If not, stop and design the experiment first.

## Sections
1. **Experiment link and what this artifact must make measurable.**
2. **Customer and job** (JTBD): "When <situation>, I want to <motivation>, so I can <outcome>."
3. **Scope: must-have only.** The smallest set that lets the experiment run. Everything else goes to "Explicitly out".
4. **Explicitly out.** List what we are not building and why.
5. **User flow.** 3–7 steps.
6. **Instrumentation.** Events, properties, where they are tracked.
7. **Acceptance criteria.** Testable statements.
8. **Effort and cost** (from Architect): hours, money, unit cost.
9. **Kill switch.** How we turn it off and what happens to users who touched it.

## Check before handing off
- Could a manual or no-code version run the same experiment? If yes, say why we aren't doing that.
