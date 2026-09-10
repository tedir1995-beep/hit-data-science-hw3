# Data Science Final Homework - Unsupervised Learning

**Student:** Tedi Revelis  
**Student ID:** 313261919  
**Course:** Introduction to Data Science

This repository contains the complete final homework analysis of the **Hugging Face Models Trending** dataset. The executable notebook covers exploratory analysis, PCA, three clustering methods, feature-space clustering, three anomaly-detection methods, critical reflection, ethical considerations, and the optional visualization dashboard.

## Main research question

> What structure exists among currently trending Hugging Face models, and which models look unusual when popularity, age, activity, metadata, and access characteristics are considered together?

The analysis uses the latest snapshot of 1,000 unique models. This avoids treating repeated daily observations of the same repository as independent samples. The complete 156,000-row source file remains included and unchanged.

## Repository contents

- `notebooks/huggingface_models_unsupervised_analysis.ipynb` - complete executed report, code, tables, and figures.
- `reports/homework_3_report.html` - browser-ready export of the executed notebook.
- `reports/anomaly_dashboard.html` - self-contained interactive anomaly explorer.
- `reports/anomaly_results.csv` - scores, flags, and method agreement for every latest-snapshot model.
- `reports/clustering_results.csv` - cluster assignments for every clustering method.
- `reports/figures/` - 18 exported figures.
- `data/raw/hf_models_snapshot.csv` - frozen source data.
- `requirements.txt` - exact environment used for the submitted run.

## Reproduce the analysis on Windows

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
jupyter notebook notebooks\huggingface_models_unsupervised_analysis.ipynb
```

Open the notebook and choose **Run All** from the repository root. All randomized procedures use seed `42`.

## Dataset integrity

- Rows: `156,000`
- Original columns: `13`
- Latest-snapshot rows: `1,000`
- Numerical analysis features: `13`
- Observation period: `2026-02-24` to `2026-07-30`
- SHA-256: `A74C74F76E7FDF3095861AFA3F52484ACE9C1B6EDD83B24B66F87BAA9DDD2966`
- Source: [Hugging Face Models Trending on Kaggle](https://www.kaggle.com/datasets/zoupet/hugging-face-models-trending)

The notebook verifies the checksum before running.
