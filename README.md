# Sean Goudy

**Self-taught engineer. Now operating 21+ automation agents, 18 cron jobs, and 12 schedulers — all running 24/7 with zero manual intervention.**

I don't just write code — I build systems that make decisions, execute trades, publish reports, and learn from outcomes while I sleep. Every project ships. Every system runs in production.

---

## What Runs 24/7

This is what's firing right now, without me touching anything:

| System | What It Does | Agents | Frequency |
|--------|-------------|--------|-----------|
| **AI Sports Betting Analyzer** | ML predictions across NBA, NHL, NCAAB, MLB — picks, confidence scoring, auto-resolve | 11 agents, 12 schedulers | Every game day |
| **OpenClaw Bot** | Browser automation, ML pick filtering, Moltbook publishing, competitive intel | 18 cron jobs | Continuous |
| **Nimrod** | Auto-generates bet slip images with stats, edges, and reasoning | 1 scheduler | Daily 11:55 AM EST |
| **Discord Alerts** | Pushes high-confidence picks and reports to private channels | 1 agent | Real-time |
| **Moltbook Auto-Poster** | Publishes AI-generated sports analysis to social platform | 1 scheduler | Daily 12:00 PM EST |
| **Injury Scraper** | Scrapes Covers.com for real-time injury data across all sports | 1 cron | 5 AM / 5 PM EST |
| **Auto-Resolver** | Resolves completed bets, updates W/L records, feeds back to ML | 1 scheduler | Daily |
| **Investment Reports** | Monte Carlo simulations, portfolio health scoring, risk analysis | Automated | Weekly via GitHub Actions |

**Total: 21+ agents, 18 cron jobs, 12 schedulers** — orchestrated through the Developer Command Center.

---

## What I Ship

### AI Sports Betting Analyzer — *11 agents, 12 schedulers, 2,670+ picks tracked, live 24/7*

A full ML prediction platform that analyzes every game across **NBA, NHL, NCAAB, and MLB** — scrapes stats, runs them through 11 specialized AI agents, generates confidence-scored picks, and tracks results across 7 users. Every sport has its own isolated model so basketball patterns never bleed into hockey. The whole thing runs autonomously on a Cloudflare tunnel.

