### **_Task 3 — Linear Regression_**
This folder contains the complete deliverable for Task 3: implementing and understanding simple & multiple linear regression for house price prediction using scikit-learn, Pandas, and Matplotlib.

### **_Objective_**
Build multiple linear regression models to predict house prices, evaluate performance using MAE, MSE, and R², and interpret regression coefficients with visualizations.

### **_Dataset_**
Housing Price Prediction dataset with features including area, bedrooms, bathrooms, stories, and categorical variables like mainroad, guestroom, basement, hotwaterheating, airconditioning, parking, prefarea, and furnishingstatus.

### **_Repository Structure_**
_Task3.ipynb:_ Main notebook with complete linear regression implementation
_housing.csv:_ Housing dataset used for price prediction
_README.md:_ This documentation file

### **_Implementation Steps_**
**_1) Data Preprocessing_**
- Selected 12 features: area, bedrooms, bathrooms, stories (numeric) plus 8 categorical variables
- Applied one-hot encoding to categorical features with drop_first=True to avoid multicollinearity
-Standardized numeric features only while preserving binary dummy variables

**_2) Model Training_**
- Split data into 80% training and 20% testing sets with random_state=42
- Fitted LinearRegression model from sklearn.linear_model on preprocessed training data
- Generated predictions for both training and testing sets

**_3) Model Evaluation_**
_Training Performance:_ MAE, MSE, and R² calculated using sklearn.metrics functions
_Testing Performance:_ Same metrics computed on held-out test set to assess generalization
_Coefficient Analysis:_ Interpreted feature importance through regression coefficients sorted by absolute magnitude

**_4) Visualizations_**
_Predicted vs Actual:_ Scatter plot with ideal diagonal line to assess prediction accuracy
_Residuals Distribution:_ Histogram with KDE to check normality assumptions
_Residuals vs Predicted:_ Scatter plot to detect heteroscedasticity patterns

### **_Key Results_**
- Multiple linear regression successfully predicts house prices using combined numeric and categorical features
- Model performance evaluated through standard regression metrics without custom functions
- Coefficient interpretation reveals most influential features for price prediction

### **_Technical Approach_**
_No Custom Functions:_ Used only built-in scikit-learn metrics and preprocessing methods
_Simple Implementation:_ Avoided ColumnTransformers and Pipelines for clarity and direct control
_Inline Visualization:_ All plots displayed with plt.show() without saving to disk

### **_How to Run_**
- Place housing dataset as housing.csv in the same folder
- Open Task3.ipynb and run all cells sequentially
_Required packages:_ pandas, numpy, scikit-learn, seaborn, matplotlib
