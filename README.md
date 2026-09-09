# Compensation Dashboard

⚠️ **Sensitive data notice:** This dashboard contains compensation data — salary, bonus, CTC, and compa-ratio broken down by department, gender, job level, and location. This is among the most sensitive categories of HR data a company holds. **Do not push real compensation figures to a public repository.** Keep this repo **private**, or replace all figures with fully synthetic/dummy data before publishing. Treat the numbers below as illustrative of the dashboard's structure, not as data cleared for public release.

A Power BI dashboard analyzing employee compensation — pay levels, gender pay distribution, performance-linked increments, and geographic salary ranges — to support compensation planning and pay-equity review.

![Dashboard Overview](docs/screenshots/overview_dashboard.png)

## Overview

Compensation analytics dashboard tracking pay across departments, gender, job levels, and locations. Covers Average CTC of 1.03M, Total CTC of 517M, and a Compa-Ratio of 502.55, plus performance-linked increment trends and a geographic salary map. Built in Power BI with DAX.

## Key Metrics

| Metric | Value |
|---|---|
| Average Bonus | 115.02K |
| Average CTC | 1.03M |
| Average Increment | 8.46 |
| Total CTC | 517M |
| Median Salary | 457M |
| Compa-Ratio | 502.55 |

## Dashboard Sections

- **Compensation by Departments** — bar chart of total compensation across IT, Finance, Operations, Marketing, HR, and Sales.
- **Salary based on Gender** — donut chart splitting total salary (517M) between Male and Female employees.
- **Increment based on Performance Rating by Job Level** — table showing average performance rating and average increment % across job levels L1–L5+, with totals.
- **Salary Range by Business Unit & Location** — geographic map plotting salary distribution across regions, segmented by business unit (Commercial, Corporate, Operations, Technology).

## Filters

- **Department** — filter all visuals by department.
- **Location** — filter all visuals by location.

## Tech Stack

- **Power BI Desktop** — dashboard authoring
- **Power Query (M)** — data transformation
- **DAX** — calculated measures (see [docs/dax_measures.md](docs/dax_measures.md))

## Data

> **No real employee compensation data is included in this repository.** Place your own dataset in `data/raw/` before opening the `.pbix` file, or point Power BI to your own data source. See [docs/data_dictionary.md](docs/data_dictionary.md) for expected columns.

## Repository Structure

```
Compensation-Dashboard/
├── data/
│   ├── raw/            # original/source dataset — sensitive, do not commit real data
│   └── processed/      # cleaned data used by the model
├── pbix/
│   └── Compensation_Dashboard.pbix
├── docs/
│   ├── screenshots/    # dashboard images for this README
│   ├── data_dictionary.md
│   └── dax_measures.md
├── reports/
│   └── Compensation_Dashboard.pdf   # optional exported PDF view
├── .gitignore
├── .gitattributes
└── README.md
```

## Getting Started

1. Clone this repository.
   ```bash
   git clone https://github.com/<your-username>/Compensation-Dashboard.git
   ```
2. Add your dataset to `data/raw/` (synthetic/anonymized data only if the repo is public).
3. Open `pbix/Compensation_Dashboard.pbix` in **Power BI Desktop**.
4. Update the data source path/connection if needed (Home → Transform Data → Data Source Settings).
5. Refresh the data and explore.

## License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.

## Data Privacy

Compensation, bonus, CTC, and compa-ratio data broken down by gender, department, and job level can reveal pay-equity patterns and individual compensation ranges. **Do not commit real employee compensation data to a public repository.** Use anonymized/synthetic data, or keep the repo private.
