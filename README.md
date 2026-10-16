# 🚗 Used Car Price & Demand Predictor

A machine learning project designed to predict used car prices based on features like manufacturer, year, kilometers driven, fuel type, transmission, engine power, and more.

## 📊 Project Workflow
1. **EDA & Data Cleaning (`eda.py`):** Cleaning missing values, handling outliers, extracting car brands from names, and preparing `cleaned_train_data.csv`.
2. **Modeling (`modeling.py`):** Training and comparing multiple machine learning models (Linear Regression, Random Forest, XGBoost, and Stacking Regressor) using Pipelines and ColumnTransformers. The best pipeline is saved as `pipe.pkl`.
3. **Deployment (UI):** (coming soon by the team).

## 🛠️ Tech Stack
- Python, Pandas, NumPy
- Scikit-Learn, XGBoost
- Matplotlib, Seaborn
- .... (for UI)
