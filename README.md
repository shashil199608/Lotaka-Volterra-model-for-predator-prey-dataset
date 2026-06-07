# GP-Assisted ABC SMC for the Lotka–Volterra Predator–Prey Model

This repository contains the Python implementation developed for the Master's thesis:

**Predictive Distance Weighting in Surrogate-Assisted ABC SMC: A Comparative Study of Predictive Distance Weighting Strategies in Importance Sampling of ABC SMC**

## Overview

This project investigates predictive distance weighting strategies within a Gaussian Process (GP)-assisted Approximate Bayesian Computation Sequential Monte Carlo (ABC SMC) framework.

A Gaussian Process surrogate model is used to approximate discrepancy values between simulated and observed data and to guide the importance weighting stage of ABC SMC.

The methodology is evaluated using a Lotka–Volterra predator–prey model fitted to the historical Lynx–Hare population dataset.

## Weighting Strategies

The following weighting strategies are implemented and compared:

- Traditional Weighting
- Mean-Based Weighting
- Probabilistic Weighting
- Annealing Weighting

## Model

The Lotka–Volterra predator–prey system is represented by a nonlinear system of ordinary differential equations (ODEs) describing the interaction between prey (hare) and predator (lynx) populations.

The parameters estimated are:

- **a** – Predation rate
- **d** – Predator mortality rate
- **r** – Prey growth rate

The remaining model parameters are fixed throughout the experiments.

## Methodology

The implementation combines:

- Approximate Bayesian Computation (ABC)
- Sequential Monte Carlo (SMC)
- Gaussian Process (GP) surrogate modelling
- Adaptive threshold selection
- Importance weighting based on predictive discrepancy information

## Outputs

The code generates:

### Diagnostic Plots

- Acceptance Rate vs Iteration
- Threshold Evolution vs Iteration
- Cumulative Simulations vs Iteration

### Posterior Analysis

- Weighted Posterior Contour Plots
- Posterior Means
- 95% Credible Intervals
- Posterior Standard Deviations
- Acceptance Rates
- Total Simulator Evaluations

## Dataset

Historical Lynx–Hare population data are used for parameter inference.

Source:

D. R. Hundley, Whitman College Predator–Prey Dataset

## Software Requirements

Python 3.x

Required packages:

- numpy
- pandas
- scipy
- matplotlib
- seaborn
- scikit-learn

Install dependencies using:

```bash
pip install numpy pandas scipy matplotlib seaborn scikit-learn
```

## Running the Code

Execute:

```bash
python lotka_volterra_gp_assisted_abc_smc.py
```

The script will:

1. Load the Lynx–Hare dataset.
2. Run GP-assisted ABC SMC inference.
3. Compare four weighting strategies.
4. Generate diagnostic plots.
5. Produce weighted posterior summaries.

## Thesis Information

This implementation was developed as part of a Master of Science Thesis in Statistical Data Analytics at Tampere University.

## Author

**Shashikala Lankadari**

Faculty of Information Technology and Communication Sciences  
Tampere University
