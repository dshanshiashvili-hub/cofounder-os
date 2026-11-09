---
name: next-step
description: Decide the single most valuable next step for the venture right now. Use when the founder asks "what now?", at session start, after any result, or when work is drifting.
---

# Next step

Output exactly one next step, plus at most two "not now" items you are deliberately parking.

## Procedure
1. Read the ledgers (`venture-state`).
2. Check the gates in order. The first one that fires decides the next step:
   - A live experiment is past its deadline → read results, decide persevere/pivot/kill.
   - No customer evidence logged in 7+ days → customer contact (interviews, outreach, a concierge session).
   - A result has no decision → make the decision.
   - More than 2 live experiments → close or pause one.
   - A research task is over its time box → force a conclusion.
3. Otherwise: take the top open assumption by priority and design the cheapest test that could invalidate it (`experiment-design`).
4. Sanity-check against `founder-constraints.md`: can it be done in the founder's available hours this week?

## Anti-patterns to call out by name
- **Building to avoid selling:** coding when the riskiest assumption is about demand.
- **Analysis paralysis:** another report when a test would answer it.
- **Premature scaling:** infra, branding, hiring, fundraising before PMF signal.
- **Feature creep:** adding scope to an experiment mid-flight.
- **Vanity metrics:** signups, likes, waitlist size without commitment.

## Output
**Next step:** <one action, owner, done-by date, how we'll know it's done>
**Why this, not something else:** <2 lines>
**Parked:** <0–2 items>