**Live at [sportsbettingaianalyzer.com](https://sportsbettingaianalyzer.com)**

**The 11 analysis agents** (each examines a different dimension of every game):

| Agent | What It Analyzes |
|-------|-----------------|
| **Orchestrator** | The general manager — coordinates all agents in parallel, aggregates results |
| **ML Learning Agent** | Gradient Boosting models trained per-sport on historical outcomes (614+ NBA samples, 857+ NCAAB, 448+ NHL) |
| **Stats Signal Agent** | Team stats, offensive/defensive ratings, pace, shooting percentages, goalie stats |
| **Trends Agent** | ATS records, over/under trends, home/away splits, streak analysis from Covers.com |
| **Injury Intelligence** | Real-time injury reports — calculates impact on spread based on player value |
| **Injury Monitor** | Background daemon that scrapes Covers.com injuries 2x daily (5 AM / 5 PM EST) |
| **Line Movement Agent** | Tracks opening vs current spread — detects sharp money and reverse line movement |
| **Line Watch Agent** | Background daemon that captures line snapshots throughout the day |
| **Consensus Agent** | Aggregates all agent signals into a single probability with confidence weighting |
| **Narrative Agent** | Generates ESPN-quality analyst text explaining why the pick was made |
| **Nimrod** | Auto-generates visual bet slip images with stats, edges, and reasoning |

**Data sources scraped and analyzed:**
- Team stats per sport (offensive rating, defensive rating, pace, shooting %, goalie stats)
- ATS records and over/under trends from Covers.com (NBA, NHL, NCAAB)
- Real-time injury reports with player impact scoring
- Live odds and line movement tracking
- AP Poll rankings and conference standings (NCAAB)
- Historical pick outcomes for ML retraining

**Tracked results (real data from production):**

| Sport | Picks | Record | Win Rate |
|-------|-------|--------|----------|
| NBA | 869 | 456W-365L | 55.5% |
| NHL | 730 | 381W-304L | 55.6% |
| NCAAB | 1,071 | 526W-495L | 51.5% |
| **Total** | **2,670** | **1,363W-1,164L** | **53.9%** |

**MCP integration — AI agents can call it:**
The analyzer exposes an MCP-compatible API gateway (`/xk/` routes) with API key authentication and rate limiting. Any AI agent or MCP client can query today's picks, historical results, and model confidence scores programmatically. 6 API keys issued, tiered access (free/pro).

Published MCP server: [sports-betting-mcp](https://github.com/seang1121/sports-betting-mcp) — listed on the MCP registry, lets any AI assistant pull live predictions.

**Automation that runs daily:**
- 12 schedulers: auto-resolve results, refresh suggestions, retrain ML models, generate Nimrod images, post to Discord, maintain data retention
- Multi-user weighted learning: admin picks carry 65% weight, other users 35% — proven track records influence the AI more
- Shadow tracking: logs picks silently to build training data without affecting live results
- 6 API keys in rotation for odds data (auto-failover on rate limits)

`Python` `Flask` `SQLite` `scikit-learn` `Playwright` `MCP` · ![Private](https://img.shields.io/badge/repo-private-gray)

---

### Agent Command Center (ACC) — *See your entire automation empire on one screen*

Imagine you've built 21 AI agents, 18 scheduled jobs, and a dozen projects — but they're scattered across folders, configs, and services. How do you know what's running? What's connected to what? What broke at 3 AM?

**ACC solves that.** It's a real-time dashboard that scans your machine, finds every agent, every scheduled job, every tool, and every project — then maps it all on one screen with zero manual setup.

```
You run one command. ACC scans everything. Your whole empire appears.
```

**Think of it like a mission control for your automations:**

| What You See | What It Shows You |
|---|---|
| **Live Relationship Map** | An interactive graph connecting all your projects — which ones talk to each other, share data, or depend on the same services. The map builds itself from your data. No dragging boxes around. |
| **Project Deep Dives** | Click any project and see everything about it — what agents run inside it, what's scheduled, what repos it touches, what tech stack it uses. One click, full picture. |
| **Automation Overview** | Every cron job, every scheduler, every agent — listed with status (running, errored, disabled), last run time, and delivery target. Know instantly if something's broken. |
| **Tool Inventory** | Every AI tool you've installed, every custom command you've written, every hook that fires on save or commit. Most developers don't even know what they have installed — this shows all of it. |
| **Global Search** | `Ctrl+K` and start typing. Finds anything across all tabs — projects, agents, tools, repos. Instant results. |

**How it works under the hood:**
1. A Python scanner (zero dependencies) crawls your machine — finds AI configs, git repos, scheduled tasks
2. It auto-detects tech stacks from 16+ framework files (package.json, requirements.txt, Cargo.toml, go.mod, etc.)
3. Everything gets mapped into 11 structured data files that the React dashboard reads
4. A hook auto-syncs the dashboard every time you end a coding session — it stays current without you thinking about it

**The whole thing is open source.** Clone it, run the scanner, and in 60 seconds you're looking at a dashboard of your own setup — even if you only have 2 projects.

`TypeScript` `React 19` `Tailwind 4.2` `Vite 8` `Python` · [View Repo →](https://github.com/seang1121/acc-agent-command-center)

---

### AI Business with Automated Agents — *6 AI agents, plug-and-play for any business*

A complete system that lets one person run an entire business using AI agents as automated employees. Website + Python backend + owner dashboard. Works for **any business type** — pressure washing, law firm, dental office, restaurant, real estate, auto detailing, landscaping. Change one config file and all 6 agents adapt.

**Live showcase: [seang1121.github.io/ai-business-with-automated-agents](https://seang1121.github.io/ai-business-with-automated-agents/)**

**The 6 agents:**
- **Leads Agent** — drafts personalized follow-ups within minutes of form submission
- **Estimating Agent** — calculates ballpark price ranges from service config
- **Scheduling Agent** — finds open time slots based on business hours and existing jobs
- **Reviews Agent** — drafts thank-you + Google review requests after job completion
- **Finance Agent** — generates invoices with line items, tax, and payment methods
- **Marketing Agent** — drafts platform-specific social media posts with hashtags

Demo mode runs without API keys. 4 live demo sites (pressure washing, law firm, dental, restaurant). 22 passing tests.

`Python` `Flask` `SQLite` `Claude API` `HTML/CSS/JS` · [View Repo →](https://github.com/seang1121/ai-business-with-automated-agents) · [Live Demos →](https://seang1121.github.io/ai-business-with-automated-agents/)

---

### Investment Command Center — *10 analyzers, automated weekly reports*

Full-stack investment intelligence. Monte Carlo simulation (10k paths), Markowitz portfolio optimization, Gordon Growth valuation, 5 stock/fund scanners, risk analysis, proactive advisor, financial health scoring. Weekly automated reports via GitHub Actions.

`Python` `FastAPI` `Next.js` `TypeScript` `SQL` · [View Repo →](https://github.com/seang1121/investment-command-center)

---

### March Madness Bracket Predictor — *77% accuracy, 14-year backtest*

5 independent prediction models combined into a calibrated ensemble. KenPom efficiency, defensive identity, market intelligence, tempo/matchup analysis, and historical seed patterns. 18 CLI commands, Monte Carlo simulation, champion-diversified bracket strategy for 2026.

`TypeScript` `Node.js` · [View Repo →](https://github.com/seang1121/ncaab-MarchMadness-Trend-analysis)

---

### Henchmen Trader — *Polymarket prediction markets*

Trading bot for Polymarket. Sportsbook odds signals feed a Kelly criterion position sizer with hard risk limits (20% max daily loss, 10% max position, 30% drawdown halt). Dead market sniper for mispriced contracts. Paper trading pipeline with live execution ready.

`Python` `Flask` `SQLite` `SQL` · ![Private](https://img.shields.io/badge/repo-private-gray)

---

### OpenClaw Bot — *18 cron jobs, fully autonomous*

AI executive assistant running 18 scheduled jobs that operate my entire ecosystem without manual intervention. Browser automation, ML pick filtering, social publishing, competitive intelligence, and cross-platform reporting — all orchestrated through a local WebSocket gateway with PM2 process management.

**Active cron jobs (all deliver to Discord automatically):**

| Job | Schedule | What It Does |
|-----|----------|-------------|
| **Morning Briefing** | Daily 7:00 AM | Compiles overnight results, today's schedule, and action items |
| **Henchmen Auto-Picks (Weekday)** | Mon-Fri 2:30 PM | Logs into betting analyzer, reads ML learnings, places picks across all sports |
| **Henchmen Auto-Picks (Weekend)** | Sat-Sun 10:30 AM | Same pipeline, earlier timing for weekend game schedules |
| **Post-Resolve Analysis** | Daily 3:15 AM | Runs pick analysis on last 500 picks, updates learning patterns, compiles W/L summary |
| **Discord Picks Digest (Weekday)** | Mon-Fri 2:45 PM | Formats and publishes today's AI picks to Discord channel |
| **Discord Picks Digest (Weekend)** | Sat-Sun 10:45 AM | Weekend version of picks digest |
| **Daily Fishing Report** | Daily 5:00 AM | Runs 6-API fishing analyzer, delivers Go/No-Go scoring to Discord |
| **Dashboard Watcher** | Every 6 hours | Monitors system health, reports agent status and anomalies |
| **Evening Summary** | Daily 11:00 PM | End-of-day recap — results, P&L, next-day preview |
| **Competitor Monitor** | Weekly (Mon 8 AM) | Scrapes competitor activity and publishes intel report |
| **Daily Henchmen Fact** | Daily 8:00 PM | AI-generated insight about patterns learned from working with the data |
| **Moltbook Publishers** | Multiple schedules | Daily picks, results recaps, comment monitoring, engagement (currently being rebuilt) |

**Key capabilities:**
- Browser automation via OpenClaw's built-in Chromium (logs into web apps, fills forms, scrapes data)
- ML-informed pick filtering — reads `BETTING_LEARNINGS.md` before every pick session
- Cross-platform delivery — Discord, Telegram, Moltbook from a single pipeline
- Isolated sessions per job — each cron runs in its own context, no crosstalk
- Auto-recovery — jobs track consecutive errors and last delivery status

`Node.js` `Python` `JavaScript` `Discord.js` `PM2` · ![Private](https://img.shields.io/badge/repo-private-gray)

---

### Google Workspace CLI — *Rust, Google Developer*

Google Workspace command-line tool — one CLI for Drive, Gmail, Calendar, Sheets, Docs, Chat, Admin, and more. Dynamically built from Google Discovery Service. Includes AI agent skills. Contributing to the official Google Workspace ecosystem.

`Rust` · [View Repo →](https://github.com/seang1121/cli)

---

### Docker MCP Registry — *Go*

Official Docker MCP registry contributor. Infrastructure for discovering and distributing Model Context Protocol servers across the ecosystem.

`Go` · [View Repo →](https://github.com/seang1121/mcp-registry)

---

## Full Project Index

<details><summary><strong>Analytics & Trading (6 projects)</strong></summary>

| Project | What It Does | Stack | Link |
|---------|-------------|-------|------|
| **AI Sports Betting Analyzer** | ML predictions across NBA, NHL, NCAAB, MLB — 11 agents, 12 schedulers | Python, Flask, SQLite, scikit-learn | [Live Site](https://sportsbettingaianalyzer.com) · Private |
| **March Madness Predictor** | 5-model ensemble, 77% accuracy, 18 CLI commands | TypeScript, Node.js | [Repo](https://github.com/seang1121/ncaab-MarchMadness-Trend-analysis) |
| **Henchmen Trader** | Polymarket bot — Kelly sizing, risk management, dead market sniper | Python, Flask, SQLite | Private |
| **Sportsipy** | Multi-sport stats scraping library | Python | [Repo](https://github.com/seang1121/sportsipy) |
| **Sports Betting MCP** | MCP server — exposes predictions to AI agents | Python, MCP | [Repo](https://github.com/seang1121/sports-betting-mcp) |
| **Betting AI Landing** | Marketing site for the analyzer platform | HTML, CSS, JavaScript | [Repo](https://github.com/seang1121/betting-ai-landing) |

</details>

<details><summary><strong>AI & Automation (5 projects)</strong></summary>

| Project | What It Does | Stack | Link |
|---------|-------------|-------|------|
| **AI Business with Automated Agents** | 6 AI agents run any business — leads, scheduling, invoicing, marketing | Python, Flask, SQLite, Claude API | [Repo](https://github.com/seang1121/ai-business-with-automated-agents) · [Live](https://seang1121.github.io/ai-business-with-automated-agents/) |
| **OpenClaw Bot** | 18 cron jobs, browser automation, ML filtering, social publishing | Node.js, Python, Discord.js, PM2 | Private |
| **Agent Command Center** | Zero-config dashboard — auto-discovers agents, MCP servers, hooks, repos, cron jobs. Relationship map, deep dives, global search. React 19 + TypeScript strict | TypeScript, React, Tailwind, Python | [Repo](https://github.com/seang1121/acc-agent-command-center) |
| **DAAV** | Developer Automation Agent Visualizer | TypeScript | [Repo](https://github.com/seang1121/developer-automation-agent-visualizer) |
| **Fishing Report Analyzer** | 6-API intelligence, 100-pt Go/No-Go scoring | Python | [Repo](https://github.com/seang1121/Fishing-Report-Analyzer) |

</details>

<details><summary><strong>Finance (4 projects)</strong></summary>

| Project | What It Does | Stack | Link |
|---------|-------------|-------|------|
| **Investment Command Center** | 10 analyzers, Monte Carlo, Markowitz optimizer, weekly auto-reports | Python, FastAPI, Next.js, TypeScript | [Repo](https://github.com/seang1121/investment-command-center) |
| **Mortgage Rate Tracker** | Daily rate monitoring, lender comparison, historical logging | Python | [Repo](https://github.com/seang1121/Mortgage-Interest-Rate-Lookup) |
| **CD Ladder Analyzer** | CD rate comparison and ladder strategy simulator | HTML, JavaScript | [Repo](https://github.com/seang1121/CD-Ladder-Analyzer) |
| **Loan Officer Exam Prep** | NMLS SAFE MLO exam study course and prep guide | HTML | [Repo](https://github.com/seang1121/Loan-Officer-Exam-Prep-Study-Guide) |

</details>

<details><summary><strong>Developer Tools & MCP (7 projects)</strong></summary>

| Project | What It Does | Stack | Link |
|---------|-------------|-------|------|
| **Google Workspace CLI** | One CLI for Drive, Gmail, Calendar, Sheets, Docs, Chat, Admin | Rust | [Repo](https://github.com/seang1121/cli) |
| **Docker MCP Registry** | Official MCP server discovery and distribution | Go | [Repo](https://github.com/seang1121/mcp-registry) |
| **MCP Servers** | Model Context Protocol server implementations | TypeScript | [Repo](https://github.com/seang1121/servers) |
| **Sports Betting MCP** | Registry-listed MCP server — exposes predictions to AI agents | Python, MCP | [Repo](https://github.com/seang1121/sports-betting-mcp) |
| **Agent Academy** | Multi-agent orchestration, reference agents | PowerShell | [Repo](https://github.com/seang1121/agent-academy) |
| **Awesome MCP Servers** | Curated community MCP server list | Markdown | [Repo](https://github.com/seang1121/awesome-mcp-servers) |
| **NVDA Screen Reader** | Contributing accessibility fixes to open-source screen reader | Python | [Repo](https://github.com/seang1121/nvda) |

</details>

<details><summary><strong>Infrastructure (3 projects)</strong></summary>

| Project | What It Does | Stack | Link |
|---------|-------------|-------|------|
| **Developer Command Center** | React dashboard — monitors all agents, schedulers, cron jobs | TypeScript, React, Tailwind | Private |
| **Process Monitor** | WMI daemon for process detection and alerting | Python, WMI | Private |
| **Fixer GitHub** | Automated repo cleanup and maintenance | Python | Private |

</details>

---

## Languages & Tools

```
Python         ████████████████████████  Primary — Flask, FastAPI, scikit-learn, scrapers
TypeScript     ████████████████         React, Next.js, Node.js, Vite
Rust           ████████████             Google Workspace CLI, systems programming
JavaScript     ████████████             Discord.js, browser automation, PM2
SQL            ████████████             SQLite across every major project
Go             ████████                 Docker MCP Registry, infrastructure
Shell/Bash     ████████                 Automation scripts, schedulers, CI
HTML/CSS       ██████                   Landing pages, dashboards, demo sites
```

**Frameworks:** Flask · FastAPI · React · Next.js · Discord.js
**AI/ML:** scikit-learn · Claude API · MCP Protocol · Multi-agent systems
**Data:** SQLite · yfinance · NOAA APIs · Polymarket CLOB API · Web scraping
**Infrastructure:** PM2 · Cloudflare Tunnel · Vite · GitHub Actions · Docker · OpenClaw
**Ecosystem:** Google Developer · MCP Protocol contributor

---

## What Sets Me Apart

**I'm self-taught — and I'm already running 21+ agents in production.** Not tutorials. Not toy projects. Real systems processing real data, making real predictions, and publishing real results every day.

**Everything is automated.** My cron jobs fire, data pipelines run, ML models retrain, reports publish, and trades execute — all without me touching a keyboard.

**I build end-to-end.** From scraping raw data to training models to deploying dashboards to monitoring with alerts. Every project is a complete system, not a script.

**I build for any industry.** The AI Business Agents system proves it — one config file adapts 6 AI agents to run a law firm, dental office, restaurant, or any other business. Same architecture, different config.

**Multi-language.** Python, TypeScript, Rust, Go, JavaScript, SQL — I pick the right tool for the job. Contributing to the Google Workspace CLI (Rust) and Docker MCP Registry (Go).

**Scale:** 27 projects · 8 languages · 21+ agents · 18 cron jobs · 12 schedulers · 4 live demo sites

---

## GitHub Stats

![Sean's GitHub Stats](https://github-readme-stats.vercel.app/api?username=seang1121&show_icons=true&theme=dark)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=seang1121&layout=compact&theme=dark)

---

*Building systems that make decisions while I sleep.*
