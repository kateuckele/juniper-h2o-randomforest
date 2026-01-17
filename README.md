# Juniper Hybrid Zone: Random Forest Ancestry Prediction (H2O)

Predict hybrid ancestry (q) from environmental and geographic predictors using a tuned Random Forest model in **H2O (DRF)**.  
This repo contains a reproducible RMarkdown workflow covering data compilation, EDA, feature engineering, model tuning, evaluation, and interpretability.

## Highlights
- End-to-end workflow: **data → EDA → feature engineering → model training**
- Hyperparameter tuning with **H2O grid search** (random discrete)
- Evaluation with **cross-validation + test set** (RMSE, R², MAE)
- Interpretability: **variable importance** + **residual diagnostics**
- Reproducible outputs saved to `outputs/`

## Repository Structure
```
.
├── juniper_h2o_rf.Rmd
├── README.md
├── data/ # input data files
└── outputs/ # generated figures/CSVs (gitignored)
```

## Requirements
- R (>= 4.1 recommended)
- Pandoc + a LaTeX distribution for PDF knitting (e.g., TinyTeX)
- R packages:
  - `h2o`, `rsample`, `dplyr`, `tidyr`, `rhdf5`, `ggplot2`, `here`

Install packages:
```r
install.packages(c("h2o","rsample","dplyr","tidyr","rhdf5","ggplot2","here"))
```

## Modeling Notes
- H2O algorithm: DRF (Distributed Random Forest)
- Tuning: random grid search with a runtime/model cap for fast iteration
- CV: 5-fold (default)




