# Hi, I'm Sean 👋

**Data enthusiast building tools that turn information into insights**

I specialize in creating practical applications that aggregate data from multiple sources, analyze trends, and provide actionable intelligence. Whether it's sports analytics, fishing conditions, or financial markets, I believe in making smart decisions backed by real data.

---

## 🚀 What I Build

### 🏀 AI Sports Betting Analyzer
Multi-sport statistical analysis system with machine learning capabilities and multi-user pick tracking.
- **Tech:** Python, Flask, SQLite, Machine Learning
- **Sports:** NBA (18-stat model), NHL (18-stat model), NCAAB (KenPom/efficiency-based)
- **Features:**
  - Sport-siloed weighted learning — NBA, NHL, NCAAB each learn independently from their own outcomes
  - Multi-user leaderboard with 30-day rolling performance windows
  - Unified AI Picks page — scan games, log picks, track results in one workflow
  - AP Poll auto-refresh scheduler (5am EST daily)
  - Auto-scan scheduler (10am / 2pm / 6pm / 10pm EST)
  - Confidence calibration with stat attribution tracking
  - Shadow picks system — learns from all games, not just logged picks
  - Covers.com injury integration for NBA, NHL, NCAAB
  - Custom domain: [sportsbettingaianalyzer.com](https://sportsbettingaianalyzer.com) *(launching soon)*
- **Status:** Private (proprietary algorithms)

### 🏈 NCAAB March Madness Trend Analysis
6-year research report (2019–2025) covering every round of the NCAA Tournament — R64 through champion.
- **Primary focus:** Why teams win and advance at each stage (statistical + efficiency analysis)
- **Coverage:** R64/R32, Sweet 16, Elite 8, Final Four — one deep-dive file per round + complete combined doc
- **Key findings:**
  - R32→Sweet 16 is the steepest efficiency cliff in the bracket (AdjEM +14 → +22+)
  - AdjD top 40 is the floor for any sustained run — without it teams exit in R32
  - KenPom inversions (lower seed outranks higher) = 60%+ outright win rate
  - Three Cinderella archetypes with distinct depth ceilings (Defense-first / Balanced / Offense-first)
  - Champion gate: KenPom top 6 + AdjO top 25 + AdjD top 25 — unbroken in the KenPom era
  - Extreme Team flag (top-10 one metric, outside top-50 other) = 0 championships in 22 years
- **ATS/Betting appendix** included in each file (labeled separately from analytical content)
- [View Repository →](https://github.com/seang1121/ncaab-MarchMadness-Trend-analysis)

### 🎣 Fishing Report Analyzer
Comprehensive fishing conditions aggregator for Mayport, Jacksonville, FL
- **Tech:** Python, Web Scraping, API Integration
- **Sources:** 6 professional data sources (NOAA, Tides4Fishing, ProAngler, etc.)
- **Features:** Live buoy data, tide predictions, solunar forecasts
- [View Repository →](https://github.com/seang1121/Fishing-Report-Analyzer)

### 🏠 Mortgage Interest Rate Tracker
Daily mortgage rate monitoring with historical analysis
- **Tech:** Python, JSON Database, Bankrate API
- **Features:** Day-to-day comparison, 7-day trends, automated tracking
- **Use Case:** Rate shopping, refinance monitoring, market analysis
- [View Repository →](https://github.com/seang1121/Mortgage-Interest-Rate-Lookup)

---

## 💻 Tech Stack

**Languages:**
- Python (Primary)
- JavaScript
- SQL

**Frameworks & Libraries:**
- Flask (Web Applications)
- SQLite (Database)
- BeautifulSoup (Web Scraping)
- Requests / httpx (API Integration)

**Infrastructure:**
- Cloudflare Tunnel + custom domain routing
- ngrok (tunneling)
- Scheduled task automation (Windows Task Scheduler)

**Specialties:**
- Sport-siloed machine learning with weighted stat attribution
- Multi-user collaborative learning systems
- Real-time odds + injury data integration (The Odds API, Covers.com)
- KenPom / efficiency-based tournament modeling
- Data aggregation from multiple live sources
- Automated scheduling and reporting

---

## 🎯 What Drives Me

I'm passionate about **data-driven decision making**. My projects share a common thread:

✅ **Multi-Source Aggregation** — Why rely on one source when you can combine many?
✅ **Historical Tracking** — Trends matter more than snapshots
✅ **Why Things Happen** — Not just what the data says, but why teams win, why markets misprice, why patterns hold
✅ **Practical Applications** — Build tools that solve real problems
✅ **Clean Architecture** — Sport-siloed learning, singleton database patterns, no cross-contamination

---

## 📊 Current Focus

- Launching [sportsbettingaianalyzer.com](https://sportsbettingaianalyzer.com) on a custom domain via Cloudflare Tunnel
- Adding MLB support to the betting analyzer (target: Opening Day 2026)
- Expanding NCAAB research to include 2026 tournament data as it happens
- Refining multi-user weighted learning as more pick history accumulates (target: 75-100 picks per sport)

---

## 🌟 Highlighted Work

### Sport-Siloed Machine Learning
Each sport (NBA, NHL, NCAAB) maintains its own independent learning weights — NBA injuries mean something different than NHL goalie injuries. Stat attributions track which of 18 factors contributed to each pick outcome, and weights adjust automatically after every resolve cycle.

### Multi-User Weighted Learning
Collaborative pick tracking where proven performers (admin users) are weighted 65% vs 35% for standard users. 30-day rolling leaderboard surfaces recent performance rather than all-time records.

### NCAAB Tournament Research (2019–2025)
Built a 4-file research system covering every round with a consistent dual-purpose structure: statistical analysis of *why teams win* is the primary content (efficiency cliffs, Cinderella archetypes, favorite warning signs), with ATS/betting data in clearly labeled appendix sections.

### 6-Source Data Fusion
Fishing report system that intelligently aggregates data from 6 professional sources — tide predictions, weather, injury reports, and solunar forecasts — into a single actionable report.

---

## 📫 Get In Touch

- **GitHub:** [@seang1121](https://github.com/seang1121)

---

## 📈 GitHub Stats

![Sean's GitHub Stats](https://github-readme-stats.vercel.app/api?username=seang1121&show_icons=true&theme=dark)

---

**"Where data meets decision-making"**
