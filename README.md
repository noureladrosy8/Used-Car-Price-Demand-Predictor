# 🚗 Used Car Price & Demand Predictor

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8%2B-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange.svg" alt="ML">
  <img src="https://img.shields.io/badge/Status-Active-success.svg" alt="Status">
</p>

An end-to-end Machine Learning project designed to accurately predict used car market prices and forecast market demand. This system leverages advanced data preprocessing, feature engineering, and robust regression models to help buyers, sellers, and dealerships make data-driven decisions.

---

## 🌟 Key Features

- **Accurate Price Prediction:** Estimates the market value of used cars based on specifications, mileage, brand, year, and condition.
- **Demand Analysis:** Explores market trends and listing attributes to understand vehicle demand drivers.
- **Exploratory Data Analysis (EDA):** Deep-dive visualizations uncovering correlations between depreciation, mileage, and price.
- **Robust ML Pipeline:** Clean, modular code structure handling missing values, categorical encoding, feature scaling, and model training.

---

## 🛠️ Tech Stack & Libraries

This project is built using Python and industry-standard machine learning libraries:

* **Language:** Python 3.x
* **Data Manipulation & Analysis:** `Pandas`, `NumPy`
* **Data Visualization:** `Matplotlib`, `Seaborn`
* **Machine Learning & Modeling:** `Scikit-Learn`, `XGBoost` / `LightGBM`
* **Environment:** Jupyter Notebook / Google Colab

---

## 📂 Project Structure

```text
Used-Car-Price-Demand-Predictor/
│
├── data/                  # Raw and processed datasets
├── notebooks/             # Jupyter notebooks for EDA and experimentation
├── src/                   # Source code (train.py, inference.py)
├── models/                # Saved trained model checkpoints (.pkl)
├── requirements.txt       # Required Python packages
└── README.md              # Project documentation
```

---

## 📊 Dataset & Features

The dataset contains comprehensive information regarding used car listings. Key features include:

| Feature Name | Description | Data Type |
| :--- | :--- | :--- |
| **Brand / Model** | Manufacturer and specific model of the vehicle | Categorical |
| **Year** | Manufacturing year / Age of the car | Numerical |
| **Mileage** | Total distance driven (in kilometers or miles) | Numerical |
| **Engine / CC** | Engine capacity and performance metrics | Numerical |
| **Fuel Type** | Gasoline, Diesel, Hybrid, Electric, etc. | Categorical |
| **Transmission** | Manual or Automatic | Categorical |
| **Condition** | Overall physical and mechanical state | Categorical |
| **Price (Target)** | Market price of the car | Numerical |

---

## 🔄 Methodology & Workflow

1. **Data Preprocessing & Cleaning:**
   - Handled missing/null values through smart imputation.
   - Removed outliers (e.g., unrealistic prices or extreme mileages).
   - Converted categorical variables using One-Hot Encoding and Label Encoding.

2. **Exploratory Data Analysis (EDA):**
   - Analyzed price distribution curves and depreciation rates over time.
   - Generated correlation matrices to find key drivers influencing car prices.

3. **Feature Engineering:**
   - Created new interaction features such as *Age of Car* and *Kilometers Driven per Year*.
   - Applied standard scaling and normalization techniques.

4. **Model Training & Evaluation:**
   - Experimented with multiple regression algorithms (Linear Regression, Random Forest, Gradient Boosting, XGBoost).
   - Evaluated models using robust metrics: **RMSE**, **MAE**, and **$R^2$ Score**.

---

## 🚀 Getting Started & Installation

To run this project locally, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/noureladrosy8/Used-Car-Price-Demand-Predictor.git
   cd Used-Car-Price-Demand-Predictor
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the training script:**
   ```bash
   python src/train.py
   ```

---

## 👤 Author

**Nour Saad Eladrosy**
- GitHub: [@noureladrosy8](https://github.com/noureladrosy8)

---

<p align="center">
  ⭐ If you found this project helpful, feel free to give it a star!
</p>