# AI Workforce Activation

A skill that makes an AI act as **Chief of Staff** for your organisation: it turns your mission into a structured AI team (Team Lead plus specialists), issues role-specific instructions, sets KPIs and reporting, produces a versioned charter and work register, and starts real work. It never claims actions, agents or automations that did not actually happen.

## What you get
| Output | Description |
|---|---|
| Mission and objectives | Structured from your answers or existing chat |
| Team and hierarchy | Roster, reporting lines, authority rules |
| Role cards | 18-element operating instructions per specialist |
| KPIs and reporting | Per role, plus executive update format |
| Charter and work register | Copyable source-of-truth documents with version control |
| Activation report | 14-section summary with honest status |

## Install
Upload the folder (or ZIP) as a skill where your platform supports skills (for example Claude skills or Claude Code `~/.claude/skills/`). On platforms without skills, paste `SKILL.md` as instructions and attach the `references/` files as project knowledge. Exact steps differ by platform; check your platform's documentation.

## Use
Say things like: "Build me an AI team for ...", "Align my existing agents to this mission", "Activate my team", "Update our charter", "What needs my approval?"

## Structure
```
SKILL.md                  core workflow
references/               modes, onboarding, architecture, leadership, role cards,
                          workflows/KPIs, platform notes, integrity rules, templates
examples/                 3 illustrative (fictional) runs
evals/evals.json          8 test prompts to run yourself
LICENSE                   MIT
```

## Compatibility and limits
- Works as pure instructions on any assistant; native agents, connectors and scheduling are used only where the host supports them.
- `references/platform-capabilities.md` holds platform notes researched on 2026-11-23 for Claude Code, ChatGPT and Manus. Codex, Grok, Meta AI and OpenClaw were **not** researched. Re-verify before relying on them.
- The skill runs only when invoked and cannot create persistent memory; keep your latest charter and paste it into new sessions.
- Test status: see `evals/evals.json`; the eval cases have not been run.
