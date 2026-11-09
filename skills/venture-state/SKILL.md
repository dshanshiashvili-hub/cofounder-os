---
name: venture-state
description: Formats and rules for the venture ledgers (assumptions, experiments, decisions, metrics, founder constraints). Load before reading or writing any file in ledgers/.
---

# Venture state: the ledgers

The ledgers are the venture's memory. Every agent reads them; only the Operator writes them (specialists propose entries). Append, don't rewrite history: superseded entries get a status change, not deletion.

## ledgers/assumptions.md
One row per assumption. Score risk 1–5 (how bad if false) and uncertainty 1–5 (how little evidence). Priority = risk × uncertainty.

| ID | Assumption | Type | Risk | Uncertainty | Priority | Evidence so far | Status |
|---|---|---|---|---|---|---|---|
| A1 | ... | desirability / viability / feasibility / founder | 5 | 4 | 20 | ... | open / validated / invalidated |

## ledgers/experiments.md
One card per experiment. Thresholds are written before launch and never edited after.

```
### E<n>: <name>
- Tests assumption: A<n>
- Hypothesis: We believe <customer> will <behavior> because <reason>.
- Method: <fake door / interviews / concierge / landing page / prototype / ...>
- Metric: <one primary metric>
- Pass if: <threshold>   Kill if: <threshold>   (in between = iterate once)
- Sample / duration: <n> / <dates>
- Cost cap: <money> and <hours>
- Owner agent(s): <...>
- Status: draft / live / done
- Result: <numbers, filled after>
- Decision: link to D<n>
```

## ledgers/decisions.md
```
### D<n> — YYYY-MM-DD — <decision: persevere / pivot / kill / other>
- Context: <experiment or question>
- Evidence: <graded: money/commitment/behavior/intent/opinion>
- Inputs: researcher: ... | architect: ... | growth: ... | skeptic (verbatim verdict): ...
- Founder override of a gate? <no / yes: which and why>
- Reversible? <yes/no>
```

## ledgers/metrics.md
Weekly snapshot table: date, stage, customers spoken to (cumulative), paying customers, primary experiment metric, burn this week, notes.

## ledgers/founder-constraints.md
Hours per week, runway/deadline the founder chooses to share, hard constraints (location, skills, budget cap). Re-read before proposing any plan; never plan beyond these.
