# California Housing Price Prediction

This project uses housing data to predict the median house value in California districts using both Simple and Multiple Linear Regression.

---

## 📌 Problem Statement
Given housing and demographic features such as median income, housing age, proximity to the ocean, etc., predict the median house price.

---

## 🔍 Exploratory Data Analysis (EDA)
- Handled missing values (e.g., `total_bedrooms` filled with median)
- One-hot encoded categorical column `ocean_proximity`
- Visualized relationships using:
  - Pairplots & Correlation heatmap
  - Histograms & Boxplots to study distributions and outliers

---

## ⚙️ Model Training

### 1️⃣ Simple Linear Regression  
- **Feature used**: `median_income`  
- **R² Score**: ~0.40  
- Model underfits due to single variable.

### 2️⃣ Multiple Linear Regression  
- **Features used**:  
  - `median_income`  
  - `housing_median_age`  
  - `population`  
  - `ocean_NEAR OCEAN`, `ocean_NEAR BAY` (one-hot encoded)
- **R² Score**: ~0.50  
- Performs better by capturing more data variance.

---

## 📊 Evaluation Metrics
- Mean Squared Error (MSE)  
- Root Mean Squared Error (RMSE)  
- R² Score  
- Actual vs Predicted scatterplots

---

## 📁 Dataset
California housing data containing:
- `total_rooms`, `total_bedrooms`, `population`, `households`, etc.
- `median_house_value` as the target variable
- `ocean_proximity` as a categorical feature

---

## 🔧 Tech Stack
- Python, Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn (Linear Regression models, train-test split, metrics)

---

## 📈 Key Takeaways
- Feature scaling wasn’t necessary due to linear regression models being used on non-regularized data.
- Simple linear regression gave quick baseline, but multiple regression improved predictions.
- Further gains possible by exploring regularization (Ridge/Lasso) or tree-based models.

---

## 🚀 How to Run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
python your_script_name.py
