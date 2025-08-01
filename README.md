This repository contains statistical analysis projects completed as part of the STAT2402 (Analysis of Observations) course at the University of Western Australia. The projects apply advanced regression and statistical modeling to real-world healthcare datasets, with full technical documentation and reproducible R code.

## Table of Contents

* [Project 1: Predicting Low Birth Weight Using Logistic Regression](#project-1-predicting-low-birth-weight-using-logistic-regression)
* [Project 2: Analysis of Patient Complaints Among Emergency Department Doctors](#project-2-analysis-of-patient-complaints-among-emergency-department-doctors)
* [Data](#data)
* [How to Run](#how-to-run)
* [License](#license)
* [References](#references)

---

## Project 1: Predicting Low Birth Weight Using Logistic Regression

**Report:** `STAT Predicting Low Birth Weight Using Logistic Regression and Variable Selection Techniques.pdf`

This project investigates the relationship between maternal factors and the probability of low birth weight (LBW, <2.5kg) in newborns. Using a logistic regression framework and variable selection techniques (AIC, backward and forward selection), significant predictors are identified, including:

* Maternal weight at last menstrual period (negative effect on LBW risk)
* Previous premature labor
* Hypertension during pregnancy
* Maternal race (Black vs. White)
* Smoking status during pregnancy
* Uterine irritability

Outliers were assessed and retained for their informative value. Model diagnostics were performed to validate fit and robustness.

**Key methods:**

* Logistic regression with interaction terms
* Variable selection (AIC, stepwise)
* Model diagnostics (residuals, Cook's distance, leverage)
* Statistical inference (Wald test, Pearson Chi-Square)

## Project 2: Analysis of Patient Complaints Among Emergency Department Doctors

**Report:** `STAT An Observational Analysis of Patient Complaints Among Emergency.pdf`
**R Markdown:** `STAT An Observational Analysis of Patient Complaints Among Emergency.Rmd`

This study models the count of patient complaints against emergency doctors in a hospital, seeking to identify influential doctor-level factors. Four count regression models were evaluated: Poisson, Negative Binomial (NB), Zero-Inflated Poisson (ZIP), and Zero-Inflated Negative Binomial (ZINB). Model selection used AIC and Vuong’s tests.

**Key findings:**

* The ZIP model provided the best fit, handling both over-dispersion and excess zeros.
* Number of patient visits (positive effect) and doctor’s hourly income (negative effect) were significant predictors of complaint counts.
* Gender, residency training, and total working hours were not significant.
* The zero-inflation component was not explained by any included variables.

**Key methods:**

* EDA (summary stats, correlation, histograms)
* Model fitting: Poisson, NB, ZIP, ZINB
* Model selection: AIC, Vuong’s test
* Model diagnostics

## Data

* **birthweight.csv**: Maternal and newborn records for Project 1.
* **compdat.txt**: Demographic and complaint data for Project 2.

Both datasets have been de-identified for privacy and are suitable for educational use.

## How to Run

1. Clone this repository.
2. Open the `.Rmd` or `.pdf` report for each project for technical details and code.
3. Data files (`birthweight.csv`, `compdat.txt`) can be loaded directly in R.
4. Required R packages: `MASS`, `pscl`, `corrplot`, `ggplot2`, `dplyr`, etc.
   See report appendices for specific code and package use.

## License

See `LICENSE` for usage terms.

## References

A full list of references for all models and datasets is provided in each report.cific code blocks added to this README, please specify.
