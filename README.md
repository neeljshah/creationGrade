# 🏀 Spatial Efficiency Engine
### Part 1 of the Basketball Intelligence Suite

> **Quantifying shot quality beyond make/miss — mapping where players truly dominate, and where they die.**

---

## 📸 Dashboard Preview

![Spatial Efficiency Dashboard](demo.gif)

> *Interactive Power BI dashboard — filter by Player, Team, Season Type, and Matchup in real time.*

---

## 🔍 What This Project Does

Most basketball analysis stops at "did it go in?" The Spatial Efficiency Engine goes deeper — it maps **where shots are created, how efficiently they're converted, and what shot types drive value** across every player and team in the league.

By combining **FG%, Creation Grade, Shot Type distribution, and a live Shot Chart**, this dashboard gives scouts and coaches an at-a-glance read of any player's offensive profile.

---

## 📊 Dashboard Breakdown

### Effective Creation Scatter Plot
- **X-axis:** Creation Grade — a composite score measuring how self-sufficiently a player generates their own shot opportunities
- **Y-axis:** FG% — how efficiently they convert those opportunities
- Players in the **top-right quadrant** are the league's elite: high creation *and* high efficiency
- Filter by matchup (e.g. LAL @ OKC) to isolate game-specific performance

### KPI Cards (Left Panel)
| Metric | Description |
|---|---|
| **FG%** | Overall field goal percentage for the selected filter |
| **Creation Grade** | Composite self-creation score (0–100 scale) |
| **Avg Shot Distance** | Mean distance (ft) of all shot attempts |

### Shot Type Bar Chart
- Side-by-side breakdown of **made vs. missed** attempts by shot category
- Covers: Jump Shot, Pullup, Step Back, Cutting Layup, Driving Layup, Fadeaway, and more
- Instantly reveals a player's **shot diet** — are they a pull-up creator or a cutter?

### Shot Chart
- Spatial scatter plot overlaid on a half-court diagram
- **Green dots** = makes, **Red dots** = misses
- Density clusters reveal **hot zones** and **efficiency deadzones**

---

## ⚙️ Tech Stack

| Tool | Usage |
|---|---|
| **Power BI** | Dashboard design, interactivity, DAX measures |
| **Python (Pandas, NumPy)** | Data cleaning, feature engineering |
| **NBA Stats API** | Shot-level play-by-play data source |
| **DAX** | Creation Grade composite metric logic |

---

## 🧠 Key Insight

> Players like **Shai Gilgeous-Alexander** and **Jalen Williams** sit in the top-right quadrant of the Effective Creation chart — combining a Creation Grade above 60 with 40%+ FG%. This confirms their status as true primary creators, not just volume shooters.

---

## 🚀 How to Use

1. Clone the repo and open the `.pbix` file in Power BI Desktop
2. Use the **Player Name**, **Team Name**, **Season Type**, and **Matchup** filters to drill into any player or game
3. The Shot Chart and KPI cards update dynamically with every filter selection

---

## 📁 Repository Structure

```
Spatial-Efficiency/
├── data/
│   └── shot_data_cleaned.csv
├── notebooks/
│   └── feature_engineering.ipynb
├── dashboard/
│   └── SpatialEfficiency.pbix
└── README.md
```

---

## 🔗 Part of the Basketball Intelligence Suite

| Part | Project | Focus |
|---|---|---|
| **1** | Spatial Efficiency Engine *(you are here)* | Shot quality & creation mapping |
| **2** | Momentum Volatility Index | Game-flow & run detection |
| **3** | Defensive Gravity Model | Off-ball spatial influence |
| **4** | Behavioral Archetyping | Player segmentation & style |
