Task 1 — Data Cleaning & Preprocessing
This folder contains the complete deliverable for Internship Task 1: cleaning and preparing a raw dataset for machine learning using Python, Pandas/NumPy, and Seaborn/Matplotlib, following the provided brief.

Contents
Task1.ipynb: Main notebook with all steps, plots, and saved artifacts.

task-1.pdf: Official task description for reference.

dataset file: The CSV used (e.g., titanic.csv) stored in this same folder.

Generated outputs: X_processed.csv, y_processed.csv (if target exists), boxplots_numeric.png, preprocessing_meta.json.

Objective
Prepare the dataset end to end: audit schema/nulls, impute missing values, encode categorical features, scale numerical features, visualize/remove outliers, and export cleaned artifacts for downstream modeling.

What was done
1) Inspect schema and nulls
Reviewed shape, data types, and per-column missing counts to determine safe imputation and encoding plans.

2) Impute missing values
Numerical: Median imputation for robustness to skew/outliers (mean is viable alternative).

Categorical: Most frequent category imputation to preserve valid levels.

3) Encode categoricals
One‑hot encoding with handle_unknown=ignore for nominal variables, preventing spurious order and handling unseen levels.

4) Scale features
Standardization to zero mean and unit variance via StandardScaler; normalization to available if required by models.

5) Outliers
Boxplots to visualize potential outliers using the IQR rule; optional trimming at k=1.5 with before/after row counts recorded in preprocessing_meta.json.

How to run
Open Task1.ipynb in this folder, adjust the dataset filename at the top if needed, and run all cells; artifacts will be saved alongside the notebook in the same folder.

Required packages: pandas, numpy, scikit‑learn, seaborn, matplotlib (Python 3.9+).

