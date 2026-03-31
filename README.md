# 🎿 Big Mountain Resort — ML-Driven Pricing Strategy
### Revenue Optimization Using Predictive Pricing Models Across 330 Ski Resorts

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Regression%20Models-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

---

## 📌 Project Overview

Big Mountain Resort had no data-backed framework for setting ticket prices — leaving revenue on the table or risking demand loss from mispricing in a competitive ski market.

This project builds predictive pricing models using data from **330 ski resorts** and **27 operational features** to help the resort understand how its pricing compares to competitors, identify which infrastructure investments justify a price increase, and quantify the exact revenue impact of those decisions.

---

## 🎯 Business Problem

> What ticket price should Big Mountain Resort charge — and which investments would justify raising it without losing customers?

Resort management needed to answer two questions:
1. Are we underpricing or overpricing relative to comparable resorts?
2. Which operational improvements would allow us to raise prices while maintaining demand?

---

## 📊 Dataset

| Property | Detail |
|----------|--------|
| Total resorts analyzed | 330 ski resorts |
| Features per resort | 27 operational features |
| Feature types | Infrastructure, terrain, services, pricing |
| Target variable | Ticket price (USD) |

**Key features included:**
- Number of runs and trails
- Vertical drop (feet)
- Number of chairlifts and surface lifts
- Snow making capability
- Resort acreage and terrain difficulty mix
- Weekend vs weekday pricing
- Amenities and services offered

---

## 🔧 Technical Approach

### 1. Exploratory Data Analysis
- Analyzed pricing distribution across 330 resorts
- Identified which features correlate most strongly with ticket price
- Detected outliers and missing values in operational data

### 2. Feature Engineering
- Handled missing values using median imputation
- Created interaction features between infrastructure variables
- Normalized continuous features for linear model compatibility

### 3. Model Development
Built and compared two regression models:

| Model | Approach | Strength |
|-------|----------|---------|
| Linear Regression | Baseline interpretable model | Easy to explain to stakeholders |
| Random Forest | Ensemble model | Captures non-linear relationships |

### 4. Model Evaluation
- Used cross-validation to assess generalization
- Compared RMSE and R² across both models
- Selected best model for business recommendations

### 5. Business Recommendation
Used model outputs to simulate the revenue impact of specific infrastructure investments at Big Mountain Resort.

---

## 📈 Results

| Metric | Value |
|--------|-------|
| Resorts analyzed | 330 |
| Features used | 27 |
| Pricing accuracy improvement | **~20%** over baseline |
| Recommended price increase | **$1.99 per ticket** |
| Estimated annual revenue impact | **~$3.47M** |
| Demand impact | None — increase is justified by infrastructure |

### Key Finding
Two infrastructure investments — **an additional chairlift** and **increased vertical drop** — justify a **$1.99 ticket price increase** without reducing customer demand. At current visitor volume, this translates to approximately **$3.47M in incremental annual revenue**.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Pandas / NumPy | Data cleaning and manipulation |
| Scikit-learn | Linear Regression, Random Forest, cross-validation |
| Matplotlib / Seaborn | EDA and model result visualization |
| Jupyter Notebook | Development environment |

---

## 📁 Project Structure

```
Capstone_3/
│
├── notebooks/
│   ├── 01_EDA.ipynb                        # Exploratory data analysis
│   ├── 02_Feature_Engineering.ipynb        # Feature creation and cleaning
│   ├── 03_Modeling.ipynb                   # Model training and comparison
│   └── 04_Business_Recommendations.ipynb  # Final pricing recommendations
│
├── data/
│   └── README.md                           # Data source description
│
├── requirements.txt                        # Python dependencies
└── README.md
```

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/patidarpuja/Capstone_3.git
cd Capstone_3

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

---

## 💡 Key Learnings

- Data-driven pricing is more reliable than intuition-based pricing in competitive markets
- **Random Forest** captured non-linear pricing relationships that Linear Regression missed
- Infrastructure features (chairlifts, vertical drop) are stronger price predictors than amenity features
- Quantifying business impact in dollar terms is what makes a model recommendation actionable
- Cross-validation is essential when working with a dataset of only 330 observations

---

## 👩‍💻 Author

**Puja Patidar**
Data Scientist | Data Analyst
📍 Jersey City, NJ | H4 EAD — No Sponsorship Required

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/puja-patidar-960037212)
[![GitHub](https://img.shields.io/badge/GitHub-patidarpuja-black?style=flat-square&logo=github)](https://github.com/patidarpuja)
