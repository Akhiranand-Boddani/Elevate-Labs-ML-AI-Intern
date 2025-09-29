### **_Task 5 — Decision Trees and Random Forests_**
Complete implementation of tree-based models for binary classification using the Heart Disease Dataset, covering decision tree visualization, overfitting control, random forest comparison, feature importance analysis, and cross-validation evaluation.

### **_Objective_**
Learn tree-based models for classification and regression using scikit-learn and Graphviz, analyzing overfitting behavior, ensemble improvements, and feature interpretability.

### **_Dataset_**
_Name:_ Heart Disease Dataset from Kaggle

_Source:_ https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset

_Target:_ Binary classification (1 = heart disease present, 0 = no disease)

_Features:_ 13 numeric/categorical features including age, sex, chest pain type, blood pressure, cholesterol, etc.

### **_Contents_**
_Task5.ipynb:_ Complete notebook with all steps, visualizations, and analysis

_README.md:_ This documentation file

### **_Implementation Steps_**
#### **_1) Decision Tree Training and Visualization_**
- Trained DecisionTreeClassifier with default parameters to observe baseline performance
- Visualized complete tree structure using sklearn.tree.plot_tree with feature names and class labels
- Generated classification report and confusion matrix for initial assessment

#### **_2) Overfitting Analysis and Depth Control_**
- Swept max_depth from 1 to 15 to analyze training vs test accuracy curves
- Identified optimal depth based on test set performance to prevent overfitting
- Retrained decision tree with best max_depth and visualized pruned structure
- Compared metrics between unconstrained and depth-limited trees

#### **_3) Random Forest Training and Comparison_**
- Trained RandomForestClassifier with 300 estimators and no depth limit
- Compared accuracy and F1-score against tuned decision tree
- Generated detailed classification reports for both models
- Analyzed ensemble effect on generalization performance

#### **_4) Feature Importance Interpretation_**
- Extracted feature_importances_ from both decision tree and random forest models
- Created bar plots comparing importance rankings between single tree and ensemble
- Identified most predictive features for heart disease classification
- Discussed differences in importance scores between tree-based methods

#### **_5) Cross-Validation Evaluation_**
- Implemented 5-fold StratifiedKFold cross-validation for robust performance estimation
- Evaluated both tuned decision tree and random forest using cross_val_score
- Reported mean and standard deviation of CV accuracy scores
- Compared model stability across different data splits

### **_Key Results_**
_Decision Tree (tuned):_ Achieved optimal performance at max_depth=[determined from analysis]
_Random Forest:_ Demonstrated improved generalization through ensemble averaging
_Feature Importance:_ Identified top predictive features with consistent rankings across methods
_Cross-Validation:_ Confirmed model performance with confidence intervals

### **_Tools and Libraries_**
_Python 3.9+_
_scikit-learn:_ DecisionTreeClassifier, RandomForestClassifier, model evaluation
_matplotlib/seaborn:_ Visualization and plotting
_pandas/numpy:_ Data manipulation and analysis
_Optional:_ graphviz for enhanced tree visualization (system install + Python package)

### **_How to Run_**
- Download heart.csv from the Kaggle dataset link and place in the same folder
- Install required packages: pandas, numpy, scikit-learn, matplotlib, seaborn
- Run Task5.ipynb cell by cell to reproduce all analysis and visualizations
- All plots display inline; no files are saved to disk per task requirements

### **_Design Choices_**
- No custom functions or pipelines used; pure scikit-learn API calls throughout
- Stratified train-test split to preserve class balance in both sets
- StratifiedKFold for cross-validation to maintain class proportions across folds
- Inline plotting only; no figure saving to focus on interactive analysis
- Random state fixed at 42 for reproducible results across runs

### **_Model Interpretation_**
- Decision trees provide interpretable rules through node splits and feature thresholds
- Random forests aggregate multiple trees to reduce variance and improve stability
- Feature importance scores indicate which variables contribute most to classification decisions
- Cross-validation ensures reported performance generalizes beyond the specific train-test split

**_This implementation demonstrates the progression from single decision trees to ensemble methods, highlighting the bias-variance tradeoff and the value of feature importance for model interpretability in healthcare prediction tasks._**
