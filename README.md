# Synthetic Control Method Analysis for France's Fertility Rate

## Overview
This notebook demonstrates the application of the Synthetic Control Method (SCM) to analyze the impact of a treatment (policy or event) on France's fertility rate. SCM is a statistical technique used to estimate the effect of an intervention by comparing the treated unit (France) to a weighted combination of control units (other countries), creating a "synthetic" version of France for comparison.

## Structure
The notebook is organized as follows:

1. **Import Libraries**  
   Loads all necessary R libraries for data manipulation, visualization, and SCM analysis.
2. **Load Data**  
   Imports fertility rate data from a Google Sheets CSV link.
3. **Data Preparation**  
   Defines the treated unit (France), donor pool (other countries), and treatment year. Prepares the data for SCM analysis.
4. **SCM Analysis**  
   Runs the synthetic control algorithm to estimate the counterfactual fertility rate for France.
5. **Results Visualization**  
   Plots the observed vs. synthetic fertility rates and the gap (treatment effect) over time.
6. **Treatment Effect Calculation**  
   Calculates the average increase in fertility rate for France after the intervention.
7. **Placebo Test**  
   Performs a placebo test by running SCM with a different treatment year to check robustness.
8. **Placebo Visualization**  
   Plots the results of the placebo test.
9. **SCM Tables and Inference**  
   Displays key tables from the SCM results and runs statistical inference using placebo tests.
10. **MSPE Analysis**  
    Calculates and visualizes the Mean Squared Prediction Error (MSPE) ratios for all units.

## How to Use
- **Run each cell sequentially** to reproduce the analysis.
- **Modify the treatment year or donor pool** to test different scenarios.
- **Review the comments in each cell** for explanations of the code and analysis steps.

## Requirements
- R (with packages: Synth, LowRankQP, dplyr, tidyverse, ggplot2, viridis, hrbrthemes, googlesheets4, skimr, kableExtra, ggthemes, stargazer, SCtools)
- Internet connection (to load data from Google Sheets)

## Output
- Plots comparing France's actual and synthetic fertility rates
- Treatment effect estimates
- Placebo test results and MSPE analysis for statistical inference