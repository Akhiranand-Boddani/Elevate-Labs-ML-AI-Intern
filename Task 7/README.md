### **_Task 7 — Support Vector Machines (SVM) Classification_**
This project implements Support Vector Machines for binary classification using both linear and RBF kernels, including comprehensive cross-validation, hyperparameter tuning, and decision boundary visualization. The Breast Cancer dataset (Kaggle CSV version) is used.

### **_Objective_**
- Demonstrate SVM modeling for both linear and non-linear class separation.
- Illustrate the impact of feature scaling, kernel choice, and core parameters (C, gamma) on model performance and boundary shape.

### **_Dataset_**
- _Breast Cancer Dataset (Kaggle version):_ CSV with diagnosis (“M” = malignant, “B” = benign) as the binary target.
- Replace data.csv with the actual CSV name as required.
- _Dataset download:_ Kaggle Link (not included—please download and place CSV in this folder).

### **_Repository contents_**
Task 7.ipynb: All code, plots, and result cells (see execution flow below).

### **_Steps performed_**
#### **_1. Data loading and preprocessing_**
- Load CSV, drop identifier columns, select numeric features, encode target as 0/1.
- Split into stratified train and test sets.

#### **_2. Feature scaling_**
- Standardize all features (fit on train, transform both splits).
- _Rationale:_ SVMs are sensitive to scale, especially with RBF kernel.

#### **_3. Baseline modeling_**
- Train SVM using both linear and RBF kernels with default hyperparameters.
- Evaluate with accuracy and confusion matrices on test set.

#### **_4. Cross-validation_**
- 5-fold cross-validation for both kernels to obtain more robust performance estimates.
- Results displayed as boxplots for visual comparison.

#### **_5. Hyperparameter tuning_**
- GridSearchCV (linear: C; RBF: C and gamma) with accuracy scoring, 5-fold CV, n_jobs=-1 for multi-core.
- Best parameters and CV scores are reported and compared.

#### **_6. Final evaluation_**
- Apply best-found models to the test set.
- Show confusion matrices and produce a side-by-side accuracy bar chart comparing baseline and tuned models.

#### **_7. 2D Visualization_**
- Use PCA to reduce high-dimensional feature space to 2D for plotting.
- Train SVMs again on PC1/PC2 and plot decision boundaries as contourf overlays with colored points.

### **_How to run_**
Clone/download this folder.

### **_Key notes and constraints_**
- All figures are displayed inline only—not saved to files.
- No pipelines or custom utility functions are used for modeling or preprocessing.
- The notebook is sequence-ready; no manual intervention or helper modules required.

### **_Deliverables_**
- Task 7.ipynb with code, results, and commentary as outlined above.
- _Not included:_ raw data—place the Kaggle CSV manually in the working directory.

### **_References_**
- _Scikit-learn SVC:_ https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html

- _Breast Cancer Dataset (Kaggle):_ https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset
Download the Kaggle CSV and rename/move to “data.csv” (or update path in notebook cell 2).

Run each cell in Task7_SVM.ipynb from start to finish (Python 3.7+ required).
