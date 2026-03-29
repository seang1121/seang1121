# Hey, I'm Sean

**Sales professional by day. Self-taught engineer by obsession.** I got tired of doing repetitive tasks manually, so I started building systems to do them for me. Now I have 20+ autonomous agents, 12 schedulers, and 11 cron jobs running 24/7 while I work my day job.

I don't have a CS degree. I have problems I refused to solve manually twice.

---

## What I Build

I solve my own problems with code, then open-source them so you don't have to.

### Betting & Sports Analytics
> I wanted better sports picks. So I built an ML platform with 12 analysis agents that runs across NBA, NHL, NCAAB, and MLB.

| Project | What It Does | Stack |
|---------|-------------|-------|
| [**Sports Betting MCP**](https://github.com/seang1121/sports-betting-mcp) | The first MCP server for sports betting -- 9 tools, 59.6% win rate, 1,353+ picks | Python, MCP |
| [**March Madness Predictor**](https://github.com/seang1121/ncaab-MarchMadness-Trend-analysis) | 5-model ensemble, 14-year backtest, 77% accuracy. Beats chalk by 26 pts/yr | TypeScript |
| [**Henchmen Trader**](https://github.com/seang1121/henchmen-trader) | Autonomous Polymarket bot -- exploits sportsbook-vs-crowd mispricings | Python, Flask |

### Finance & Mortgage Tools
> I work in sales in the mortgage/finance space. These tools save me hours every week and they'll save you hours too.

| Project | What It Does | Stack |
|---------|-------------|-------|
| [**Mortgage Rate Lookup**](https://github.com/seang1121/Multi-Lender-Mortgage-Rate-Lookup) | One command, 10 lenders ranked best to worst. Beats anti-bot detection | Python, Patchright |
| [**Daily Rate Reports**](https://github.com/seang1121/OpenClaw-Mortgage-Interest-Rates-Report) | Automated daily mortgage rates delivered to Discord -- set up once, never check again | Python, OpenClaw |
| [**Investment Command Center**](https://github.com/seang1121/investment-command-center) | Monte Carlo simulation, Markowitz optimization, 12 AI analyzers | TypeScript, Python, Next.js |
| [**CD Ladder Analyzer**](https://github.com/seang1121/CD-Ladder-Analyzer) | Compare CD rates and ladder strategies across 6 institutions | Python, GitHub Pages |

### Henchmen -- My Autonomous AI Operator
> Everything above runs itself because of this. Henchmen is an autonomous AI operator built on [OpenClaw](https://openclaw.ai) that orchestrates my entire ecosystem -- 24/7, zero manual intervention.

```
                Morning Briefing (7 AM)
                     |
  Injury Monitor --> Betting Analyzer --> AI Picks --> Discord
  (5 AM / 5 PM)     (12 agents)         (2:30 PM)    (auto-posted)
                          |
                     ML Learning <-- Auto-Resolver (nightly)
                          |
  Mortgage Scraper ------+----- Fishing Report (sunrise)
  (daily, 10 lenders)    |
                    Evening Summary (11 PM)
```

**What it manages autonomously:**
- 28 cron jobs -- morning briefings, sports picks, fishing reports, mortgage rates, evening summaries
- Self-healing -- detects crashed processes, restarts services, diagnoses gateway issues
- Brain database -- 6 SQLite tables tracking picks, patterns, trades, and auto-extracted learnings
- Validators -- PII guard blocks personal info before any public output, threat detector catches prompt injection, pick validator enforces betting rules as code
- Memory system -- structured by topic (patterns, anti-patterns, systems), not date dumps

**Why OpenClaw:** I needed something that could operate a computer like a human -- browse the web, manage files, run scripts, and make decisions. OpenClaw gave me that. I built the 4-layer architecture (Identity, State, Knowledge, Operations) on top of it so every file has exactly one job and the system can reason about itself.

### AI Agents & Automation
> I believe one person with the right agents can run what used to take a team. These tools prove it.

| Project | What It Does | Stack |
|---------|-------------|-------|
| [**AI Business Agents**](https://github.com/seang1121/ai-business-with-automated-agents) | Run a business with 6 AI agents -- one config file, any industry. [Live demo](https://seang1121.github.io/ai-business-with-automated-agents) | Python, Flask |
| [**Agent Command Center**](https://github.com/seang1121/acc-agent-command-center) | Dashboard that auto-discovers your MCP servers, agents, hooks, and cron jobs | TypeScript, React |

### Everything Else
| Project | What It Does |
|---------|-------------|
| [**Fishing Report Analyzer**](https://github.com/seang1121/Fishing-Report-Analyzer) | 7 free APIs, 9 spots ranked, Go/No-Go score for Jacksonville ICW fishing |
| [**NMLS Exam Prep**](https://github.com/seang1121/Loan-Officer-Exam-Prep-Study-Guide) | Built my own study system to pass the mortgage loan originator exam |

---

## The Sales + Code Playbook

Most people think sales and engineering are different worlds. I think they're the same skill applied differently:

- **Mortgage rates are hard to compare?** I built a scraper that checks 10 lenders in 30 seconds
- **Sports picks take hours of research?** I built 12 AI agents that do it in parallel
- **Small businesses can't afford a marketing team?** I built 6 AI agents that handle leads, scheduling, invoicing, and reviews for any industry
- **Bracket pools are pure guesswork?** I built a 5-model ensemble backtested against 14 tournaments

If you're in sales, finance, or any non-technical field -- **you can do this too.** Every one of these projects started as "I wonder if I can automate this" and ended as a production system. Start with a problem you're tired of solving manually.

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Shell](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)

---

## GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=seang1121&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="GitHub Stats" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=seang1121&layout=compact&theme=tokyonight&hide_border=true&langs_count=10" alt="Top Languages" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=seang1121&theme=tokyonight&hide_border=true" alt="GitHub Streak" />
</p>

---

## Currently

- Building MLB prediction models for Opening Day 2026
- Expanding the MCP server ecosystem for sports analytics
- Trading on Polymarket with autonomous edge detection
- Tracking mortgage rates daily across 10 lenders for my sales work

---

## Let's Connect

- **Live platform:** [sportsbettingaianalyzer.com](https://sportsbettingaianalyzer.com)
- **Social:** [Moltbook @HenchmenAI](https://www.moltbook.com/u/henchmenai)

---

*Sales professional. Self-taught engineer. Building the systems that do the boring stuff so I don't have to.*
