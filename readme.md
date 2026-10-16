# 🚗 Used Car Price & Demand Predictor

An end-to-end Machine Learning project focused on analyzing used car market trends, predicting resale prices, and identifying key drivers behind vehicle valuation and market demand. This project covers the full data lifecycle—from extensive exploratory data analysis and rigorous cleaning to feature engineering and multi-model evaluation.

---

## 🌟 Key Features

* **Advanced Price Estimation:** Leverages machine learning models to forecast market values based on vehicle specifications, age, mileage, and condition.
* **In-Depth EDA & Insights:** Comprehensive visual analysis uncovering non-linear depreciation patterns, brand equity value, and mileage thresholds.
* **Comprehensive Data Pipeline:** Multi-step pipeline that cleans noisy real-world data, handles missing values, removes statistical outliers, and encodes categorical attributes.
* **Model Benchmarking:** Comparison across diverse regression algorithms to select the best-performing model based on evaluation metrics.

---

## 🛠️ Tech Stack & Libraries

* **Programming Language:** Python 3.x
* **Data Manipulation & Cleaning:** `Pandas`, `NumPy`
* **Exploratory Data Analysis & Visualization:** `Matplotlib`, `Seaborn`, `Plotly`
* **Machine Learning & Preprocessing:** `Scikit-Learn`, `XGBoost`, `LightGBM`
* **Development Environment:** Jupyter Notebooks / Google Colab

---

## 📂 Project Structure

```text
Used-Car-Price-Demand-Predictor/
│
├── data/                  # Raw and cleaned datasets
├── notebooks/             # Exploratory Data Analysis & Modeling Notebooks
├── src/                   # Pipeline modules (preprocessing, training, evaluation)
├── models/                # Serialized trained model checkpoints (.pkl)
└── README.md              # Project documentation
```

---

## 🧹 Data Preprocessing & Cleaning Pipeline

Real-world used car listing data contains significant noise, missing records, and anomalies. The following preprocessing steps were applied:

1. **Handling Missing Values:**
   * Numerical features (e.g., engine size, mileage) imputed using median values grouped by vehicle brand and year.
   * Categorical features (e.g., fuel type, transmission) imputed using mode values based on vehicle segment.

2. **Outlier Detection & Removal:**
   * Used Interquartile Range (IQR) filtering and domain thresholding to prune unrealistic listings (e.g., zero prices, extreme mileage outliers exceeding physical limits, or incorrect production years).

3. **Text Cleaning & Normalization:**
   * Extracted and standardized manufacturer names and vehicle models from unstructured title strings.
   * Unified engine capacities (converting displacement metrics to standard CC/Liter units).

4. **Feature Engineering:**
   * **Vehicle Age:** Derived directly from the manufacturing year relative to the dataset collection period.
   * **Mileage per Year:** Quantified annual usage intensity ($\text{Total Mileage} / \text{Vehicle Age}$) to distinguish heavily driven cars from well-maintained low-mileage cars.
   * **Brand Tier Categorization:** Grouped vehicle makes into Budget, Mid-Range, and Luxury tiers to help models capture brand premium effects.

5. **Encoding & Scaling:**
   * Applied **One-Hot Encoding** to low-cardinality categorical attributes (e.g., Fuel Type, Transmission).
   * Applied **Target/Frequency Encoding** to high-cardinality attributes (e.g., Car Model).
   * Standardized numerical continuous features using `StandardScaler` to optimize distance-based and gradient-based algorithms.

---

## 📊 Dataset & Feature Overview

The processed dataset includes key structural features used across the training pipeline:

| Feature Name | Type | Description |
| :--- | :--- | :--- |
| **Brand & Model** | Categorical | Manufacturer and specific vehicle model name |
| **Manufacturing Year** | Numerical | Production year used to derive vehicle age |
| **Mileage** | Numerical | Total accumulated distance driven |
| **Engine Capacity (CC)** | Numerical | Engine displacement in cubic centimeters |
| **Fuel Type** | Categorical | Gasoline, Diesel, Hybrid, Electric |
| **Transmission** | Categorical | Manual or Automatic transmission type |
| **Condition / Owner Rank** | Categorical | Physical condition tier or number of previous owners |
| **Price (Target)** | Numerical | Market listing price |

---

## 🔄 Exploratory Data Analysis & Insights

* **Depreciation Dynamics:** Depreciation follows an exponential decay curve, with the steepest price drop occurring within the first 3–5 years of vehicle age.
* **Mileage Impact:** Price sensitivity to mileage is non-linear; luxury brands exhibit significantly higher price drops per 10,000 km compared to economy brands.
* **Transmission Preference:** Automatic vehicles command a consistent price premium over manual equivalents in mid-to-high tiers.

---

## 📈 Model Training & Evaluation Results

Multiple regression models were trained and benchmarked against standard evaluation metrics ($R^2$ Score, Mean Absolute Error, and Root Mean Squared Error):

* **Baseline Linear Models:** Ridge & Lasso Regression
* **Tree-Based Models:** Decision Trees, Random Forest Regressor
* **Gradient Boosting:** XGBoost & LightGBM Regressors

---

## 👤 Author

**Nour Saad Eladrosy**
* GitHub: [@noureladrosy8](https://github.com/noureladrosy8)