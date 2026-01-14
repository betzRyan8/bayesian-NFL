# Bayesian Modeling of NFL Betting Outcomes

## Overview
This project applies Bayesian logistic regression models to evaluate the predictive performance of 
sportsbook betting information for National Football League (NFL) games. The analysis focuses on three betting outcomes:
1. Whether the home team wins
2. Whether the betting favorite covers the spread
3. Whether the total score exceeds the over/under line

## Data
The dataset obtained from Kaggle includes team and game level information.

- Source: NFL Scores and Betting Data (Kaggle)
- Key Variables:
  - Point Spread
  - Over/Under line
  - Home team favorite indicator

Games with missing betting information were removed during preprocessing using Python.

## Methodology
All three outcomes are modeled using Bayesian logistic regression with Bernoulli likelihoods. 
Models are fit using rstanarm and sampled with MCMC via the No-U-Turn Sampler (NUTS).

- Software: R, rstanarm
- Priors: Weakly informative normal priors
- Diagnostics: Trace plots and R-hat statistics

## Model Evaluation
Model performance is evaluated using Brier scores. A baseline sportsbook probability of 0.50 is used 
across all three models for comparison.

## Results
- The Win model is the only model to demonstrate improved predictive performance over the baseline probability
- Both the Spread and Over/Under models performed similarly to the baseline

---

## Reproducibility
All data prepocessing steps were conducted in Python using the `Pandas` library.
All statistcal modeling and analysis were conducted in R using the `rstanarm` package.

## Author
**Ryan Betz**







