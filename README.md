# EXIM Bank Strategic Credit Analysis Dashboard

A Power BI dashboard testing the hypothesis: **EXIM Bank is structurally backwards-looking** — allocating credit based on legacy patterns rather than forward-looking export growth signals.

---

## The Core Idea

Three questions drive this project:

1. **Where is EXIM Bank putting its money?** *(e.g., "50% of loans go to Engineering Goods")*
2. **Where is India's export growth actually happening?** *(e.g., "Electronics exports are growing at 32%, but only get 5% of loans")*
3. **What is the mismatch?** — Which sectors are *Underfinanced* (High growth + Low credit) and which are *Legacy Brands* (Low growth + High credit)?

---

## Project Phases

| Phase | Task | Output |
|-------|------|--------|
| **Phase 1 — ETL & Data Structuring** | Vertical stacking of 5-year TradeStat and Annual Report data | Master CSV (~500 records, 7 columns) |
| **Phase 2 — Quantitative Analysis (Python)** | Calculate Export CAGR vs. Credit Growth | Identification of under-funded high-growth sectors |
| **Phase 3 — Visual Intelligence (Power BI)** | Map Risk (NPA) vs. Reward (Demand Index) | Strategic Mismatch Dashboard |
| **Phase 4 — Strategic Recommendations** | Propose Credit Reallocation Model | Gap Analysis and reallocation targets |

---

## Dashboard Pages

| Page | Description |
|------|-------------|
| **Export Momentum** | Tracks export growth trends across sectors to identify high-momentum industries |
| **Credit Allocation** | Visualizes current credit distribution and concentration across sectors |
| **Mismatch Detection** | Scatter plot of Export Value (X) vs. Credit Exposure (Y), bubbles colored by NPA status |
| **Portfolio Optimization** | Reallocation recommendations based on Strategic Priority Score |

---

## Data Dictionary

Dataset covers **FY 2020-21 to FY 2024-25** across **HS Codes 01–99** (~500 observations).

| Column | Field | Definition | Source |
|--------|-------|------------|--------|
| Col 1 | `Year` | Fiscal Year (2020-21 to 2024-25) | Annual Reports |
| Col 2 | `HSCode` | Harmonized System Code (01–99) | TradeStat |
| Col 3 | `Commodity` | Name of the export product | TradeStat |
| Col 4 | `Export_Value` | Total export revenue (INR Cr) | TradeStat |
| Col 5 | `Credit_Exposure` | Bank commitment — (Fund-based + Non-fund based) / 10 (INR Cr) | Table DF-3, Annual Reports |
| Col 6 | `Sectoral_NPA_%` | Default risk per industry | Page 167 Disclosures |
| Col 7 | `Demand_Index` | Future growth potential score (1–5) | MD's Statement |

---

## Core Analytics Logic

### 1. Credit Normalization
```
Credit_Exposure = (Fund-based Credit + Non-fund based Credit) / 10
```
> *Example — FY 2024-25, HS-84 (Engineering Goods):*
> Fund Based ₹1,941.15 Cr + Non-Fund Based ₹1,024.84 Cr = **₹2,965.99 Cr**

### 2. Strategic Priority Score
```
Score = (Demand_Index × 0.7) − (NPA_% × 0.3)
```
Ranks sectors by **Investment Worthiness** — balancing future demand potential against credit risk.

### 3. Mismatch Indicator — "Strategic Funding Gap"
```
IF Export_Growth_Rank < 10 AND Credit_Exposure_Rank > 50 → Flag as "Strategic Funding Gap"
```
Identifies sectors with top-10 export growth but bottom-half credit allocation.

---

## Tier Classification

| Tier | Criteria | Action |
|------|----------|--------|
| **High Priority** | High Demand Index + Low NPA + Strong Export CAGR | Increase Credit Allocation |
| **Moderate Priority** | Balanced growth and credit exposure | Monitor and maintain |
| **Low Priority** | Low Demand + High NPA + Weak Export Growth | Rationalize / Reallocate Credit |

---

## Key Visualizations

- **Asset Quality Trend** — Line chart of Gross NPA over 5 fiscal years
- **Sectoral Concentration** — Credit distribution across HS code categories
- **Mismatch Scatter Plot** — Export Value (X-axis) vs. Credit Exposure (Y-axis), bubble size = sector weight, color = NPA status

---

## Data Sources

- **India Exim Bank Annual Reports** (FY 2020-21 to FY 2024-25) — credit exposure, NPA disclosures (Table DF-3, Page 167)
- **TradeStat (DGCI&S)** — sector-wise export values by HS Code
- **MD's Statement & Disclosures** — Demand Index signals and strategic priorities

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard development and visualization |
| **DAX** | Calculated measures, KPIs, and scoring models |
| **Power Query (M)** | ETL — data transformation, HS code standardization, FY alignment |
| **Python** | Export CAGR calculation, credit growth analysis, mismatch ranking |
| **Excel / CSV** | Master dataset (~500 records, 7 columns) |

---

## Project Structure

```
exim-bank-dashboard/
├── README.md
├── EXIM Dashboard.pbix     # Power BI project file
├── EXIM Dashboard.pdf      # Dashboard screenshots
└── screenshots/            # Individual page screenshots
```

---

## Author

**Lakshay Malik**
MBA (Business Analytics) — BITS Pilani, Pilani Campus
[GitHub](https://github.com/Lakshayx007) · [LinkedIn](https://www.linkedin.com/in/lakshaymalik3127)

---

## License

This project is intended for academic and portfolio purposes. Data sourced from publicly available EXIM Bank annual reports and government trade statistics.
