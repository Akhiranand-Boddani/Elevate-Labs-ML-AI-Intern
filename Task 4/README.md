### **_Task 4 — Logistic Regression Classification_**
Binary classifier using Logistic Regression on a two‑class dataset with train/test split, standardization, evaluation via confusion matrix, precision, recall, ROC‑AUC, threshold tuning, and a brief sigmoid explanation.

### **_Dataset_**
_Suggested:_ Breast Cancer Wisconsin (Diagnostic) dataset from scikit‑learn or Kaggle CSV version linked in the task brief (Malignant vs Benign).

_Target convention in sklearn loader:_ 0 = malignant, 1 = benign; confirm when using Kaggle CSV by reading the data dictionary.

### **_Constraints_**
- No custom functions defined in the notebook.
- No pipelines and no column transformers; use direct fit/transform calls.
- Do not save figures; only display plots inline with matplotlib.

### **_What the notebook does_**
- Loads the binary dataset into X, y and prints basic shape and class balance for context.
- Splits into train/test with stratification to preserve class ratios.
- Standardizes features using StandardScaler fitted on train, applied to test.
- Fits LogisticRegression with sufficient max_iter for convergence (e.g., 2000).

### **_Evaluates:_**

- Confusion matrix and classification report.
- Precision, recall, and ROC‑AUC.
- ROC curve and Precision‑Recall curve displayed inline.

### **_Threshold tuning:_**

- Sweeps thresholds (e.g., 0.1 to 0.9) and prints precision/recall pairs.
- Selects a threshold by approximate F1 computed inline (no helper functions) and compares confusion matrices at 0.5 vs the tuned threshold.

### **_How to run_**
_Requirements:_ Python 3.9+, scikit‑learn, pandas, matplotlib.

### **_Notes and rationale_**
-Standardization is applied because Logistic Regression optimizes a convex log‑loss with L2 regularization and benefits from features on comparable scales.
- Threshold tuning shows the precision‑recall trade‑off; for medical screening, higher recall may be preferred to reduce false negatives, accepting more false positives if necessary.
- No custom functions/pipelines ensures transparency of each step for interview‑style review and aligns with the task constraints.
