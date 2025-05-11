# Overlapp.Insight

**Overlapp.Insight** is an interactive Shiny web application designed for the statistical comparison of multiple numerical distributions, with a focus on visualizing and testing their pairwise overlaps. Originally developed for analyzing typological features in sign language datasets, it can be easily adapted for any type of numerical distribution data.

## Features

- Upload your own `.csv` file containing numerical data.
- Select any combination of variables (columns) to compare.
- Visualize **density plots** of selected distributions.
- Compute pairwise **overlapping indices** using the `overlapping` R package.
- Perform **permutation tests** to determine statistical significance.
- View results in both **tabular** and **matrix** formats.
- Real-time **progress bar** during computation.
- **Error handling** and UI feedback using `shinyjs`.
  
## Getting Started
## Example Dataset

An example CSV file is included in the [`example-data/`](example-data/) folder:

[overlapp_insight_example_data.csv](example-data/overlapp_insight_example_data.csv)

This dataset contains simulated values for several sign language distributions, intended for testing the app's functionality.

### Prerequisites

Ensure that you have R and the following packages installed:

```r
install.packages(c("shiny", "ggplot2", "readr", "dplyr", "tidyr", "overlapping", "shinyjs"))
Running the App
Clone the repository and run the app.R file in RStudio or directly from the R console:

r
Copy
Edit
shiny::runApp("path/to/Overlapp.Insight")
Alternatively, if deployed online (e.g., via shinyapps.io), access the app through your web browser.

Input Format
The app expects a .csv file where:

Each column represents a distribution (e.g., a variable or linguistic feature).

Each row is an observation.

All values must be numeric.

Missing values will be dropped automatically.

Output
Density Plot: Shows distributional shapes overlaid by group.

Pairwise Overlap Table: Includes Overlap Index, Z-observed values, and p-values.

Overlap Matrix: A square matrix summarizing overlaps among all selected variables.

Use Case Example
Overlapp.Insight has been used to analyze datasets such as:

STP13 and STP21 linguistic profiles compared against median values of older sign languages.

Longitudinal comparisons within Nicaraguan Sign Language (e.g., 2007 vs. 2017 cohorts).

Multigroup comparisons combining contemporary and historical data.

See the /examples/ folder for sample datasets and analyses.

Built With
Shiny

ggplot2

overlapping

shinyjs

Repository Structure
graphql
Copy
Edit
Overlapp.Insight/
├── app.R               # Main Shiny app
├── README.md           # This file
├── example-data/       # Sample CSV files 


Author
Developed by [Your Name or Team Name]
Affiliation / Project / Institution

License
This project is licensed under the MIT License – see the LICENSE file for details.

# References:
Pastore, M. (2018). Overlapping: a R package for estimating overlapping in empirical distributions. Journal of Open Source Software, 3(32), 1023.
Pastore, M., & Calcagnì, A. (2019). Measuring distribution similarities between samples: A distribution-free overlapping index. Frontiers in psychology, 10, 1089.
Perugini, A., Calignano, G., Nucci, M., Finos, L., & Pastore, M. (2024). How do my distributions differ? Significance testing for the Overlapping Index using Permutation Test (No. 8h4fe_v1). Center for Open Science.
