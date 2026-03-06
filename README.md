# 🎯 Spatial Efficiency & Revenue-Per-Shot (xP) Optimization
> **An Advanced Geospatial Analytics Engine transforming raw coordinate data into strategic "Expected Value" (EV) maps using Python, BigQuery, and Spatial Modeling.**

![Python](https://img.shields.io/badge/Analytics-Python_3.10-3776AB?style=for-the-badge&logo=python&logoColor=white)
![BigQuery](https://img.shields.io/badge/Data_Warehouse-Google_BigQuery-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Business](https://img.shields.io/badge/Focus-Business_Intelligence-FFD700?style=for-the-badge)

---

## 📖 Executive Summary
In both professional sports and global retail, **Spatial Efficiency** is the primary driver of ROI. This project analyzes 500,000+ data points of spatial tracking to solve the "Efficiency Gap." By mapping coordinate-based performance, I developed an **Expected Points (xP) Model** that identifies "High-Value Zones" and "Efficiency Deadzones," shifting strategy from high-volume output to **High-Expected-Value (EV) output.**

---

## 🛠️ Business Analytics Translation
This project demonstrates the exact same methodology used in **Market Territory & Real Estate Analytics**:
*   **Court Zones** $\rightarrow$ Sales Territories or Retail Floor Sections.
*   **Shot Frequency** $\rightarrow$ Customer Traffic / Footfall Density.
*   **Field Goal %** $\rightarrow$ **Conversion Rate**.
*   **Points Per Shot (PPS)** $\rightarrow$ **Average Transaction Value (ATV)**.

---

## 🚀 Key Project Phases

### 1. Data Ingestion & Geospatial Cleaning 🏗️
* **The Problem:** Raw API data provides (X, Y) coordinates but lacks context (Distance, Angle, Zone).
* **Technical Skill:** Data Engineering with `NBA_API`, Coordinate Transformation, and SQL cleaning in **BigQuery**.
* **The Code:** [🔗 View Ingestion Script](./Scripts/Data_Cleaning.py)

### 2. Efficiency Modeling (Hexbin & Heatmapping) 🗺️
* **The Problem:** Raw scatter plots are "noisy." How do we visualize where a resource is *truly* effective?
* **Technical Skill:** Kernel Density Estimation (KDE), Logarithmic Hexbinning, and Matplotlib Court Overlays.
* **The Result:** Identified the **"Point-of-Diminishing-Returns"** in mid-range shot attempts.
* **Visual Representation:**
> ![Shot Chart Placeholder](https://via.placeholder.com/800x400?text=Insert+Hexbin+Shot+Chart+Image+Here)

### 3. Expected Value (EV) & Pricing Sensitivity 📊
* **The Problem:** Is a 40% Three-Point shot better than a 55% Two-Point shot?
* **Technical Skill:** Comparative **ROI Modeling**, Z-Score Normalization against League Averages.
* **The Insight:** Modeled the "Mathematical Break-Even Point" to optimize offensive flow and maximize **Revenue-Per-Possession**.

### 4. Zone Performance Benchmarking (SQL) 🚚
* **The Problem:** Which territories are underperforming the Global Average?
* **Technical Skill:** SQL Window Functions (`AVG() OVER`), `CASE` statements for Zone Partitioning.
* **The Code:** [🔗 View BigQuery SQL Logic](./SQL/Zone_Benchmarking.sql)

---

## 🛠️ Technical Mastery Checklist
- [x] **Geospatial Processing:** Using Euclidean distance to calculate shot proximity.
- [x] **Expected Metrics:** Calculating **eFG%** (Effective Field Goal) and **PPS** (Points Per Shot).
- [x] **BigQuery Integration:** Standardized 10,000+ rows into partitioned tables for high-speed querying.
- [x] **Business Storytelling:** Converting "Missed Opportunities" into **Opportunity Cost** ($$).

---

## 📂 Project Structure
```text
├── SQL/
│   ├── Zone_Benchmarking.sql       # Comparison against League Averages
│   └── Territory_Efficiency.sql    # Conversion rate by court zone
├── Scripts/
│   ├── Data_Cleaning.py            # Coordinate normalization
│   ├── PPS_Analysis.py             # Expected Points Model (ROI)
│   └── Shot_Chart_Engine.py        # Visual Heatmap generator
├── Visuals/
│   ├── Efficiency_Map.png          # Hexbin Visualization
│   └── ROI_Analysis.png            # Points-per-shot Bar Chart
└── README.md
