# Australian Open: 120 Years of Champions (1905–2025)

> **"What does 120 years of Grand Slam tennis tell us about how champions are made — and who gets to become one?"**

A visual analytics project exploring the full history of Australian Open singles finals, from 1905 to 2025. Built with Tableau and Excel for UTS 32146 Data Visualisation and Visual Analytics (Autumn 2025).

---

## The Story

The Australian Open is one of the oldest Grand Slam tournaments in the world. Behind the match scores lies 120 years of data on seeding, nationality, gender, and match performance — enough to ask meaningful questions about dominance, equity, and what actually predicts a champion.

This project surfaces patterns that aren't obvious from watching the games.

---

## Key Insights

- **Australia and the USA dominate** total wins across both men's and women's divisions — but the gender composition within each country varies significantly
- **Higher seeds win more, but not always** — the relationship between seed ranking and win rate is negative but weak, with notable outliers in both directions (low-seeded champions, high-seeded early exits)
- **Women's champions are more varied in seed position** than men's, suggesting the women's draw has historically been less predictable
- **Early set wins predict match outcomes** — players who win the first set carry a measurable advantage through to the final score
- **The women's tournament began 17 years later** (1922 vs. 1905) — visible as a structural gap in participation timelines
- **Margaret Court (11 titles), Novak Djokovic (10), Serena Williams (7)** are the all-time top performers, with win rates between 0.60–0.68 across sets — high, but not as extreme as titles alone would suggest

---

## Dataset

- **Scope:** Australian Open singles finals, 1905–2025
- **Variables:** 30 total — player identity, nationality, seed, set-wise scores, match outcomes
- **Source:** Compiled historical match records

**Data engineering (manually calculated):**

| Field Added | Description |
|---|---|
| Total Wins | Championships won per player across all years |
| Total Games Played | Total appearances in finals |
| Win Rate | Total Wins / Total Games Played |
| Set Win Rates (1st–5th) | Set-by-set win ratio per player |
| Total Win Rate | Aggregate of all set-wise win rates |

**Missing data handling:**
- Unseeded / missing seed → encoded as `0` (retained for analysis)
- Set win rates for incomplete sets → left blank (preserved accuracy in parallel coordinates)
- Match duration (only 4 valid entries) → removed from dataset

---

## Visualizations (15+)

| Type | What It Shows |
|---|---|
| Choropleth Maps | Global spread of participating countries; champion vs runner-up by country |
| Treemaps | Top players (5+ wins) sized by title count; country win rate by gender |
| Scatter Plot | Seed ranking vs win rate, by gender — with trendlines |
| Gantt Chart | Championship-winning years of top players over time |
| Parallel Coordinates | Set-by-set win rate patterns across all sets |
| 100% Stacked Bar | Gender proportion of champions by country |
| Line Charts | Historical match timelines; set-wise performance trends |
| Geographic Bubble Maps | Champion/runner-up distribution with embedded gender pie charts |

---

## Tech Stack

`Tableau` · `Microsoft Excel` (data wrangling, formula-based transformations) · `Data storytelling`

---

## Files

| File | Description |
|---|---|
| `aus_open_analysis.twb` | Tableau workbook — all 15+ dashboards |
| `data.xlsx` | Cleaned dataset with manually engineered variables |

---

## Context

Individual project. UTS Bachelor of IT — Data Analytics (Autumn 2025).
