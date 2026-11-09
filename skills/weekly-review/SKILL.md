---
name: weekly-review
description: Run the weekly venture review: what we learned, decisions, metrics snapshot, Skeptic audit, next week's single focus, and proposed lesson updates for each agent. Use weekly or when the founder asks for a review.
---

# Weekly review

## Steps
1. **Learned this week:** 3–5 bullets, each tied to evidence and graded (money / commitment / behavior / intent / opinion).
2. **Experiments:** for each live or finished one: result vs. thresholds, decision (log it in `ledgers/decisions.md`).
3. **Metrics:** append a row to `ledgers/metrics.md`.
4. **Assumptions:** re-score risk × uncertainty; mark validated/invalidated.
5. **Skeptic audit:** call `skeptic` with the ledgers only (no recommendations). Relay its output verbatim.
6. **Next week:** one focus and one experiment (use `next-step`). Check against founder constraints.
7. **Team learning:** propose lesson updates (below).

## Proposing lesson updates
Look for: wrong calls an agent made, corrections the founder had to give, gates that were skipped, tools that worked or failed, recurring friction.

For each proposal:
```
Agent: <operator / researcher / architect / growth / skeptic>
Lesson: <one line, actionable rule, written as an instruction>
Evidence: <what happened this week>
Generalizes to other ventures? <yes / no: venture-specific>
```
- If **yes**: it goes to the agent's `## Lessons` section in the cofounder-os repo (the founder applies and commits it; see the repo README).
- If **no**: it goes to the venture's `domain-primer.md` or `venture.md`, not the team.
- Never apply a lesson without the founder's explicit approval. Max 3 proposals per week; quality over quantity.
- Prefer sharpening or replacing an existing rule over adding a new one. Profiles must stay short.

## Output
Write the review to `reviews/YYYY-MM-DD.md` and give the founder a 10-line summary with the proposals.
