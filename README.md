# Applied Machine Learning – Classification & Imbalanced Data

## Overview

This repository contains end-to-end classification case studies focused on evaluation discipline, handling class imbalance, and practical model selection. The notebooks demonstrate reproducible pipelines, sensible metrics for imbalanced settings, and short write-ups that capture modelling judgment (not just leaderboard results).

## Why this repo is useful for recruiters

- Compact, focused case studies that each follow a reproducible pipeline.
- Emphasis on evaluation and modelling trade-offs (precision/recall/F1, ROC-AUC).
- Demonstrates data-prep, feature pipelines, resampling (SMOTE), and model benchmarking.

## Top-line results (at-a-glance)

- Breast cancer — KNN (notebook): primary focus on recall/F1 and k-selection analysis. See `notebooks/breast_cancer_knn.ipynb` for test metrics and plots.
- Customer churn — SMOTE & benchmarking (notebook): compares resampling vs class-weighting and benchmarks Logistic Regression, Decision Trees, and XGBoost; primary metric: precision/recall trade-offs and ROC‑AUC. See `notebooks/churn_prediction_smote.ipynb`.
- Diabetes — XGBoost vs Logistic Regression (notebook): hyperparameter tuning and calibration checks; primary metric: ROC‑AUC. See `notebooks/diabetes_xgboost_vs_logreg.ipynb`.

## Techniques demonstrated

- Evaluation: stratified splits, cross-validation
- Imbalance: SMOTE, class-weighting comparisons
- Modeling: Logistic Regression, KNN, Decision Trees, Random Forest, Gradient Boosting, XGBoost
- Engineering: pipelines, scaling, reproducible notebooks

## Case studies (short table)

| Project                               | Purpose (1 line)                                               |             Primary metric |      Status | File                                         |
| ------------------------------------- | -------------------------------------------------------------- | -------------------------: | ----------: | -------------------------------------------- |
| Breast cancer — KNN                   | Small-scale diagnostic classifier with k-selection and scaling |                Recall / F1 | exploratory | `notebooks/breast_cancer_knn.ipynb`          |
| Customer churn — SMOTE & benchmarking | Imbalanced churn prediction; compare resampling and models     | Precision/Recall / ROC‑AUC |    polished | `notebooks/churn_prediction_smote.ipynb`     |
| Diabetes — XGBoost vs LogReg          | Benchmarking and calibration checks; hyperparameter tuning     |                    ROC‑AUC | exploratory | `notebooks/diabetes_xgboost_vs_logreg.ipynb` |

Notes: the `Status` column marks whether a notebook is a polished, recruiter-ready artifact or an exploratory working notebook.

## How to run (quick)

Preferred quick route: open the notebook in Colab or run locally in a virtual environment.

Local example (macOS / zsh):

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -U pip
pip install -r requirements.txt
jupyter lab  # or jupyter notebook
```

`requirements.txt` is included at the repo root and contains common packages used by the notebooks.

## Naming & presentation (optional)

- Recommendation: keep exploratory work in `notebooks/`. Export recruiter-ready, polished copies to `projects/<project-name>/` with a short project README and a single result figure.
- Recruiter-friendly filename style (optional): `01-breast-cancer-knn-classification.ipynb`, `02-customer-churn-smote-classification.ipynb`, `03-diabetes-xgboost-vs-logreg.ipynb`.

## Developer notes

- `requirements.txt` is available at the repo root; use it for reproducibility.
- If you want, I can extract final numeric metrics for each notebook and add them into the "Top-line results" section.

---

Last updated: 2026-02-02
