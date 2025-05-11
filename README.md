# Overlapp.Insight

# Distribution Overlapping Visualizer

This Shiny web application visualizes and compares the empirical distributions of variables using the **Overlapping Index (η)** and its complement **ζ (1 - η)**. It also performs permutation-based significance testing (`ζ-Overlapping Test`) to assess whether distributions differ statistically without relying on strong parametric assumptions.

references:
Perugini, A., Calignano, G., Nucci, M., Finos, L., & Pastore, M. (2024). How do my distributions differ? Significance testing for the Overlapping Index using Permutation Test (No. 8h4fe_v1). Center for Open Science.
Pastore, M., & Calcagnì, A. (2019). Measuring distribution similarities between samples: A distribution-free overlapping index. Frontiers in psychology, 10, 1089.
Pastore, M. (2018). Overlapping: a R package for estimating overlapping in empirical distributions. Journal of Open Source Software, 3(32), 1023.


## Features

- Upload a CSV file and select numeric variables
- Visualize distributions via density plots
- Compute the Overlapping Index (η) for each pair
- Estimate the area of non-overlap (ζ = 1 − η)
- Perform permutation-based significance testing to obtain p-values
- Display overlapping matrix and detailed comparison table

---

## Requirements

### R (version ≥ 4.0.0)
Make sure R is installed: https://cran.r-project.org/

### Required R Packages

```r
install.packages(c(
  "shiny", "ggplot2", "readr", "dplyr", "tidyr", "overlapping"
))
