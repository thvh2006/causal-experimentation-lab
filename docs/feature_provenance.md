# Feature provenance and decision-time policy

This register explains where portfolio-facing features come from and what was known at the decision point. The machine-readable source is [`reports/feature_provenance.csv`](../reports/feature_provenance.csv).

| Feature | Family | Raw source | Transformation | Cutoff | Fit scope | Role | Main risk |
|---|---|---|---|---|---|---|---|
| f0 | pre-treatment covariate | Criteo uplift source column f0 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f1 | pre-treatment covariate | Criteo uplift source column f1 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f2 | pre-treatment covariate | Criteo uplift source column f2 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f3 | pre-treatment covariate | Criteo uplift source column f3 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f4 | pre-treatment covariate | Criteo uplift source column f4 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f5 | pre-treatment covariate | Criteo uplift source column f5 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f6 | pre-treatment covariate | Criteo uplift source column f6 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f7 | pre-treatment covariate | Criteo uplift source column f7 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f8 | pre-treatment covariate | Criteo uplift source column f8 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f9 | pre-treatment covariate | Criteo uplift source column f9 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f10 | pre-treatment covariate | Criteo uplift source column f10 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| f11 | pre-treatment covariate | Criteo uplift source column f11 | No invented semantic transformation; numeric value supplied by source | Measured before randomized assignment | none | T-learner outcome model | low: pre-treatment source covariate |
| predicted_uplift | model output | treatment and control outcome models | P(visit/X,T=1) - P(visit/X,T=0) | Models trained before holdout scoring | development split | evaluation/ranking only | medium: individual treatment effect is not observed |

## Governance rules

1. Outcomes and post-decision events are targets or evaluation evidence, never predictors.
2. Learned bins, imputers, encoders, cutoffs, and feature eligibility are fitted before locked evaluation.
3. Anonymous fields are described by source and statistical behavior; business meanings are not invented.
4. Proxy and fairness risks remain explicit even when protected attributes are unavailable.
5. The notebook is explanatory; reusable code and tests remain the implementation source of truth.
