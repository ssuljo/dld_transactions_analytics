# Dubai Real Estate Analysis & Price Prediction

A data science project analyzing Dubai’s property market — from **data exploration** and **cleaning** to **feature engineering** and **price prediction** using XGBoost. The goal is to uncover patterns that drive property values and build a predictive model that estimates prices based on property and location features.

---

## 📂 Project Overview

This project follows a structured data science workflow:

1. **Data Exploration** – Initial analysis and visualization of Dubai property transactions.
2. **Data Cleaning** – Filtering for core residential sales, handling missing values, and managing outliers.
3. **Feature Engineering** – Creating predictive features from raw data, including location, temporal, and engineered metrics.
4. **Modeling & Prediction** – Training and evaluating an XGBoost regression model to predict property sale prices.

---

## 📊 Dataset

We use open real estate transaction data from **Dubai Pulse**:
[Dubai Pulse DLD Transactions Dataset](https://www.dubaipulse.gov.ae/data/dld-transactions/dld_transactions-open)

The dataset contains property transaction records including:

* Property location & area
* Transaction date & type
* Sale price
* Project and master development information
* Number of rooms (where available)

---

## 📥 Setup Instructions

1. **Download the Dataset**
   Download `Transactions.csv` from the [Dubai Pulse link](https://www.dubaipulse.gov.ae/data/dld-transactions/dld_transactions-open).

2. **Place in Project Directory**
   Save the file to:

   ```
   data/raw/Transactions.csv
   ```

3. **Install Dependencies**
   Install required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

4. **Run Notebooks**
   The Jupyter notebooks in the `notebooks/` directory correspond to each project stage:

   * `data_peparation.ipynb`
   * `xgboost_localmode_train_test.ipynb`

---

## 🚀 Usage

* **Reproduce the analysis:** Follow the notebooks in order to go from raw data to a trained price prediction model.
* **Modify for your own use:** Replace `Transactions.csv` with updated Dubai Pulse data or other regional datasets.
* **Deploy the model:** Extend Modeling Part to integrate the trained model into a prediction API or web app.

---

## 📈 Results

* Model type: **XGBoost Regressor**
* Test R² (original prices): **0.91**
* Test MAE: \~**190k AED**
* Key price drivers: Property size, location, master project, number of rooms, year of sale.

---

## 📌 Notes

While the model performs well given the available data, important features such as **property condition** (furnished/unfurnished, renovated/new), **sale type** (first sale vs. secondary), and **building age** were not present. Adding these could significantly improve predictive performance.