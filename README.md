# ✅ Real Estate Price Prediction Using Linear Regression

## 📌 Project Overview
This project builds a **Linear Regression model** to predict real estate prices based on property size. The model is trained using supervised learning on a dataset containing 100 real estate transactions. We evaluate the model using R² score and common error metrics such as MAE and RMSE.

---

## 🗃️ Dataset Information
- **File:** `real_estate_price_size.csv`
- **Format:** CSV
- **Number of Rows:** 100
- **Columns:**
  - `price`: Property price in dollars (float)
  - `size`: Property size in square feet (float)

---

## 📊 Data Preprocessing
- Loaded dataset using `pandas.read_csv()`
- Checked for null values and data types using `.info()`
- Separated the features (`size`) and target (`price`) columns
- Performed data splitting with `train_test_split()`

---

## 🧠 Model Building

### Algorithm:
- **Linear Regression** from `sklearn.linear_model`

### Data Split:
```python
xtrain, xtest, ytrain, ytest = train_test_split(x, y, test_size=0.2, random_state=150)
