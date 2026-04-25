# Ames Housing Regression Benchmark

<p align="center">
  <strong>Advanced Regression Analysis using Manual ML, Classical Regression Models, and Ensemble Learning</strong>
</p>

<p align="center">
  A portfolio-ready machine learning project built on the <strong>Ames Housing</strong> dataset, designed to show end-to-end regression workflow, model engineering, evaluation, reporting, and comparison.
</p>

## Project Overview

This project studies house price prediction on the **House Prices: Advanced Regression Techniques** dataset from Kaggle:

- Dataset link: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques

The full workflow is organized as a sequence of notebooks, starting from raw data inspection and cleaning, then moving through feature engineering, training, validation, model saving, ensemble learning, and final benchmarking.

This repository is especially strong for a CV, higher study application, or academic portfolio because it demonstrates:

- manual implementation of linear regression with gradient descent
- classical scikit-learn regression models
- ensemble learning with boosting, bagging, stacking, and voting
- saved model artifacts for reproducibility
- report-ready visual outputs and comparison tables
- structured notebook-based experimentation

## Project Highlights

| Area | What This Project Shows |
|---|---|
| Data Work | cleaning, preprocessing, train-validation splitting, scaled features |
| Algorithm Depth | custom linear regression from scratch |
| ML Benchmarking | KNN, Linear Regression, Decision Tree, SVM, Random Forest |
| Ensemble Learning | AdaBoost, Bagging, Stacking, Voting |
| Reporting | comparison dashboard, exported PNG figures, CSV summary tables |
| Portfolio Value | strong evidence of applied ML workflow and model evaluation discipline |

## Best Validation Result

The current top model from `08_model_comparison.ipynb` is:

- **Stacking Regressor**
- **R2 Score:** `0.8877`
- **RMSE:** `0.1448`
- **MAE:** `0.0939`

These values come from the processed validation target used across the notebooks and are exported to:

- `reports/results/model_comparison_summary.csv`
- `reports/results/model_comparison_ranking.csv`

## Repository Structure

```text
Advanced-Regression-Analysis-using-Classical-ML-and-Ensemble-Techniques-Ames-Housing-Dataset-/
|
|-- README.md
|-- requirements.txt
|
|-- data/
|   |-- raw/
|   |   |-- train.csv
|   |   `-- test.csv
|   `-- processed/
|       |-- cleaned_train.csv
|       |-- cleaned_test.csv
|       |-- engineered_train.csv
|       |-- engineered_test.csv
|       |-- X_train.csv
|       |-- X_valid.csv
|       |-- X_train_scaled.csv
|       |-- X_valid_scaled.csv
|       |-- y_train.csv
|       |-- y_valid.csv
|       `-- final_test.csv
|
|-- models/
|   |-- manual_linear_regression.pkl
|   |-- knn.pkl
|   |-- linear_regression.pkl
|   |-- decision_tree.pkl
|   |-- svm.pkl
|   |-- random_forest.pkl
|   |-- boosting_model.pkl
|   |-- bagging_model.pkl
|   |-- stacking_model.pkl
|   `-- voting_model.pkl
|
|-- notebooks/
|   |-- 01_data_loading_and_overview.ipynb
|   |-- 02_data_cleaning.ipynb
|   |-- 03_feature_engineering.ipynb
|   |-- 04_train_test_split.ipynb
|   |-- 05_manual_linear_regression.ipynb
|   |-- 06_sklearn_regression_models.ipynb
|   |-- 07_ensemble_learning.ipynb
|   `-- 08_model_comparison.ipynb
|
`-- reports/
    |-- figures/
    |   |-- model_accuracy_comparison.png
    |   |-- model_comparison_dashboard.png
    |   `-- model_rmse_comparison.png
    `-- results/
        |-- model_comparison_summary.csv
        |-- model_comparison_ranking.csv
        `-- model_comparison_summary.md
