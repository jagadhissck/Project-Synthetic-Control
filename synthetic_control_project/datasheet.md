# Datasheet for dataset.csv

**Overview**
- Synthetic panel dataset for SCM demonstration.
- 11 units (u0..u10), 100 time periods (0..99).
- Unit `u0` receives a simulated policy at time 60.

**Fields**
- `unit` : string — unit identifier (u0 is treated)
- `time` : integer — time period index
- `outcome` : float — simulated outcome variable (e.g., GDP per capita or index)
- `cov_gdp` : float — simulated time-varying covariate (proxy for economic level)
- `cov_unemp` : float — simulated time-varying covariate (proxy for unemployment)
- `treated` : 0/1 — indicator set to 1 for treated unit after intervention

**Generation process**
- Each unit's outcome is the sum of: unit-level intercept, linear trend, seasonal component, and Gaussian noise.
- Treated unit has an added positive treatment effect starting at t=60.
- Covariates follow simple linear trends plus noise.

**Limitations**
- Synthetic data — results are illustrative, not real-world causal claims.
- No measurement error beyond Gaussian noise; no spillovers modeled.