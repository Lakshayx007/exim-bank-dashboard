# EXIM Bank Portfolio Optimization Dashboard

A Power BI dashboard built for **India Exim Bank** to analyze export credit allocation across 98 sectors, identify funding gaps, and provide data-driven portfolio reallocation recommendations.

---

## Overview

India Exim Bank extends export credit across a wide range of sectors, but traditional allocation methods may not reflect the growth potential of each sector. This dashboard addresses that gap by classifying sectors by priority tier, simulating NPA risk, and recommending strategic reallocations.

---

## Dashboard Pages

| Page | Description |
|------|-------------|
| **Export Momentum** | Tracks export growth trends across sectors to identify high-momentum industries |
| **Credit Allocation** | Visualizes current credit distribution across all 98 sectors |
| **Mismatch Detection** | Highlights sectors where credit allocation is misaligned with export potential |
| **Portfolio Optimization** | Provides reallocation recommendations based on strategic scoring |

---

## Key Features

### Tier Classification
Sectors are classified into three priority tiers based on export performance and growth trajectory:
- **High Priority** — Fast-growing, underfunded sectors with strong export momentum
- **Moderate Priority** — Stable sectors with balanced credit and growth
- **Low Priority** — Declining or over-funded sectors with limited strategic value

### Portfolio NPA Simulation
- Simulates Non-Performing Asset (NPA) risk under different credit allocation scenarios
- Helps assess the credit health impact of reallocation decisions

### Credit Reallocation Recommendations
- Identifies sectors receiving disproportionately low credit relative to their export performance
- Suggests optimal reallocation targets to maximize export credit efficiency

### Strategic Scoring
Two composite scoring models power the optimization engine:

- **Aggressive Growth Score** — Prioritizes sectors with the highest export growth rates and market expansion potential
- **Strategic Alignment Score** — Balances growth with India's trade policy priorities and Exim Bank's mandate

---

## Key Findings

- Identified **underfunded high-growth sectors** where export potential significantly exceeds current credit exposure
- Quantified the **credit-to-export mismatch** across 98 sectors
- Generated actionable **reallocation recommendations** to shift capital toward strategically aligned, high-growth opportunities
- Demonstrated potential NPA risk reduction through optimized portfolio distribution

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard development and visualization |
| **DAX** | Calculated measures, KPIs, and scoring models |
| **Power Query (M)** | Data transformation and cleaning |
| **Excel / CSV** | Source data for sector-level export and credit metrics |

---

## Data Sources

- **India Exim Bank Annual Reports** — sector-wise export credit disbursement and portfolio data
- **Government of India Trade Profiles** — export performance metrics across sectors
- Ministry of Commerce & Industry publications and RBI statistical reports

---

## Project Structure

```
exim-bank-dashboard/
├── README.md
├── screenshots/          # Dashboard page screenshots
└── EXIM Dashboard.pbix   # Power BI project file
```

---

## Screenshots

> Screenshots of all four dashboard pages will be added to the `/screenshots` folder.

---

## Author

**Lakshay Malik**  
MBA (Business Analytics) — BITS Pilani, Pilani Campus  
[GitHub](https://github.com/Lakshayx007) · [LinkedIn](https://www.linkedin.com/in/lakshaymalik3127)

---

## License

This project is intended for academic and portfolio purposes. Data used is for illustrative analysis only.
