# Agency Client Audit

[![skills.sh](https://skills.sh/b/techking007/agency-client-audit-skill)](https://skills.sh/techking007/agency-client-audit-skill)

An [Agent Skill](https://agentskills.io) for **design and development agencies**: web design studios, dev shops, and digital agencies preparing client proposals.

Give it a prospect's company name or URL and get a structured **17-step audit**: discovery, website review, SEO, competitors, design direction, scope, pricing, and outreach hooks, exported as a markdown report ready for pre-sales and proposal work.

Works with **Cursor**, **Claude Code**, **Codex**, and [68+ agents](https://github.com/vercel-labs/skills#supported-agents).

## Install

```bash
npx skills add techking007/agency-client-audit-skill --skill agency-client-audit -a cursor -y
```

```bash
# Global install (all projects)
npx skills add techking007/agency-client-audit-skill --skill agency-client-audit -a cursor -g -y
```

```bash
# Preview without installing
npx skills add techking007/agency-client-audit-skill --list
```

## How to run

| Step | What happens |
|------|--------------|
| 1 | Install the skill (commands above) |
| 2 | Open your agent project (Cursor, Claude Code, Codex, or any [supported agent](https://github.com/vercel-labs/skills#supported-agents)) |
| 3 | Invoke the skill with a prospect URL or describe the task (see **Usage** below) |
| 4 | The agent loads [`reference.md`](skills/agency-client-audit/reference.md) and runs **Steps 1–16** in order, from discovery through executive summary |
| 5 | At **Step 17**, choose where to save the report when prompted |
| 6 | Receive `{CompanySlug}-Audit.md`. See [`examples/Lorem-Corp-Audit.md`](examples/Lorem-Corp-Audit.md) for structure |

### Optional setup

**Default (no setup):** curl and public web sources. Works out of the box.

| Enhancement | Purpose | Setup |
|-------------|---------|-------|
| [Exa MCP](https://exa.ai) | Faster search and page fetch | [`exa-limits.md`](skills/agency-client-audit/exa-limits.md) |
| Browser MCP | Live UI/UX audit, screenshots | Enable in your agent's MCP settings |
| curl fallbacks | When Exa rate-limits | [`curl-tools.md`](skills/agency-client-audit/curl-tools.md) |

## Usage

Invoke the skill or describe the task in plain language:

```
/agency-client-audit https://example.com
```

```
Research this prospect for a website redesign proposal: full audit and scope recommendations
```

```
Our dev shop needs pre-sales discovery: audit their site, SEO, and competitors
```

The agent runs the full workflow and saves `{CompanyName}-Audit.md` to a path you choose.

## Who it's for

| Agency | Typical use |
|--------|-------------|
| Web design studios | Redesign pitches, brand audits, design direction |
| Development shops | Technical audits, migration scope, stack review |
| Full-service digital agencies | End-to-end discovery, CRO, SEO, outreach prep |

## What's included

| Steps | Deliverables |
|-------|--------------|
| 1–2 | Company snapshot, business model, ICP, value proposition |
| 3–5 | Website audit (brand, UI, UX, technical, CRO), SEO, content review |
| 6–8 | Digital presence, competitor landscape, industry context |
| 9–10 | Design inspiration and creative direction |
| 11–13 | Website scope, pricing tiers, opportunity map |
| 14–15 | Outreach hooks, proposal readiness notes |
| 16–17 | Executive summary and markdown export |

Sample report: [`examples/Lorem-Corp-Audit.md`](examples/Lorem-Corp-Audit.md)

## Repository layout

```
skills/agency-client-audit/
├── SKILL.md                    # Entry point
├── reference.md                # Full 17-step workflow
├── templates.md                # Scorecards and export structure
├── client-marketing-context.md # Personas, objections, customer language
├── curl-tools.md               # Free curl fallbacks
└── exa-limits.md               # Exa MCP setup and limits
```

## License

[MIT](LICENSE)
