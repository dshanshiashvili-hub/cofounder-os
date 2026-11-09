# cofounder-os

A venture-agnostic AI founding team for Claude Code. One team, reused across every venture; each venture keeps its own state.

## The team

| Agent | Role | How you reach it |
|---|---|---|
| **Operator** | Lead cofounder. Runs build-measure-learn, enforces the gates, routes work, runs weekly reviews. | The main session (via the venture's `CLAUDE.md` + `operator` skill) |
| **Researcher** | Market & customer research, interviews, synthesis | Operator calls it, or ask "have the researcher…" |
| **Architect** | CTO: stack, build-vs-buy, tool scouting, minimum builds | Same |
| **Growth** | Positioning, channels, pricing tests, unit economics | Same |
| **Skeptic** | Independent board advisor: pre-mortems, kill/continue verdicts. Read-only. | Same; verdicts relayed verbatim |

## Layout

```
cofounder-os/                 ← this repo: the team (plugin)
├── .claude-plugin/           plugin + marketplace manifests
├── agents/                   specialist profiles (each ends with a ## Lessons section)
├── skills/                   playbooks: operator charter, next-step, experiment-design,
│                             prd-writer, weekly-review, customer-discovery, tool-scout,
│                             gtm-experiments, unit-economics, pre-mortem, venture-state,
│                             new-venture
└── templates/venture/        scaffold for each new venture repo

your-venture/                 ← one repo per venture: the state
├── CLAUDE.md                 makes the main session the Operator
├── venture.md  domain-primer.md  stack.md
├── ledgers/                  assumptions, experiments, decisions, metrics, founder-constraints
├── research/  reviews/
└── .mcp.json                 connectors for this venture (from .mcp.json.example)
```

## Install (once)

In Claude Code:

```
/plugin marketplace add dshanshiashvili-hub/cofounder-os
/plugin install cofounder-os@cofounder-os
```

## Start a venture

```
mkdir fashion-venture && cd fashion-venture
claude
> /cofounder-os:new-venture
```

It copies the templates, interviews you, drafts assumptions, gets a Skeptic verdict and proposes the first experiment. Then copy `.mcp.json.example` to `.mcp.json` and keep only the connectors you need now.

## Daily use

- Just talk. The Operator reads the ledgers at session start and tells you the single next step.
- `/cofounder-os:next-step` when you want it to re-decide.
- `/cofounder-os:weekly-review` once a week (or set it as a scheduled task).

## The gates (enforced by the Operator)

1. No build without an experiment card.
2. Max 2 live experiments.
3. A cheaper test is proposed before any build.
4. Research is time-boxed (default 1 day).
5. Every result ends in persevere / pivot / kill, logged.
6. 7 days without customer evidence → customer contact becomes the next step.

You can override any gate; the override is logged.

## Teaching the team

1. The weekly review proposes up to 3 lessons, each marked "generalizes" or "venture-specific".
2. Venture-specific lessons go into that venture's `domain-primer.md` / `venture.md`.
3. General lessons: edit the agent's `## Lessons` section (or the `operator` skill) **in this repo**, commit, push.
4. In Claude Code run `/plugin marketplace update cofounder-os` so every venture picks up the new version.

Git history is the record of how the team changed. Keep profiles short: sharpen or replace rules rather than piling on.

## Notes and limits

- Profiles reference skills as `cofounder-os:<skill>` in the `skills:` frontmatter field and also name them in the body. If your Claude Code version doesn't preload them, the agent still loads them by name.
- Only the Skeptic has a restricted tool list. Tighten others by adding a `tools:` line to their frontmatter.
- Agent teams (agents talking peer-to-peer) are not used by default. The same profiles work as teammates if you enable that experimental mode for a specific debate.

## Setting up on a new computer

Everything lives on GitHub (repos) and Google Drive (files), so a new laptop needs about 10 minutes:

1. Install the **Claude** desktop app and sign in.
2. Install Homebrew (https://brew.sh), then in Terminal:
   ```bash
   brew install gh git
   gh auth login          # choose GitHub.com → HTTPS → Yes → log in with browser
   gh auth setup-git
   ```
3. Download both repos:
   ```bash
   mkdir -p ~/code && cd ~/code
   gh repo clone dshanshiashvili-hub/cofounder-os
   gh repo clone dshanshiashvili-hub/fashion-venture
   ```
4. Install the team:
   ```bash
   claude plugin marketplace add dshanshiashvili-hub/cofounder-os
   claude plugin install cofounder-os@cofounder-os
   ```
5. In the Claude app: **New session** → choose the folder `~/code/fashion-venture`. The Operator loads automatically; approve the connectors when asked.

Before giving an old computer away: check both repos are pushed (`git status` says "up to date"), then erase it (System Settings → General → Transfer or Reset → Erase All Content and Settings).
