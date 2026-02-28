# Effects of Marijuana Legalization on Usage Rates: A Difference-in-Differences Analysis

## Project Summary

This project looks at how legalizing recreational marijuana actually impacted usage rates across the U.S. using a difference-in-differences approach. By pulling in SAMHSA survey data and Census stats, the analysis compares early-adopting states like Colorado, Washington, and Oregon against a group of similar states where it stayed illegal. On top of measuring the direct impact of the law, I also built a LASSO regression model to help predict usage trends based on those same state-level factors. The whole analysis was written in R and formatted using Quarto.

## Research Question

Did recreational marijuana legalization increase usage rates among the general adult population and among teenagers, and how large were those effects?

## Key Findings

- Legalization is associated with a **5.89 percentage point increase** in past-year marijuana use among individuals aged 12 and older — a highly significant effect (p < 0.001) that represents the core causal estimate.
- **Teen usage (ages 12–17) did not increase significantly** following legalization (0.36 pp increase, p = 0.265), a counterintuitive finding suggesting that legalization did not meaningfully increase usage rates for teens.
- Pre-legalization parallel trends between treated and control states hold from 2005–2013, supporting the validity of the DiD design.
- Counterfactual analysis shows divergence beginning in the early 2010s in Colorado and Oregon, consistent with anticipatory or gradual cultural effects preceding formal legalization.
- The LASSO predictive model achieves an evaluation RMSE of 0.012, with 10-fold cross-validation selecting an optimal lambda of 0.019.

## Tools & Methods

**Language:** R
**Packages:** tidyverse, ggplot2, dplyr, lmtest, sandwich, broom, glmnet, readxl
**Methods:** Difference-in-differences with state and year fixed effects, interaction modeling (Treated × Post), robust standard errors, parallel trends verification, LASSO regression with 10-fold cross-validation, counterfactual trajectory analysis
**Data:** SAMHSA National Survey on Drug Use and Health (usage rates by state/age group), Census Bureau (poverty rates, median income, state populations)

## Rendered Report

The full analysis — including state-level usage trajectories, parallel trends plots, counterfactual comparisons, teen usage trends, and regression output — is best viewed in the rendered HTML report:

**[Full Analysis with Code](docs/analysis.html)**
**[Clean Report (no code)](docs/analysisnocode.html)**
