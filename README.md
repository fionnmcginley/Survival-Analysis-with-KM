# Survival Analysis with Kaplan-Meier and Cox Models in R

This notebook provides an introduction to survival analysis using R. It covers Kaplan-Meier survival estimation, stratified survival curves, and the Cox Proportional Hazards model, using the built-in `lung` dataset from the `survival` package.

## 📦 Packages Used

- `survival`: for survival analysis functions
- `tidyverse`: for data manipulation and plotting
- `ggsurvival`: for survival curve visualizations with ggplot2
- `ggplot2`: for customizable plots

## 📈 Analysis Overview

### 1. Kaplan-Meier Estimation
- Estimates survival probabilities over time.
- Visualized using `geom_step()` and shaded confidence intervals.

### 2. Stratified Kaplan-Meier Curves
- Stratification by sex to compare male and female survival curves.
- Uses `survfit(Surv(time, status) ~ sex, ...)`.

### 3. Cox Proportional Hazards Model
- Models the hazard function with sex (coded via a dummy variable) as a covariate.
- Survival predictions are computed for male and female separately using the fitted Cox model.

## 📝 How to Run

1. Clone the repo or download the `.Rmd` / `.nb.html` file.
2. Install required packages:
   ```r
   install.packages(c("survival", "tidyverse", "devtools"))
   devtools::install_github("nicolash2/ggsurvival", force = TRUE)
