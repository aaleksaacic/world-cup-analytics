# World Cup Analytics

A data processing and analysis project focused on historical FIFA World Cup tournaments. The project cleans, transforms, and consolidates raw tournament records, host country information, and player awards into structured datasets.

## Report

The Power BI report built on top of the processed datasets is available as a PDF (static, non-interactive): [WorldCupReport.pdf](report/WorldCupReport.pdf).

The interactive source file is [worldcup.pbix](report/worldcup.pbix) and can be opened with Power BI Desktop.

## Project Structure

```text
world-cup-analytics/
├── data/
│   ├── raw/           # Raw CSV and JSON data sources
│   └── processed/     # Cleaned and structured output datasets
├── notebooks/
│   ├── 01_cleaning.ipynb
│   ├── 02_worldcup.ipynb
│   ├── 03_hosts.ipynb
│   └── 04_awards.ipynb
├── report/
│   ├── worldcup.pbix        # Power BI report (interactive)
│   └── WorldCupReport.pdf   # Static PDF export of the report
└── README.md
```

## Notebooks Overview

- **01_cleaning.ipynb**: Data cleaning and preprocessing for historical match data (pre-2018). Handles duplicate entries, missing values (including attendance figures), column pruning, and type conversions.
- **02_worldcup.ipynb**: Aggregation and analysis of tournament-level statistics across editions (1930–2026). Calculates champions, runners-up, third and fourth places, total and average goals, extra time and penalty shootouts, attendance metrics, and top-scoring teams.
- **03_hosts.ipynb**: Cleans host country records, standardizes nation names, maps continents, and tracks host team performance.
- **04_awards.ipynb**: Cleans and parses individual tournament awards (e.g., Golden Ball, Golden Boot), standardizing award categories, player names, and team designations.

## Output Datasets

Cleaned outputs are stored in `data/processed/`:

- `matches-pre2018.csv`: Standardized match-by-match historical records.
- `world_cups.csv`: Consolidated tournament summaries with aggregate statistics.
- `hosts.csv`: Host countries, continents, and tournament performance.
- `awards.csv`: Structured player awards and honors.

## Requirements

- Python 3.10+
- pandas
- matplotlib