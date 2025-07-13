# 🏡 California Housing Price Prediction (Ridge Regression + Polynomial Features)

This project builds a regularized linear regression (Ridge) model to predict median house values in California. It walks through model debugging techniques such as feature selection, polynomial expansion, and lambda tuning.

---

## 📂 Dataset

- **Source**: `sklearn.datasets.fetch_california_housing()`
- **Target**: `MedHouseVal` (Median house value in $100,000s)
- **Features**: 8 numeric variables (e.g., MedInc, HouseAge, AveRooms, Latitude)

---

## 🔧 Model Overview

| Stage                         | Description                                 |
|------------------------------|---------------------------------------------|
| Baseline                     | Ridge with all 8 features                   |
| Feature Reduction            | Ridge with 3 key features                   |
| Polynomial Features          | Degree=2 for enhanced expressiveness        |
| Lambda Tuning                | Tried alphas from 0.001 to 500              |
| Log-Target Experiment        | Rejected due to performance drop            |
| ✅ Final Model                | Ridge + All Features + Poly (deg=2) ✅       |

---

## 📊 Final Results

| Model                     | RMSE   | R² Score |
|--------------------------|--------|----------|
| Final Ridge + Poly Model | 0.7133 | 0.612    |

- Visualizations: Actual vs Predicted plots
- Best performance achieved with `alpha=100`

---

## 🧠 Key Takeaways

- Polynomial features improve model fit if used with full features and proper regularization
- Regularization is critical to prevent overfitting on expanded features
- Log-transformation may not always help — test with caution

---

## 🛠 Tech Stack

- Python, NumPy, Pandas, scikit-learn, Matplotlib
- Jupyter Notebook environment

---

## 🚀 Next Steps

- Try nonlinear models (e.g., Random Forest, XGBoost)
- Use cross-validation instead of train-test split
- Deploy with Streamlit or Flask for interactive demo

---

**Project by:** Anshul Rai
**Status:**  In progress
