# EEG Functional Data Analysis: Thesis Code Repository

This repository contains all R Markdown (`.Rmd`) files used in our thesis:  
**"Functional Data Analysis of EEG Data: Comparing Alcoholics and Controls"**

The project applies Functional Principal Component Analysis (FPCA), clustering, and predictive modelling to EEG data collected from alcoholic and control participants.
This codebase was developed by Aoife O'Brien and Alannah Blacoe as part of the MSc in Health Data Science thesis project (2025), supervised by Andrew Simpkin.
---

## File Overview

### **Preprocessing & Visualisation**
- `1_datacleaning.Rmd` – Loads and reshapes raw EEG data.
- `2_plots.Rmd` – Exploratory plots of raw EEG signals.
- `3_permutation.Rmd` – Permutation testing to check for structure in EEG data.

### **FPCA**
- `4.1_pca.Rmd` – General PCA process.
- `4.2_pca_plots.Rmd` – Scree plots, mean function, and eigenfunctions.
- `4.3_pca_bspline.Rmd` – FPCA using B-spline basis functions.
- `4.4_pca_fourier.Rmd` – FPCA using Fourier basis (used in final models).

### **Modelling**
- `6_matchingconditionmodel.Rmd` – Predicts stimulus matching condition using FPCA scores (multinomial, RF, LASSO).
- `7_subjectidentifiermodel.Rmd` – Attempts to classify subject ID based on EEG response.

### **Tuning & Comparison**
- `8_nharm_comparison.Rmd` – Evaluates model accuracy across number of harmonics and basis types.
- `9_clustering.Rmd` – Performs clustering on FPCA scores and visualises EEG patterns by cluster.

---

##  Required Packages

This project uses the following R packages:

- `tidyverse`
- `fda`, `fda.usc`
- `nnet`
- `randomForest`
- `glmnet`
- `caret`
- `knitr`, `rmarkdown`

Install all at once with:

```r
install.packages(c("tidyverse", "fda", "fda.usc", "nnet", "randomForest", "glmnet", "caret", "knitr", "rmarkdown"))
