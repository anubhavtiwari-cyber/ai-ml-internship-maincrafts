# 🏠 AI/ML Internship — Task 1: Linear Regression (House Price Predictor)

> **Organization:** Maincrafts Technology  
> **Task:** Build & Evaluate a Linear Regression Model on the California Housing Dataset

---

## 📌 Objective

Train a Linear Regression model to predict median house prices in California, covering the complete ML workflow — data loading, EDA, preprocessing, model training, evaluation, and reporting.

---

## 📂 Project Structure

```
Task-1-Linear-Regression/
│
├── task1_ml_linear_regression.ipynb   # Main Jupyter Notebook (code + plots + comments)
├── Task1_ML_Report.pdf                # 2-page project report
├── linear_regression_model.pkl        # Saved trained model (generated after running notebook)
├── scaler.pkl                         # Saved StandardScaler (generated after running notebook)
└── README.md                          # This file
```

---

## 📊 Dataset

- **Name:** California Housing Dataset
- **Source:** `sklearn.datasets.fetch_california_housing`
- **Samples:** 20,640 rows
- **Features:** 8 numerical features
- **Target:** `MedHouseVal` — Median House Value (in $100,000s)

| Feature | Description |
|---|---|
| MedInc | Median income in block group |
| HouseAge | Median house age |
| AveRooms | Average rooms per household |
| AveBedrms | Average bedrooms per household |
| Population | Block group population |
| AveOccup | Average household members |
| Latitude | Geographic latitude |
| Longitude | Geographic longitude |

---

## ⚙️ Setup & Installation

```bash
# 1. Clone the repo
git clone https://github.com/<your-username>/ai-ml-internship-maincrafts.git
cd ai-ml-internship-maincrafts/Task-1-Linear-Regression

# 2. Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn jupyter joblib

# 3. Launch Jupyter
jupyter notebook task1_ml_linear_regression.ipynb
```

---

## 🔬 ML Workflow

1. **Data Loading** — Load dataset via sklearn, merge into DataFrame
2. **EDA** — Distributions, correlation heatmap, feature vs target scatter plots
3. **Preprocessing** — StandardScaler normalization, 80/20 train/test split
4. **Model Training** — `LinearRegression` (Ordinary Least Squares)
5. **Evaluation** — MAE, RMSE, R² on test set
6. **Visualization** — Actual vs Predicted, Residuals plot, Coefficient bar chart
7. **Save Model** — joblib pickle for future inference

---

## 📏 Model Results

| Metric | Value | Meaning |
|---|---|---|
| MAE | ~0.5300 | Avg error ≈ $53,000 per prediction |
| RMSE | ~0.7320 | Penalizes larger errors |
| R² | ~0.6060 | Model explains ~60.6% of price variance |

> **Key insight:** `MedInc` (median income) is the strongest predictor of house prices (correlation ≈ 0.69).

---

## 💡 Improvement Ideas

- **Ridge / Lasso Regression** — Add regularization to reduce overfitting
- **Random Forest / XGBoost** — Expected R² > 0.80
- **Feature Engineering** — e.g., rooms per person = AveRooms / AveOccup
- **Outlier Removal** — Handle capped values at MedHouseVal = 5.0
- **Cross-Validation** — 5-fold CV for more robust evaluation
- **Polynomial Features** — Capture non-linear interactions

---

## 📁 Deliverables

- [x] Jupyter Notebook with code, plots, and comments
- [x] 2-page PDF report (EDA + metrics + improvement ideas)
- [x] Saved model pickle (`linear_regression_model.pkl`)

---

## 🔗 Resources

- [scikit-learn Linear Regression Docs](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
- [California Housing Dataset Info](https://scikit-learn.org/stable/datasets/real_world.html#california-housing-dataset)
- [Kaggle Intro to ML](https://www.kaggle.com/learn/intro-to-machine-learning)
