# Maritime Logistics Operations Analysis

## Project Overview
End-to-end data analysis project analyzing 15,000 cargo movement 
records across a 4-table star schema for Global Maritime Solutions. 
The analysis identifies operational inefficiencies following the 2021 
Suez Canal disruption and provides data-driven recommendations to 
reduce cargo movement times by 15%.

---

## Business Questions Answered
1. **Suez Effect** — When did the disruption occur and how did it 
   impact cargo operations across regional hubs?
2. **Infrastructure Bottleneck** — Which terminals are overloaded 
   and which are underutilized?
3. **Efficiency Anomalies** — Which factors predict longer movement 
   times and which terminals are underperforming?

---

## Key Findings

| Finding | Detail |
|---|---|
| Suez duration spike | +24.1% increase during disruption |
| Most affected region | LATAM (+39.4% spike) |
| Recovery | Unstable for 12+ months, EMEA and LATAM never fully recovered |
| Overloaded terminal | Shannon Gray (APAC) at 1.87x median load |
| Slowest vessel category | Cargo at 534.59 hrs avg (+7% above global avg) |
| Utilization-duration correlation | r = -0.044 (no relationship) |
| Strongest duration predictor | Vessel category (0.55% variance explained) |
| Outlier terminals | 6 terminals >20% above regional average |
| Shift effect | Not statistically significant (p = 0.378) |

---

## Dashboard Preview

### Page 1 — Suez Canal Impact
![Q1 Dashboard](assets/Q1_suez_impact.jpg)

### Page 2 — Terminal Infrastructure Bottleneck
![Q2 Dashboard](assets/Q2_terminal_bottleneck.jpg)

### Page 3 — Efficiency Anomalies
![Q3 Dashboard](assets/Q3_efficiency_anomalies.jpg)

---

## Tools & Technologies
- **Python** — Data cleaning, EDA, statistical analysis
- **Pandas** — Data manipulation and aggregation
- **SciPy** — Pearson correlation, t-tests, statistical significance
- **Matplotlib** — Exploratory visualizations
- **Power BI** — Interactive 3-page executive dashboard
- **SQLite** — (in progress) SQL query layer

---

## Project Structure
maritime-logistics-analysis/
├── data/
│   ├── raw/                    # Original 4-table star schema CSVs
│   └── processed/              # Cleaned analysis-ready tables
├── notebooks/
│   ├── 01_data_cleaning.py     # Cleaning pipeline
│   ├── 02_eda.py               # Exploratory data analysis
│   └── 03_targeted_analysis.py # Phase 3 business question answers
├── dashboard/
│   └── maritime_dashboard.pbix # Power BI dashboard
└── assets/                     # Dashboard screenshots

---

## Data Pipeline
Raw CSVs (15,000 rows)
↓
Data Cleaning
(removed 13,999 duplicates, referential integrity checks,
domain validation, outlier flagging)
↓
Analysis-ready dataset (1,601 verified records)
↓
EDA → Phase 3 Targeted Analysis
↓
Power BI Dashboard (3 pages)

---

## Statistical Methods Used
- Pearson correlation coefficient
- Independent samples t-test
- Between-group variance analysis
- Percentage change calculations
- Standard deviation-based outlier detection
- Median-based utilization scoring

---

## Data Source
Ondatax DataDNA Maritime Challenge (March 2026)
Synthetic dataset — 4 table star schema
Date range: 2021-01-01 to 2024-12-31

---

## How to Run

**Python scripts:**
```bash
pip install pandas numpy scipy matplotlib
python notebooks/01_data_cleaning.py
python notebooks/02_eda.py
python notebooks/03_targeted_analysis.py
```

**Power BI dashboard:**
Open dashboard/maritime_dashboard.pbix in Power BI Desktop
Data will load automatically from processed/ folder

---

## Author
**Sujal** 
Programmer Analyst Trainee — Cognizant Technology Solutions  
[LinkedIn](your-linkedin-url) | [GitHub](your-github-url)
