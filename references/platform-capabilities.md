# Platform Capability Discovery

Principle: **the skill supplies organisational intelligence; the host platform supplies execution capability.** Keep the structure constant, adapt the implementation.

## Three environments (can be combined)
| Env | Description | How to operate |
|---|---|---|
| A | Plain conversational AI | Simulate Chief of Staff, Team Lead and specialists; have them review and challenge each other; keep the charter and register in the conversation |
| B | Native agents / delegation / subagents | Create agents with supported features, give each its role card, delegate, collect and review; Chief of Staff stays the coordinator |
| C | Plugins, connectors, APIs, browser, computer use, automation | Use only integrations that are connected and authorised and that materially help |

## Discovery checklist (assess only what the mission needs)
| Capability | Question | Status values |
|---|---|---|
| Web research | Can it search, browse, verify? | Available / needs setup / needs permission / unsupported |
| Native agents | Can it create and delegate to agents? | same |
| Agent communication | Can agents exchange results? | same |
| Files | Read, create, update documents? | same |
| Email / Calendar | Search, draft, send, schedule? | same |
| External services | Connectors, MCP, APIs? | same |
| Computer use | GUI interaction? | same |
| Automation | Scheduled or event-driven runs? | same |
| Persistent memory | Retained across conversations? | same |
| Project / task tools | Track tasks and deadlines? | same |
Do not assume a mentioned integration is connected or authorised.

## Manual fallbacks
| Missing | Fallback |
|---|---|
| Email | Complete, copy-ready draft |
| Calendar | Schedule and reminder list |
| Native agents | Simulated roles, labelled as such |
| Automation | Written recurring checklist the user triggers |
| Memory | Charter the user keeps and pastes into new sessions |
| Files | Copyable Markdown |

## Platform notes (researched, dated 2026-11-23; re-verify before relying)
Sources are official documentation or vendor posts where noted. Features change quickly.

| Platform | What was found | Source type |
|---|---|---|
| Claude Code | Custom subagents are Markdown files with YAML frontmatter in `.claude/agents/` (project) or `~/.claude/agents/` (user), each with its own context window, system prompt, tool access and permissions. Built-in subagents include Explore, Plan and general-purpose. Docs state subagents can spawn their own subagents as of v2.1.172, with a depth limit. | Official docs (code.claude.com) |
| Claude (chat apps, Cowork, Chrome, Excel and others) | Product list taken from Anthropic's own product information given to this assistant; no further feature research done here. Treat agent/delegation and scheduling support as **unverified** and check in the product. | Not researched in depth |
| ChatGPT | OpenAI's July 9, 2026 post introduces **ChatGPT Work** (agent that gathers info across apps and produces sheets, slides, docs, web apps) with **Scheduled Tasks** (one-off, recurring, event-based, monitoring). An OpenAI help page says the earlier "ChatGPT agent" is no longer available and points to ChatGPT Work. Connectors and custom GPTs also exist. Availability and limits vary by plan. | Official OpenAI pages |
| Manus | Vendor posts (May 2026) describe Scheduled Tasks 2.0 (runs in the same task context, reuses Project setup), Projects with connectors, skills and instructions, and connectors via MCP. Manus is described as part of Meta. A trade article mentions a Chief of Staff template. | Vendor blog / trade press |
| Codex, Grok, Meta AI, OpenClaw and others | **Not researched.** Treat capabilities as unknown; run the discovery checklist live. | n/a |

Rule: if a platform note conflicts with what the live environment shows, trust the live environment and say so.
