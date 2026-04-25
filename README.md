# SP26 Datathon

**Research Question:** How can nonprofits use AI to personalize outreach to increase donor retention?

## Setup
```bash
cd work
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Dependencies
- pandas
- matplotlib
- numpy
- seaborn
- scipy
- scikit-learn

## Data
- `ai_survey_results_2024_n=930.csv` — primary survey dataset, one row per respondent (930 nonprofits across 5 continents)
- `ai_survey_normalized_clustering_data.csv` — binary-encoded version for AI use/demand comparisons, no nulls

## Notebook Structure (`work/main.ipynb`)
- **Step 0** — Data cleaning: parse list columns, impute nulls, strip whitespace, merge datasets
- **Theme Classification** — `ai_theme` column classifying each respondent's AI sentiment into 7 themes
- **Step 0: EDA** — Distributions of org size, role, and AI readiness cluster
- **Step 1: Capacity Gap** — Staffing and infrastructure analysis identifying which nonprofits have the least capacity to personalize donor outreach

## Key Findings
- Orgs with 0–15 staff make up the majority of respondents and have the lowest technical capacity
- Only 11% of 0–5 staff orgs have dedicated tech staff vs. 78% for 121+ staff orgs
- Late Adopters (cluster 0) are the highest-opportunity segment — open to AI but not yet using it
- Bias & Equity is the dominant AI concern across all org sizes
