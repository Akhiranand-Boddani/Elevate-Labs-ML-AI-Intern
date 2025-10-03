### **_Task 8 — K-Means Clustering_**
This project demonstrates K-Means clustering for customer segmentation using the Mall Customers dataset, including elbow and silhouette analysis, cluster visualization, and cluster profiling. All steps are performed with Pandas, Matplotlib, and scikit-learn.

### **_Objective_**
- Perform unsupervised learning to identify customer segments using K-Means.
- Select optimal number of clusters with inertia (elbow) and silhouette, and describe the resulting clusters.

### **_Dataset_**
- _Kaggle:_ Mall Customers—CSV with demographics and behaviors.
- Place Mall_Customers.csv in the same folder as the notebook.

### **_Repository contents_**
_Task 8.ipynb:_ Notebook with code cells for loading, scaling, clustering, visualization, and summary reports.

### **_Steps performed_**
#### _**1. Load and preprocess**_
- Import customers data, retain numeric features, encode gender to binary if present.
- Remove non-informative identifiers (e.g., CustomerID).

#### **_2. Scaling and PCA_**
- Standardize features using StandardScaler.
- Use PCA to project data to 2D for visualization; clustering is done in full feature space.

#### **_3. Elbow and silhouette analysis_**
- For K=2 to 25, compute inertia (Sum of Squared Errors) and silhouette score.
- Select K maximizing silhouette and/or the elbow point.

#### **_4. Fit final model and label clusters_**
- Cluster full data using K-Means, assign cluster labels.
- Attach cluster assignments to customers in the original dataset.

#### **_5. Visualize clusters_**
- Plot clusters and their centers in PCA 2D projection with color coding.
- All figures are displayed within the notebook, not saved to files.

#### **_6. Evaluate and summarize_**
- Report final inertia and silhouette score.
- Show per-cluster averages of key features (income, spending, etc) for clear segment interpretation.

### **_How to run_**
- Download Mall_Customers.csv from Kaggle and place it in the working directory.
- Open Task 8.ipynb and run cells sequentially.
- Required Python packages: pandas, numpy, scikit-learn, matplotlib.

### **_Deliverables_**
- Task 8.ipynb with all code, outputs, and narrative commentary.
- No assets are saved; all plots are shown in notebook cells only.
