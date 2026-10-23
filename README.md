# 🏠 House Prices: Advanced Regression Techniques

My first end-to-end Machine Learning project on Kaggle.

## 📌 Problem Statement
Predict residential home prices in Ames, Iowa using 79 explanatory variables.

## 🎯 Approach
- **Preprocessing**: Missing value imputation (mean for numeric, mode for categorical)
- **Encoding**: One-Hot Encoding for categorical variables
- **Target Transform**: Log1p transformation on `SalePrice`
- **Models**: Linear Regression, XGBoost
- **Validation**: 5-Fold Cross-Validation
- **Post-processing**: Intelligent clipping (min × 0.9, max × 1.3)

## 📊 Results

| Model | CV MAE (log) | Public Score | Rank |
|-------|:---:|:---:|:---:|
| Linear Regression (v1) | 0.09372 | ~14,000 | 162 |
| **XGBoost (v3)** | **0.08366** | **14,015.69** | **163** |
| XGBoost + Ordinal (v4) | 0.08419 | (Not submitted) | — |

**Best Model**: XGBoost (v3) — Top 4% on the public leaderboard.

## 📁 Project Structure

## 🚀 How to Run
1. Open the notebook in Kaggle.
2. Run all cells.

## 📝 Key Lessons Learned
1. **One-Hot Encoding > LabelEncoder** for nominal features (no false ordering).
2. **Log1p transform on target** significantly improves model performance.
3. **Cross-Validation** is more reliable than a single train/test split.
4. **Ordinal Encoding** did not improve XGBoost, so I kept One-Hot.
5. **Intelligent clipping** prevents catastrophic outlier predictions.

## 👤 Author
[YOUR NAME] — [YOUR KAGGLE PROFILE LINK]