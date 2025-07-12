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
```
### Model Training:
python```
lr = LinearRegression()
lr.fit(xtrain, ytrain)```
Model Coefficients:
Intercept: 94850.22

Coefficient (slope): 231.58

This gives the linear equation:
python```
price = 231.58 * size + 94850.22```
## ✅ Evaluation
### Predictions:
python```
ypred = lr.predict(xtest)```
### R² Score:
python```
r2_score(ytest, ypred)  →  0.6398```
### Error Metrics:
Mean Absolute Error (MAE): 40848.90

Mean Squared Error (MSE): 2578017526.77

Root Mean Squared Error (RMSE): 50774.57

## 📉 Visualization
Scatter Plot with Regression Line:
python```
plt.scatter(xtrain, ytrain, color='b')
plt.plot(xtest, ypred, color='r')```
Blue dots represent training data

Red line represents the predicted linear model on test data

## 🔮 Prediction Examples
python```
lr.predict([[100]])  →  $118,008.60
lr.predict([[50]])   →  $106,429.41```
## 📌 Tools & Libraries Used
Pandas for data handling

NumPy for numerical operations

Matplotlib for plotting

Scikit-learn for model training and evaluation

## 🧠 Future Improvements
Add more features like location, number of rooms, property age, etc.

Perform feature scaling and polynomial regression for non-linear data

Visualize residuals and improve model robustness

Build an interactive dashboard for price prediction

## 🙌 Acknowledgments
Dataset used for educational purposes

Inspired by real estate regression examples from tutorials and textbooks


