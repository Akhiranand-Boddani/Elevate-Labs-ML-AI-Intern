### **_Task 6 — K-Nearest Neighbors (KNN) Classification_**
Implement KNN classification on the Kaggle Iris dataset format, normalizing features, tuning K, evaluating accuracy and confusion matrices, and visualizing decision boundaries with inline plots only.

### **_Objective_**
Understand KNN and its dependence on feature scaling, K selection, and distance-based decision regions for multi-class classification.

### **_Dataset_**
_Source:_ Kaggle Iris (CSV with columns: Id, SepalLengthCm, SepalWidthCm, PetalLengthCm, PetalWidthCm, Species).
_Requirement:_ Use the Kaggle CSV file directly.

**_What’s included_**
_Task 6.ipynb:_ End-to-end notebook with sequential cells that:

- Load the Kaggle-format CSV and drop Id.
- Encode Species labels as integers.
- Split train/test with stratification.
- Standardize features using train statistics only.
- Fit and evaluate KNN for multiple K values.
- Plot confusion matrices and decision boundaries (no saving to disk).

### **_How to run_**
Place Iris.csv in the same folder as Task 6.ipynb.

### **_Key steps_**
#### **_1) Load and prepare_**
- Drop Id, set X = [SepalLengthCm, SepalWidthCm, PetalLengthCm, PetalWidthCm], y = Species.
- Encode labels with a simple map derived from unique Species values.

#### **_2) Normalize features_**
- Standardize with mean and variance computed on the train split; transform test accordingly.
- _Rationale:_ KNN uses distances; unscaled features distort neighborhoods.

#### **_3) Train and tune K_**
- Fit KNeighborsClassifier for odd K in [1, 3, 5, …, 25].
- Report test accuracy per K and select the best.

#### **_4) Evaluate_**
- Print accuracy and show confusion matrix for baseline K and best K.
- Use ConfusionMatrixDisplay for clarity.

#### **_5) Visualize decision boundaries_**
- Plot decision regions using two informative features (PetalLengthCm vs PetalWidthCm) after scaling.
- Additionally, project all four features to 2D via PCA and plot KNN decision regions on the 2D plane.
- Plots are displayed inline only; no files are saved.

### **_Notes and constraints_**
- No custom helper functions, no pipelines, and no column transformers were used; only direct sklearn classes are instantiated inline.
- Figures are not saved to disk; all plots are shown in the notebook output cells.
- If file/column names differ from the Kaggle schema, update the path and feature list at the top cell accordingly.

### **_Deliverables_**
- Task 6.ipynb with outputs (accuracy logs, confusion matrix plots, decision boundary plots).
- Iris.csv or a README pointer to the Kaggle download link.

### **_References_**
_Task brief:_ K selection, normalization, confusion matrix evaluation, and decision boundary visualization as required.
_Dataset:_ Kaggle Iris CSV.

Open the notebook and run cells from top to bottom.

Required packages: pandas, numpy, scikit-learn, matplotlib.
