# 🛒 Walmart Weekly Sales Prediction
### Demand Planning Pipeline Using XGBoost on 420K+ Weekly Records

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![XGBoost](https://img.shields.io/badge/XGBoost-R²%200.88-orange?style=flat-square)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Feature%20Engineering-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

---

## 📌 Project Overview

Retail chains lose millions annually to stockouts and overstock. Accurate weekly demand forecasting across hundreds of stores and departments is critical — but hard to scale reliably without a rigorous, data-driven approach.

This project builds a time-aware demand forecasting pipeline on **420,000+ weekly sales records** from Walmart stores, using advanced feature engineering and XGBoost regression to predict weekly sales with high accuracy while preventing data leakage through proper time-series validation.

---

## 🎯 Business Problem

> How can Walmart predict weekly sales at the store-department level with enough accuracy to support demand planning and inventory optimization decisions?

Inaccurate forecasting leads to two costly outcomes:
- **Overstock** — excess inventory ties up capital and increases storage costs
- **Stockout** — lost sales and poor customer experience

This project aims to reduce forecasting error to a level that makes inventory decisions more reliable and data-driven.

---

## 📊 Dataset

| Property | Detail |
|----------|--------|
| Total records | 420,000+ weekly observations |
| Stores | 45 Walmart stores |
| Departments | 81 departments per store |
| Time period | Multi-year weekly data |
| Features engineered | 20+ |
| Target variable | Weekly sales (USD) |

---

## 🔧 Technical Approach

### 1. Data Cleaning
- Handled missing values across store, department, and date fields
- Standardized date formats for time-series processing
- Removed or imputed outliers in weekly sales values

### 2. Exploratory Data Analysis
- Analyzed sales distribution across stores and departments
- Identified seasonal patterns, holiday spikes, and promotional effects
- Detected and visualized correlations between features and sales

### 3. Feature Engineering
Engineered **20+ time-aware features** across four categories:

| Category | Features |
|----------|---------|
| Calendar | Week of year, month, quarter, year |
| Holiday | IsHoliday flag, days before/after holiday |
| Promotions | Markdown events (1–5), promotion flags |
| Store-level | Store type, store size, department number |

### 4. Time-Series Cross-Validation
Used **TimeSeries Split** for all cross-validation to prevent data leakage — training always uses only past data to predict future values.

> Standard k-fold cross-validation randomly shuffles data. For time series this allows the model to see the future during training. TimeSeries Split prevents this completely.

### 5. Model Comparison

| Model | RMSE | R² | Notes |
|-------|------|----|-------|
| Linear Regression | ~11,200 | ~0.61 | Baseline |
| Random Forest | ~8,400 | ~0.79 | Improved but slower |
| **XGBoost** | **6,900** | **0.88** | Best performance |

---

## 📈 Results

| Metric | Value |
|--------|-------|
| Final Model | XGBoost Regressor |
| R² Score | **0.88** |
| RMSE | **6,900** |
| MAE | **4,100** |
| Baseline R² | 0.61 |
| Improvement over baseline | **+27 percentage points** |

> An R² of 0.88 means the model explains 88% of the variance in weekly sales — a strong result for retail forecasting at store-department granularity.

---

## 📁 Repository Structure

```
Capstone_3/
│
├── cap3_data_cleaning_final.ipynb       # Data cleaning and preprocessing
├── cap3_EDA.ipynb                       # Exploratory data analysis
├── Final_submitted_cap_3.ipynb          # Final model and business recommendations
├── Capstone_3_Final_report_walmart.pdf  # Full project report
├── final_PPT_capstone_3.pptx            # Presentation slides
└── README.md
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Pandas / NumPy | Data manipulation and feature engineering |
| Scikit-learn | TimeSeries Split, baseline models, metrics |
| XGBoost | Final regression model |
| Matplotlib / Seaborn | EDA and results visualization |
| Jupyter Notebook | Development environment |

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/patidarpuja/Capstone_3.git
cd Capstone_3

# Install dependencies
pip install pandas numpy scikit-learn xgboost matplotlib seaborn jupyter

# Step 1 — Data cleaning
jupyter notebook cap3_data_cleaning_final.ipynb

# Step 2 — Exploratory data analysis
jupyter notebook cap3_EDA.ipynb

# Step 3 — Final model and recommendations
jupyter notebook Final_submitted_cap_3.ipynb
```

---

## 💡 Key Learnings

- **TimeSeries Split** is not optional for time-based data — standard cross-validation will overestimate model performance by leaking future data into training
- **Feature engineering** matters more than model choice — holiday and markdown features drove most of the accuracy improvement
- **XGBoost** outperformed Random Forest because it handles non-linear interactions between store type, department, and seasonal patterns better
- **RMSE** is the right primary metric here because large errors are more costly than small ones in inventory planning
- Retail forecasting at department level is significantly harder than store-level forecasting due to high variability across product categories

---

## 👩‍💻 Author

**Puja Patidar**
Data Scientist | Data Analyst
📍 Jersey City, NJ | H4 EAD — No Sponsorship Required

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/puja-patidar-960037212)
[![GitHub](https://img.shields.io/badge/GitHub-patidarpuja-black?style=flat-square&logo=github)](https://github.com/patidarpuja)
