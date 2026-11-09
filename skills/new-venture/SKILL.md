---
name: new-venture
description: Scaffold a new venture workspace (CLAUDE.md, ledgers, primer, MCP config) in the current directory from the cofounder-os templates, then run a kickoff interview. Use when starting a new venture repo.
disable-model-invocation: true
---

# New venture

1. The templates are in `templates/venture/` at the root of the cofounder-os plugin (two levels above this skill's base directory). Copy all of them into the current directory. Don't overwrite existing files; report any you skipped.
2. Rename `.mcp.json.example` → keep it as an example; tell the founder which servers to enable.
3. **Kickoff interview** (one question at a time, max 8):
   - What is the venture in one sentence, and who is it for?
   - Why you? (founder–market fit, unfair advantage)
   - What evidence do you already have? (grade it)
   - Hours per week, budget cap, deadline you're working to.
   - What would make you stop?
4. Fill `venture.md` and `ledgers/founder-constraints.md` from the answers.
5. Draft 8–15 assumptions in `ledgers/assumptions.md` across desirability, viability, feasibility, founder. Score them.
6. Call `skeptic` on the thesis (venture.md + assumptions only).
7. Propose the first experiment with `experiment-design` and the first `next-step`.
8. Suggest `git init` and a first commit if this isn't a repo yet.
