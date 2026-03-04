# Hi, I'm Sean 👋

**Builder of data-driven tools that turn raw information into smarter decisions**

I build practical applications that aggregate data from multiple sources, detect patterns, and surface actionable insights — whether it's sports analytics, personal finance, or local fishing conditions. Python-first, automation-heavy, and always backed by real data.

---

## 🚀 What I Build

### 🏀 AI Sports Betting Analyzer
Full-stack AI betting platform with an 11-agent analysis pipeline, per-sport ML models, and multi-user pick tracking.
- **Tech:** Python, Flask, SQLite (WAL), scikit-learn, APScheduler, Cloudflare Tunnel
- **Sports:** NBA (16 stats) · NHL (18 stats) · NCAAB (18 stats) · MLB (28 stats — Opening Day 2026)
- **Highlights:**
  - 11-agent pipeline (line movement, injury intelligence, trends, ML learning, consensus, narrative, and more)
  - Sport-siloed ML models — each sport trains independently, no cross-contamination
  - Dual-signal totals model (raw scoring + defense-adjusted) for Over/Under direction
  - Independent bet direction — spread, ML, and totals each compute separately
  - Shadow picks system — learns from all games, not just logged ones
  - Multi-user leaderboard with 30-day rolling window and H2H matchups
  - Auto-resolve scheduler (9:30pm + 3am EST), auto-scan (10am/2pm/6pm/10pm EST)
  - Nimrod — automated bet slip generator + Twitter/X posting agent
  - Real-time injury + ATS data from Covers.com
  - 6-key API rotation with auto-failover
  - Live at [sportsbettingaianalyzer.com](https://sportsbettingaianalyzer.com)
- **Status:** Private repo (proprietary model)

### 🏈 NCAAB March Madness Trend Analysis
6-year deep dive (2019–2025) into why teams win at every round of the NCAA Tournament.
- **Coverage:** All 192 R64 games, 96 R32 games, Sweet 16, Elite 8, Final Four, and Championship
- **Key findings:**
  - The "Efficiency Staircase" — each round has a distinct AdjEM floor teams must clear
  - R32→Sweet 16 is the steepest cliff in the bracket (+14 → +22+ AdjEM)
  - Champion gate: KenPom top 6 + AdjO top 25 + AdjD top 25 — unbroken in the KenPom era
  - "Extreme Teams" (elite one dimension, weak the other) = 0 championships in 22 years
  - Three Cinderella archetypes with distinct depth ceilings
- **Live site:** [seang1121.github.io/ncaab-MarchMadness-Trend-analysis](https://seang1121.github.io/ncaab-MarchMadness-Trend-analysis/)
- [View Repository →](https://github.com/seang1121/ncaab-MarchMadness-Trend-analysis)

### 💰 Fidelity Fund Analyzer
Portfolio strategy comparison tool across 30+ Fidelity mutual funds and ETFs.
- **Tech:** Python, GitHub Pages, GitHub Actions (auto-generates weekly reports)
- **Strategies:** 6 tiers from Conservative (5-7%) through Moonshot (60-150%+)
- **Features:** 1-year projections, risk profiles, rebalancing guides, DCA implementation plans, tax efficiency guidance
- **Live site:** [seang1121.github.io/Fidelity-Fund-Analyzer](https://seang1121.github.io/Fidelity-Fund-Analyzer/Fidelity-Fund-Analyzer/)
- [View Repository →](https://github.com/seang1121/Fidelity-Fund-Analyzer)

### 🏦 CD Ladder Analyzer
CD ladder simulator comparing rates, strategies, and institutions to maximize savings yield.
- **Tech:** Python, GitHub Pages
- **Institutions:** Pentagon Federal, Navy Federal, Connexus, Vanguard, Ally, Marcus
- **Strategies:** 3-Rung Short, 5-Rung Classic, 5-Rung Staggered, Barbell
- **Features:** Maturity schedules, projected interest earned, liquidity timelines
- **Live site:** [seang1121.github.io/CD-Ladder-Analyzer](https://seang1121.github.io/CD-Ladder-Analyzer/)
- [View Repository →](https://github.com/seang1121/CD-Ladder-Analyzer)

### 📝 Loan Officer Exam Prep Study Guide
Self-contained NMLS SAFE MLO exam study course with structured learning across 4 modes.
- **Modes:** Topic deep dives, flashcards, quizzes, full practice exams
- **Coverage:** All 5 exam categories — Loan Origination (27%), Federal Laws (24%), Ethics (18%), General Knowledge (20%), State Content (11%)
- **Features:** 7-week study plan, 16 sessions, critical threshold reference tables, law-to-regulation mapping
- [View Repository →](https://github.com/seang1121/Loan-Officer-Exam-Prep-Study-Guide)

### 🏠 Mortgage Interest Rate Tracker
Daily mortgage rate monitor with historical analysis and trend detection.
- **Tech:** Python, Bankrate API + Chase scraper fallback, JSON storage
- **Features:** Day-to-day comparison, 7-day trends with directional indicators, configurable alert thresholds
- **Use case:** Rate shopping, refinance timing, market analysis
- [View Repository →](https://github.com/seang1121/Mortgage-Interest-Rate-Lookup)

### 🎣 Fishing Report Analyzer
6-source fishing conditions aggregator for Mayport, Jacksonville, FL.
- **Tech:** Python, BeautifulSoup, NOAA API
- **Sources:** ProAngler, FishingBooker, Tides4Fishing, NOAA Buoy MYPF1, TideTime
- **Features:** Live buoy data, tide predictions, solunar forecasts, water temp, wind conditions
- [View Repository →](https://github.com/seang1121/Fishing-Report-Analyzer)

---

## 💻 Tech Stack

| Category | Tools |
|----------|-------|
| **Languages** | Python (primary), JavaScript, SQL |
| **Backend** | Flask, SQLite (WAL mode), APScheduler |
| **ML/AI** | scikit-learn, multi-agent pipelines, sport-siloed models |
| **Scraping** | BeautifulSoup, Requests, lxml |
| **Frontend** | Jinja2, HTML/CSS/JS, GitHub Pages |
| **Infrastructure** | Cloudflare Tunnel, GitHub Actions CI/CD, Windows Task Scheduler |
| **APIs** | The Odds API, NOAA, Bankrate, Twitter/X, Covers.com |

---

## 🎯 What Drives Me

**Multi-source aggregation** — one source is a data point, six sources is intelligence

**Pattern recognition** — trends matter more than snapshots; why things happen matters more than what happened

**Practical tools** — everything I build solves a real problem I actually have

**Clean architecture** — sport-siloed learning, singleton DB patterns, no cross-contamination, automated scheduling

---

## 📊 Current Focus

- Adding MLB to the betting analyzer (28-stat pitcher-first model, target: Opening Day 2026)
- Expanding NCAAB research with 2026 tournament data as it happens
- Refining multi-user weighted ML as pick history grows (75-100+ picks per sport)

---

## 📈 GitHub Stats

![Sean's GitHub Stats](https://github-readme-stats.vercel.app/api?username=seang1121&show_icons=true&theme=dark)

---

## 📫 Get In Touch

- **GitHub:** [@seang1121](https://github.com/seang1121)

---

**"Where data meets decision-making"**
