# Stroke Prediction Using XGBoost and Logistic Regression

## About
This project develops and compares machine learning models to classify stroke occurrence using patient health and demographic data. XGBoost is optimized using GridSearchCV, while Logistic Regression serves as a baseline model. Model performance is evaluated using classification metrics and ROC curves.

## Data
- **Dataset:** Stroke prediction dataset (`smote3.test.csv`)
- **Target Variable:** `stroke` (stroke occurrence)
- **Data Type:** Structured patient data
- **Features:** Patient demographic and health-related variables, including age, hypertension, heart disease, average glucose level, BMI, and other available predictors
- **Preprocessing:** Missing-value handling, BMI type conversion, and feature standardization

## Methods
1. **Data Preparation** — Load the dataset, replace `"N/A"` values with missing values, convert BMI to numeric format, remove incomplete observations, and drop the unnecessary index column.
2. **Data Splitting** — Divide the dataset into training and testing sets using an 80:20 ratio. A validation set is also prepared for XGBoost.
3. **Feature Scaling** — Standardize numerical predictors using `StandardScaler`.
4. **XGBoost Modeling** — Train an XGBoost classifier and optimize its hyperparameters using `GridSearchCV` with five-fold cross-validation and ROC-AUC as the selection metric.
5. **Logistic Regression Modeling** — Build a Logistic Regression classifier as a baseline for comparison.
6. **Model Evaluation** — Evaluate training and test performance using confusion matrices, accuracy, sensitivity (recall), classification reports, and ROC-AUC.
7. **Feature Importance Analysis** — Examine XGBoost feature importance and Logistic Regression coefficients to identify influential predictors.
8. **Model Comparison** — Compare the ROC curves and AUC values of both models on the test set.

## Author
**Sandra Berliana Putri** - Statistics and Data Science graduate from IPB University, interested in statistical modeling and machine learning.
