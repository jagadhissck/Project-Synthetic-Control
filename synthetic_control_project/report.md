# Project Report — Synthetic Control for Policy Evaluation

## 1. Research question
Estimate the causal effect of a policy implemented in unit `u0` at time 60 on the outcome variable.

## 2. Data
See `data/dataset.csv` and `datasheet.md`.

## 3. Method
- Construct synthetic control as weighted average of donor units (u1..u10).
- Weights chosen to match pre-treatment outcome and optionally covariates.
- Estimate treatment effect as difference between treated unit and synthetic after t=60.

## 4. Diagnostics
- Pre-treatment RMSPE (root mean squared prediction error).
- Plot: actual vs synthetic for treated unit.
- Placebo tests: run SCM treating each donor as if treated and compare effect sizes.
- Sensitivity: remove high-correlation donors and re-estimate.

## 5. Results (instructions)
Run `analysis.ipynb` to produce numeric estimates and figures. Include discussion of:
- Pre-treatment fit quality.
- Post-treatment treatment effect trajectory and cumulative effect.
- Whether SCM assumptions are plausible.

## 6. Conclusion & Limitations
- SCM provides an interpretable counterfactual but relies on the no-interference and good donor pool assumptions.
- For full credit, report robustness checks and explicitly state limitations.