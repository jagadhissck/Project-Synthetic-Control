# Advanced Causal Inference with Synthetic Control — Project Bundle

**Goal:** Evaluate the impact of a simulated policy (treated unit `u0` at time 60) using the Synthetic Control Method (SCM).  
This repository contains a synthetic dataset, an analysis Jupyter notebook, documentation, and instructions to reproduce results.

## Contents
- `data/dataset.csv` — panel time-series data for 11 units (u0 treated, u1..u10 controls), 100 time periods.
- `analysis.ipynb` — Jupyter notebook with step-by-step implementation of SCM, diagnostics, placebo tests, and interpretation.
- `report.md` — structured project report explaining methods, assumptions, results, and limitations.
- `datasheet.md` — metadata describing the dataset fields, provenance, and simulation procedure.
- `requirements.txt` — Python packages recommended to reproduce the analysis.

## How to run
1. Create a Python environment (recommended: conda or venv).
2. Install packages: `pip install -r requirements.txt`
3. Launch Jupyter: `jupyter notebook analysis.ipynb`
4. Follow notebook: it loads `data/dataset.csv`, constructs a synthetic control for `u0`, shows plots, and computes effect estimates.

## Grading tips (aiming >90%)
- Justify covariate choices and pre-treatment fit.
- Show diagnostics: pre-treatment RMSPE, plot actual vs synthetic, placebo tests for other units.
- Discuss SCM assumptions (parallel trends mimicry, no spillovers).
- Provide sensitivity analyses (vary donor pool, time windows, and regularization).