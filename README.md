# Nuggets-Lineup-Analysis
Analyzing Denver Nuggets linenup performance without Nikola Jokic using 2025-26 season data
# Denver Nuggets Lineup Optimization: Without Jokić (2025-26)

## Overview

What happens to the Denver Nuggets when Nikola Jokić sits? This project analyzes Denver's 2025-26 lineup data to identify which 5-man combinations perform best without their MVP center — examining offensive efficiency, shot selection patterns, and how individual players adapt their games when the team's offensive hub leaves the floor.

Built as part of a sports analytics portfolio by a data professional transitioning into the sports industry.

---

## The Question

Nikola Jokić is one of the greatest players in NBA history and the fulcrum of everything Denver does offensively. But roster depth matters — especially in a long playoff run. Which lineups can hold things together when he's on the bench? And how does his absence change the way individual players operate?

The 2025-26 season provided a real-world case study: Jokić missed significant time due to injury, forcing David Adelman's coaching staff to experiment with non-traditional lineup combinations under actual game conditions.

---

## Key Findings

- **8 of the top 20 most-used Nuggets lineups** this season do not include Jokić — a direct result of his injury absence
- **Non-Jokić lineup performance varies significantly** — the best bench combinations approach league-average efficiency while others struggle considerably
- **Spencer Jones features prominently** in non-Jokić lineups due to injuries — a two-way player seeing rotation minutes he wouldn't typically receive in a healthy season
- **Peyton Watson's shot selection changes dramatically** without Jokić on the court — he takes significantly more non-restricted area paint shots (floaters, pull-up jumpers) as he creates more off the dribble rather than operating as a catch-and-shoot weapon in Jokić's system

---

## Case Study: Peyton Watson With vs. Without Jokić

One of the most interesting individual storylines of Denver's 2025-26 season is Peyton Watson's expanded role. Without Jokić acting as the offensive hub and drawing defensive attention, Watson must create more for himself — resulting in a notably different shot profile.

**Methodology:** Compared Watson's 2024-25 season (Jokić healthy, full season) to 2025-26 (Jokić missing significant time) as a proxy for on/off court impact.

**Key Differences:**
- Increased volume of mid-range and non-RA paint shots in 2025-26
- More off-the-dribble creation (floaters, pull-up jumpers)
- Shift away from catch-and-shoot opportunities within Jokić's system

> This analysis demonstrates how a dominant player's presence fundamentally shapes the shot profiles of his teammates — and what those players look like when forced to operate independently.

---

## Data & Methodology

### Lineup Data
- Source: Basketball Reference (2025-26 Denver Nuggets lineups)
- Metric: Net rating per 100 possessions vs. league average
- Scope: Top 20 lineups by total minutes played

> **Note on data:** Basketball Reference's 5-man lineup data is presented as differentials vs. league average rather than raw counting stats. Positive values indicate better-than-average performance; negative values indicate worse-than-average. This still allows meaningful lineup comparison and ranking.

### Shot Chart Data
- Source: NBA API (shotchartdetail endpoint)
- Players: Peyton Watson
- Seasons: 2024-25 and 2025-26 Regular Season

---

## Visualizations

### Peyton Watson Shot Chart Comparison
Side-by-side shot charts comparing Watson's 2024-25 season (more Jokić) vs. 2025-26 season (less Jokić), showing the shift in shot location and selection.

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python | Core programming language |
| Pandas | Data manipulation and analysis |
| nba_api | NBA official statistics API |
| Matplotlib | Shot chart visualization |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Development environment |

---

## Data Sources

- **Basketball Reference** — Nuggets 5-man lineup data (2025-26)
- **NBA API** — Peyton Watson shot chart data (2024-25 and 2025-26)

---

## How to Run

**Prerequisites:**
```bash
pip install nba_api pandas numpy matplotlib seaborn
```

**Steps:**
1. Clone this repository
2. Place `nuggets_lineups_2025-26.csv` in the project directory
3. Open `Nuggets_Lineup_Analysis.ipynb` in Jupyter Notebook
4. Run all cells from top to bottom

> **Note:** The NBA API can be rate-limited. If you encounter connection errors, add `time.sleep(3)` between API calls.

---

## Project Structure

```
Nuggets-Lineup-Analysis/
│
├── Nuggets_Lineup_Analysis.ipynb        # Main analysis notebook
├── nuggets_lineups_2025-26.csv          # Lineup data (Basketball Reference)
├── watson_shot_chart_comparison.png     # Shot chart visualization
└── README.md                            # This file
```

---

## Limitations & Future Enhancements

**Current Limitations:**
- Lineup data represents net rating differentials, not raw counting stats
- Shot chart analysis uses season-over-season comparison as proxy for on/off court impact (play-by-play data would be more precise)
- Analysis limited to top 20 lineups by minutes

**Future Enhancements:**
- **Play-by-play analysis** — directly measure lineup performance on specific possessions
- **Defensive metrics** — opponent shooting %, rim protection, defensive rating by lineup
- **Additional players** — expand shot chart analysis to Murray, Porter Jr., Gordon
- **Opponent context** — how do lineups perform vs. top defenses specifically?
- **Full season data** — revisit at end of 2025-26 season with complete dataset
- **Playoff analysis** — do optimal lineups change in postseason?

---

## About

Built by **Zach Peterschmidt** — analytics professional with 6+ years of experience in data strategy, predictive modeling, and performance analytics. Former 4-year collegiate soccer player at Johnson & Wales University (Denver campus). Seeking opportunities in sports analytics with Denver-area organizations.