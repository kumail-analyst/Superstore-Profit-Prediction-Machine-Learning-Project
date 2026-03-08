# 🛒 Superstore Profit Prediction — Machine Learning Project
## 📌 Project Overview

This project predicts whether a retail order from the **Sample Superstore dataset** will be **Profitable or result in a Loss**, using Machine Learning classification models.

A live interactive web app is also built using the trained model — allowing users to input order details and instantly get a profit prediction.

---

## 🎯 Problem Statement

> *"Given an order's details such as category, discount, region, and sales amount — can we predict whether this order will generate profit or loss?"*

This is a **Binary Classification** problem:
- `1` → Profitable Order ✅
- `0` → Loss Order ❌

---

## 📊 Dataset

| Property | Detail |
|---|---|
| Name | Sample Superstore |
| Rows | 9,994 |
| Columns | 21 |
| Time Period | January 2014 — December 2017 |
| Source | Tableau Sample Dataset |

**Key Features Used:**
- Category, Sub-Category
- Region, Segment
- Ship Mode
- Quantity, Discount, Sales

---

## 🔍 Project Structure

```
📁 superstore-profit-prediction/
│
├── 📓 01_EDA_Analysis.ipynb       # Exploratory Data Analysis
├── 📓 02_ML_Model.ipynb           # Model Training & Evaluation
├── 🌐 profit_predictor.html       # Interactive Web App
├── 📊 Sample_Superstore.csv       # Dataset
└── 📄 README.md                   # Project Documentation
```

---

## 📈 Exploratory Data Analysis

Key insights discovered during EDA:

- 📦 **Technology** category has the highest profit margins
- 🪑 **Furniture** (especially Tables) frequently results in losses
- 💸 Orders with **discount > 30%** almost always result in loss
- 🌍 **West region** performs best in terms of profitability
- 📅 **Q4 (Sep–Nov)** shows peak sales every year

---

## 🤖 Machine Learning Models

The model were train:

| Model | Accuracy |
| **XGBoost** | **94.45% ✅ Best** |

### Model Pipeline:
1. Target variable created: `Profitable = (Profit > 0)`
2. Categorical encoding with `LabelEncoder`
3. 80/20 Train-Test Split
4. Model training & evaluation
5. Confusion Matrix & Feature Importance analysis

---

## 🔑 Key Findings

```
Most Important Features (XGBoost):
1. Discount       ← Most critical factor
2. Sales Amount
3. Sub-Category
4. Quantity
5. Region
```

> **Main Insight:** High discount is the #1 cause of loss.
> Orders with 0% discount are profitable 98%+ of the time.

---

## 🌐 Interactive Web App

A browser-based prediction tool built with pure HTML/CSS/JS.
The trained Random Forest model is embedded directly in the app — **no server required!**

**Features:**
- Select all 8 order features
- Real-time discount risk indicator
- Profit probability with confidence score
- Animated results with key factor tags

**How to use:**
1. Open `profit_predictor.html` in any browser
2. Fill in order details
3. Click **RUN PREDICTION**
4. See instant result! ✅

---

## 🛠️ Tech Stack

| Tool | Usage |
|---|---|
| Python 3.8+ | Core language |
| Pandas | Data manipulation |
| NumPy | Numerical computation |
| Matplotlib & Seaborn | Data visualization |
| Scikit-learn | ML models |
| XGBoost | Best performing model |
| HTML/CSS/JS | Web app |

---

## 🚀 How to Run
### 1. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

### 2. Run the notebooks
```bash
jupyter notebook
```
Open `01_EDA_Analysis.ipynb` first, then `02_ML_Model.ipynb`

### 3. Open Web App
Simply open `profit_predictor.html` in your browser — no installation needed!

---

## 📉 Results Summary

```
Dataset     : 9,994 orders (2014–2017)
Problem     : Binary Classification
Best Model  : XGBoost
Accuracy    : 94.45%
Key Finding : Discount > 30% = High Loss Risk
Web App     : Live prediction in browser
```

---

## 👤 Author

**Kumail Riaz**
- 📧 kumail.788998@gmail.com
---

---

*⭐ If you found this project helpful, please give it a star!*