```

## Notebook Roadmap

### `01_data_loading_and_overview.ipynb`

- loads the raw Ames Housing dataset
- explores the columns and initial data quality
- builds the first understanding of the regression problem

### `02_data_cleaning.ipynb`

- handles missing values
- prepares a cleaner training and testing dataset
- standardizes the base structure for later modeling

### `03_feature_engineering.ipynb`

- transforms the cleaned data into model-ready features
- creates engineered datasets for better predictive performance

### `04_train_test_split.ipynb`

- splits the processed dataset into training and validation sets
- creates scaled feature matrices used by the later notebooks

### `05_manual_linear_regression.ipynb`

- implements linear regression manually
- uses gradient descent and K-Fold validation
- evaluates with regression metrics and saves `manual_linear_regression.pkl`

### `06_sklearn_regression_models.ipynb`

- trains classical regression models
- benchmarks KNN, Linear Regression, Decision Tree, SVM, and Random Forest
- saves trained scikit-learn model files

### `07_ensemble_learning.ipynb`

- trains ensemble models
- evaluates AdaBoost, Bagging, Stacking, and Voting regressors
- saves ensemble model artifacts and comparison outputs

### `08_model_comparison.ipynb`

- loads all saved models
- compares them on the same validation dataset
- exports polished report tables and figures into `reports/`

## How To Run The Project

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd Advanced-Regression-Analysis-using-Classical-ML-and-Ensemble-Techniques-Ames-Housing-Dataset-
```

### 2. Create and activate a virtual environment

On Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

On Linux or macOS:

```bash
python -m venv .venv
source .venv/bin/activate
```

### 3. Install the required libraries

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter joblib xgboost
```

### 4. Download the dataset

Download the Kaggle competition files:

- `train.csv`
- `test.csv`

Place them inside:

- `data/raw/train.csv`
- `data/raw/test.csv`

### 5. Launch Jupyter

```bash
jupyter notebook
```

### 6. Run the notebooks in order

Run the notebooks from top to bottom in this exact sequence:

1. `01_data_loading_and_overview.ipynb`
2. `02_data_cleaning.ipynb`
3. `03_feature_engineering.ipynb`
4. `04_train_test_split.ipynb`
5. `05_manual_linear_regression.ipynb`
6. `06_sklearn_regression_models.ipynb`
7. `07_ensemble_learning.ipynb`
8. `08_model_comparison.ipynb`

### 7. Check the outputs

After running the full pipeline, review:

- `models/` for saved model files
- `reports/figures/` for exported comparison charts
- `reports/results/` for comparison tables and summary files

## Models Included

### Manual model

- Manual Linear Regression

### Classical machine learning models

- K-Nearest Neighbors
- Linear Regression
- Decision Tree Regressor
- Support Vector Regressor
- Random Forest Regressor

### Ensemble learning models

- AdaBoost Regressor
- Bagging Regressor
- Stacking Regressor
- Voting Regressor

## Evaluation Metrics

The project focuses on regression metrics, not classification metrics.

Primary metrics used:

- `R2 Score`
- `RMSE`
- `MAE`
- `Within 10% Rate`

Interpretation:

- **Higher `R2 Score` is better**
- **Lower `RMSE` is better**
- **Lower `MAE` is better**
- **Higher `Within 10% Rate` is better**

## Report Outputs

The final comparison notebook exports visual and tabular results into the report directory.

### Figures

- `reports/figures/model_comparison_dashboard.png`
- `reports/figures/model_accuracy_comparison.png`
- `reports/figures/model_rmse_comparison.png`

### Results

- `reports/results/model_comparison_summary.csv`
- `reports/results/model_comparison_ranking.csv`
- `reports/results/model_comparison_summary.md`

## Why This Project Is Valuable For Higher Study Or CV Use

This project is a strong academic and professional showcase because it combines:

- mathematical understanding through manual model implementation
- practical ML engineering with scikit-learn
- model benchmarking discipline
- reproducible artifact saving
- polished reporting outputs for presentation
- a complete end-to-end workflow from raw data to final comparison

If you are presenting this in a CV, SOP, or graduate portfolio, you can describe it as:

> Developed an end-to-end housing price regression benchmark on the Ames Housing dataset, including custom linear regression, classical regression models, ensemble methods, model serialization, and report-ready comparative analysis.

## Suggested CV Bullet

- Built an end-to-end machine learning regression benchmark on the Ames Housing dataset using manual linear regression, classical ML models, and ensemble learning, achieving a best validation `R2 Score` of `0.8877` with a Stacking Regressor and producing reusable model artifacts and report visualizations.

## Future Improvements

- add hyperparameter tuning with `GridSearchCV` or `RandomizedSearchCV`
- include cross-validation for all scikit-learn and ensemble models
- add feature importance analysis and SHAP-based interpretability
- export final Kaggle submission files automatically
- convert the notebook workflow into a Python package or pipeline script

## Author Note

This repository is structured not only as a learning project, but as a serious regression benchmarking portfolio piece. The notebook flow, saved models, and report outputs are intended to make the work easy to inspect, reproduce, and present.
