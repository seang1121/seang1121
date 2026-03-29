# Sean Goudy

**I work in sales. I build production software.** I started coding because I got tired of doing the same tasks manually every day — comparing mortgage rates, researching sports bets, tracking investments. Now I operate 20+ autonomous agents, 12 schedulers, and 11 cron jobs across 5 domains, all running 24/7 while I work my day job in finance.

Every project here started as a real problem I had. If you have the same problem, it's yours — open source, documented, and ready to run.

---

## By the Numbers

**1,353+** picks tracked | **59.6%** win rate | **10** lenders scraped daily | **20+** autonomous agents | **7** platform users | **12** analysis models | **5** live systems | **11** open-source repos

---

## Production Machine Learning Systems

I built a multi-sport prediction platform with 12 analysis agents that independently evaluate every game across NBA, NHL, NCAAB, and MLB — then reach consensus through weighted scoring. It serves agents with an API key and multiple users, resolves bets automatically, and feeds outcomes back into the models nightly. **Live at [sportsbettingaianalyzer.com](https://sportsbettingaianalyzer.com).**

| Project | What It Demonstrates | Links |
|---------|---------------------|-------|
| **Sports Betting MCP Server** | Published Python package to PyPI. Serves real-time sports analytics to AI agents via the Model Context Protocol. 9 tools, documented track record. | [GitHub](https://github.com/seang1121/sports-betting-mcp) / [PyPI](https://pypi.org/project/sports-betting-mcp/) |
| **March Madness Predictor** | 5-model ensemble with Monte Carlo simulation. Backtested against 14 tournaments (882 games). 77% accuracy, outperforms chalk by 26 pts/year. | [GitHub](https://github.com/seang1121/ncaab-MarchMadness-Trend-analysis) |
| **Polymarket Trading Bot** | Autonomous arbitrage between sharp sportsbook odds and soft prediction market prices. Kelly criterion sizing, 6 sports, 3 execution modes. | [GitHub](https://github.com/seang1121/henchmen-trader) |

## Data Aggregation & Scoring

| Project | What It Demonstrates | Links |
|---------|---------------------|-------|
| **Fishing Report Analyzer** | Aggregates 7 free APIs (NOAA, NWS, Solunar) to score 9 fishing spots with a 100-point Go/No-Go system. Zero dependencies, zero API keys. | [GitHub](https://github.com/seang1121/Fishing-Report-Analyzer) |

## Full-Stack Applications

These are the tools I use in my day job and personal finances. Each one replaced a manual process I was doing weekly.

| Project | What It Demonstrates | Links |
|---------|---------------------|-------|
| **Mortgage Rate Comparison** | Stealth-browser scraper that defeats anti-bot protection on 10 major bank websites simultaneously. Async parallel execution, day-over-day tracking. | [GitHub](https://github.com/seang1121/Multi-Lender-Mortgage-Rate-Lookup) |
| **Investment Command Center** | Next.js + FastAPI platform with Monte Carlo simulation (10K paths), Markowitz portfolio optimization, Gordon Growth valuation, and 5 stock scanners. | [GitHub](https://github.com/seang1121/investment-command-center) |
| **Daily Rate Reports** | Automated mortgage rate delivery to Discord via OpenClaw. Set up once, runs daily, zero maintenance. | [GitHub](https://github.com/seang1121/OpenClaw-Mortgage-Interest-Rates-Report) |
| **CD Ladder Analyzer** | Compare certificate of deposit rates and ladder strategies across 6 institutions. | [GitHub](https://github.com/seang1121/CD-Ladder-Analyzer) / [Live Demo](https://seang1121.github.io/CD-Ladder-Analyzer/) |
| **NMLS Exam Prep** | Built a structured study system to pass the mortgage loan originator exam. 4 modes, 7-week plan, 120 practice questions. | [GitHub](https://github.com/seang1121/Loan-Officer-Exam-Prep-Study-Guide) |

## Autonomous Agents & Orchestration

Everything runs itself because of [OpenClaw](https://openclaw.ai) — an AI operator that can browse the web, manage files, and make decisions like a human. I built **Henchmen** on top of it: a 4-layer autonomous architecture (Identity, State, Knowledge, Operations) that self-heals, learns from outcomes, and orchestrates 20+ agents across sports analytics, mortgage tracking, trading, and daily reporting — all without manual intervention.

| Project | What It Demonstrates | Links |
|---------|---------------------|-------|
| **AI Business Agents** | Plug-and-play website integrator: 6 AI agents handle leads, scheduling, invoicing, reviews, and marketing for any industry. One config file adapts tone, pricing, and behavior. | [GitHub](https://github.com/seang1121/ai-business-with-automated-agents) / [Live Demo](https://seang1121.github.io/ai-business-with-automated-agents) |
| **Agent Command Center** | React dashboard that scans your system and visualizes every MCP server, agent, hook, cron job, and repo in one view. Auto-discovers config, zero manual setup. | [GitHub](https://github.com/seang1121/acc-agent-command-center) |
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

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=seang1121&layout=compact&theme=tokyonight&hide_border=true&langs_count=10" alt="Top Languages" />
</p>

---

## Currently Building

- MLB prediction models with 28 pitcher-specific edges — targeting Opening Day 2026
- A mortgage rate MCP server so any AI agent can call `get_rates(zip_code)` and get live data
- Paper-to-live migration on the Polymarket trading bot with real USDC execution

---

## Live Sites & Demos

- [sportsbettingaianalyzer.com](https://sportsbettingaianalyzer.com) — Live AI betting platform, 7 users, 1,353+ picks tracked
- [AI Business Agents Demo](https://seang1121.github.io/ai-business-with-automated-agents) — Run a business with 6 AI agents, any industry
- [CD Ladder Analyzer](https://seang1121.github.io/CD-Ladder-Analyzer/) — Compare CD rates and ladder strategies across 6 institutions
- [Sports Betting MCP on PyPI](https://pypi.org/project/sports-betting-mcp/) — Install with `pip install sports-betting-mcp`

## Platforms & Social

- [OpenClaw](https://openclaw.ai) — The AI operator foundation my autonomous systems run on
- [Moltbook @HenchmenAI](https://www.moltbook.com/u/henchmenai) — Daily sports analysis and betting insights

## All Repositories

| Repo | Description |
|------|-------------|
| [sports-betting-mcp](https://github.com/seang1121/sports-betting-mcp) | MCP server for sports betting -- 9 tools, live odds, AI picks |
| [ncaab-MarchMadness-Trend-analysis](https://github.com/seang1121/ncaab-MarchMadness-Trend-analysis) | March Madness bracket predictor -- 5-model ensemble, 77% accuracy |
| [henchmen-trader](https://github.com/seang1121/henchmen-trader) | Autonomous Polymarket trading bot -- sportsbook arbitrage, Kelly sizing |
| [Multi-Lender-Mortgage-Rate-Lookup](https://github.com/seang1121/Multi-Lender-Mortgage-Rate-Lookup) | Stealth-browser mortgage rate scraper -- 10 lenders in 30 seconds |
| [OpenClaw-Mortgage-Interest-Rates-Report](https://github.com/seang1121/OpenClaw-Mortgage-Interest-Rates-Report) | Daily mortgage rates delivered to Discord via OpenClaw |
| [investment-command-center](https://github.com/seang1121/investment-command-center) | Monte Carlo, Markowitz optimization, 12 AI financial analyzers |
| [ai-business-with-automated-agents](https://github.com/seang1121/ai-business-with-automated-agents) | 6 AI agents run a business -- one config file, any industry |
| [acc-agent-command-center](https://github.com/seang1121/acc-agent-command-center) | Dashboard that auto-discovers your AI dev setup |
| [Fishing-Report-Analyzer](https://github.com/seang1121/Fishing-Report-Analyzer) | 7 APIs, 9 spots ranked, Go/No-Go fishing score |
| [CD-Ladder-Analyzer](https://github.com/seang1121/CD-Ladder-Analyzer) | CD rate comparison and ladder strategy simulator |
| [Loan-Officer-Exam-Prep-Study-Guide](https://github.com/seang1121/Loan-Officer-Exam-Prep-Study-Guide) | NMLS SAFE MLO exam study system -- 4 modes, 120 questions |
