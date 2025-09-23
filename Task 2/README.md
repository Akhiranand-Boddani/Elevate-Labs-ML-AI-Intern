### **_Task 2 — Exploratory Data Analysis (EDA)_**
Exploratory Data Analysis to understand the dataset using summary statistics and visualizations with Pandas, Matplotlib, Seaborn, and Plotly, aligned to the internship brief.

### **_Objective_**
Generate descriptive statistics, visualize distributions, examine feature relationships, identify patterns/anomalies, and write brief feature-level inferences. Plots are displayed only and not saved.

### **_Contents_**
_Task2.ipynb:_ Single notebook with all EDA steps and inline plots. No extra files or images are written to disk.

_Dataset:_ CSV located alongside the notebook (update the path in the first cell if different).

### **_Steps performed_**
_Summary statistics:_ mean, median, std, quartiles, min/max via pandas describe and custom metrics.

_Univariate plots:_ histograms with KDE and boxplots for numeric features to assess spread and outliers.

_Categorical exploration:_ bar plots for top categories per column.

_Relationships:_ numeric correlation heatmap and a sampled pairplot for up to 5 numeric columns for clarity.

_Interactive check:_ optional Plotly scatter to inspect relationships by category.

_Inferences:_ short printed notes on skewed features, high-missing columns, and top correlated pairs.

### **_How to run_**
Open Task2.ipynb in this folder, set DATA_PATH to the dataset filename (e.g., titanic.csv), and run all cells.

_Requirements:_ Python 3.9+, pandas, numpy, seaborn, matplotlib, plotly. Example install:

pip install pandas numpy seaborn matplotlib plotly

_Note:_ The notebook displays plots in-line; it does not save figures or other files.
