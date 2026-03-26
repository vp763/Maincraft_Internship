# 🏠 House Price Predictor — Linear Regression
### AI & ML Internship — Task 1 | Maincrafts Technology

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-latest-orange?logo=scikit-learn)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](https://jupyter.org/)

---

## 📌 Overview

This project implements a **Linear Regression model** to predict California house prices using the classic **California Housing Dataset**. It covers the complete Machine Learning workflow from data exploration to model deployment.

---

## 🎯 Objective

Introduce the ML workflow:
- Data loading & exploration (EDA)
- Preprocessing & train/test split
- Model training with `LinearRegression`
- Evaluation using MAE, RMSE, R²
- Visualization of results
- Model saving with `joblib`

---

## 📁 Project Structure

```
Task1-House-Price-Predictor/
│
├── task1_ml_linear_regression.ipynb   ← Main Jupyter Notebook
├── Task1_Linear_Regression_Report.pdf ← Project Report (2-4 pages)
├── california_housing_lr.joblib       ← Saved trained model
└── README.md                          ← This file
```

---

## 📊 Dataset

**California Housing Dataset** — built into scikit-learn

| Property | Value |
|----------|-------|
| Records | 20,640 |
| Features | 8 |
| Target | `MedHouseVal` (Median House Value in $100,000s) |
| Missing Values | None ✅ |

### Features:
| Feature | Description |
|---------|-------------|
| `MedInc` | Median income in block group |
| `HouseAge` | Median house age |
| `AveRooms` | Average rooms per household |
| `AveBedrms` | Average bedrooms per household |
| `Population` | Block group population |
| `AveOccup` | Average house occupancy |
| `Latitude` | Geographic latitude |
| `Longitude` | Geographic longitude |

---

## 🔍 EDA Highlights

- **No missing values** — clean dataset
- Target variable (`MedHouseVal`) is **right-skewed**
- **MedInc** has the strongest correlation with house price (+0.69)
- Prices are **capped at $500,000** — creating outliers at the upper end

---

## 🤖 Model

**Algorithm:** Linear Regression (`sklearn.linear_model.LinearRegression`)

**Formula:**
```
Price = w1×MedInc + w2×HouseAge + w3×AveRooms + ... + bias
```

**Split:** 80% Train / 20% Test | `random_state=42`

---

## 📈 Results

| Metric | Value | Interpretation |
|--------|-------|----------------|
| **MAE** | 0.5332 | Avg prediction error ~$53,320 |
| **RMSE** | 0.7456 | Some large errors present |
| **R²** | 0.5758 | Model explains 57.58% of variance |

> **Note:** R² of ~0.58 is expected for a simple Linear Regression model with no feature engineering.

---

## 📉 Visualizations

### Actual vs Predicted
Points close to the red diagonal line = good predictions. The model tends to underestimate expensive houses.

### Residuals Plot
A downward trend at higher predicted values indicates the model underestimates high-priced homes — a classic Linear Regression limitation with non-linear data.

---

## 💡 Improvement Ideas

| Idea | Expected Impact |
|------|----------------|
| Feature Engineering (`rooms_per_person`) | Better signal |
| Ridge / Lasso Regression | Reduces overfitting |
| Random Forest Regressor | R² → 0.80+ |
| Feature Scaling (StandardScaler) | Improves Linear Regression |
| K-Fold Cross Validation | More stable evaluation |

---

## 🛠️ Tech Stack

- **Python 3**
- **pandas** — Data manipulation
- **numpy** — Numerical computing
- **scikit-learn** — ML model & metrics
- **matplotlib** — Plotting
- **seaborn** — Statistical visualization
- **joblib** — Model serialization

---

## 🚀 How to Run

### Option 1: Google Colab (Recommended)
1. Open `task1_ml_linear_regression.ipynb` in Google Colab
2. Click **Runtime → Run All**
3. All libraries are pre-installed in Colab ✅

### Option 2: Local Setup
```bash
# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn jupyter

# Launch Jupyter
jupyter notebook task1_ml_linear_regression.ipynb
```

---

## 📄 Report

A detailed 2-4 page PDF report (`Task1_Linear_Regression_Report.pdf`) is included covering:
- EDA findings
- Model summary
- Metric analysis
- Improvement ideas

---

## 👤 Author

**Maincrafts Technology — AI & ML Internship**  
Task 1 | Linear Regression | California Housing Dataset
