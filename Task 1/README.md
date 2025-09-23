### **_Task 1 — Data Cleaning & Preprocessing_**
This folder contains the complete deliverable for Internship Task 1: cleaning and preparing a raw dataset for machine learning using Python, Pandas/NumPy, and Seaborn/Matplotlib, following the provided brief.

### **_Contents_**
**Task1.ipynb:** Main notebook with all steps, plots, and saved artifacts.

**task-1.pdf:** Official task description for reference.

**dataset file:** The CSV used (e.g., titanic.csv) stored in this same folder.

**Generated outputs:** X_processed.csv, y_processed.csv (if target exists), boxplots_numeric.png, preprocessing_meta.json.

### **_Objective_**
Prepare the dataset end to end: audit schema/nulls, impute missing values, encode categorical features, scale numerical features, visualize/remove outliers, and export cleaned artifacts for downstream modeling.

### **What was done**
**_1) Inspect schema and nulls_**
Reviewed shape, data types, and per-column missing counts to determine safe imputation and encoding plans.

**_2) Impute missing values_**
_Numerical:_ Median imputation for robustness to skew/outliers (mean is viable alternative).

_Categorical:_ Most frequent category imputation to preserve valid levels.

**_3) Encode categoricals_**
One‑hot encoding with handle_unknown=ignore for nominal variables, preventing spurious order and handling unseen levels.

_**4) Scale features**_
Standardization to zero mean and unit variance via StandardScaler; normalization to available if required by models.

**_5) Outliers_**
Boxplots to visualize potential outliers using the IQR rule; optional trimming at k=1.5 with before/after row counts recorded in preprocessing_meta.json.

### **_How to run_**
Open Task1.ipynb in this folder, adjust the dataset filename at the top if needed, and run all cells; artifacts will be saved alongside the notebook in the same folder.

_Required packages:_ pandas, numpy, scikit‑learn, seaborn, matplotlib (Python 3.9+).
