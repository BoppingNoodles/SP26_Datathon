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
- The smallest orgs (0–5 staff) are the **largest segment in the dataset** yet face the sharpest capacity constraints — the personalization problem is widespread, not niche
- Small nonprofits face a **double constraint**: tech staffing gaps (11% vs 78% at 121+) and infrastructure gaps (cloud, data policies, agreements) compound each other
- The bottleneck is **implementation, not evaluation** — the tech staff gap is steeper than the MERL staff gap, meaning small orgs can't operationalize AI even when they want to
- **Bias & Equity** is the dominant AI concern, not cost or access — suggesting small orgs are worried about harming the communities they serve, not just about affordability
