# Hierarchical Microscopy Data Analysis with Python

**A reproducible scientific data science project exploring statistical inference, pseudoreplication and experimental design using simulated fluorescence lifetime imaging microscopy (FLIM) data.**

## Project Overview

Microscopy experiments often collect measurements from multiple cells within images, across conditions and independent biological experiments. These observations are not necessarily statistically independent.

This project investigates how hierarchical data structures affect statistical inference and evaluates alternative approaches to analysing treatment effects.

The workflow combines exploratory data analysis, statistical modelling, Monte Carlo simulation and data visualisation.

## Objectives

- Generate realistic hierarchical synthetic microscopy datasets.
- Explore dose- and time-dependent fluorescence lifetime changes.
- Demonstrate the consequences of pseudoreplication.
- Compare cell-level, image-level and experiment-level statistical analyses.
- Implement mixed-effects models with random intercepts and slopes.
- Evaluate statistical power, false-positive rates and confidence-interval coverage.
- Investigate how experimental design affects statistical reliability.

## Tools and Technologies

**Python:** NumPy, pandas, SciPy, Matplotlib, Seaborn, statsmodels

**Methods:** Exploratory data analysis, hypothesis testing, linear mixed-effects modelling, Monte Carlo simulation, model diagnostics and experimental-design evaluation.

**Environment:** Jupyter Notebook

## Methodology

### 1. Synthetic data generation

Simulated fluorescence lifetime measurements were generated across independent experiments, exposure conditions, microscopy images and individual cells.

The simulation incorporated hierarchical sources of variability and dose- and time-dependent treatment effects.

### 2. Exploratory data analysis

Data were summarised at cell, image and experiment levels to examine treatment effects, distributions and between-experiment variability.

### 3. Pseudoreplication

Naive cell-level statistical tests were compared with analyses accounting for the experimental hierarchy.

### 4. Mixed-effects modelling

Random-intercept and random-slope mixed-effects models were used to estimate treatment effects while accounting for experimental variation.

### 5. Monte Carlo validation

Repeated simulated experiments were used to evaluate estimator bias, confidence-interval coverage, false-positive rates and fitting stability.

### 6. Experimental-design evaluation

Alternative sampling strategies were compared, including collecting more cells, more images or more independent experiments.

## Key Findings

- Ignoring hierarchical dependence can produce overly narrow confidence intervals and inflated false-positive rates.
- Increasing cell counts does not necessarily compensate for limited independent biological replication.
- Random-intercept models may underestimate uncertainty when treatment responses differ between experiments.
- Random-slope models can represent biological heterogeneity but may be unstable with small numbers of experiments.
- Experiment-level paired analyses provide a useful statistical benchmark for balanced paired designs.

## Limitations

All datasets are simulated, and their parameters are illustrative rather than experimentally calibrated. Monte Carlo results depend on the specified simulation assumptions and number of repetitions. The final random-slope validation used a small pilot simulation, so its performance estimates are exploratory.

## Reproducibility

The Jupyter notebook contains the simulation procedures, analysis code, statistical comparisons and visualisations. Random seeds are specified to support reproducibility.

## Project Context

This independent portfolio project draws on analytical challenges encountered in fluorescence lifetime microscopy and experimental biophysics. It demonstrates transferable skills in Python programming, scientific data analysis, statistical modelling and research reproducibility.

**All reported findings are from synthetic data and should not be interpreted as experimental biological results.**