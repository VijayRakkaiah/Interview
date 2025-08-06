## 📈 1. What models did you use and why?

You used 4 regression models:

### 🔹 Linear Regression
- Fits a straight line to predict fare
- Works well when relationships are linear

### 🔹 Decision Tree Regressor
- Creates decision rules like:  
  “If distance > 5 km and hour = night, fare = $X”

### 🔹 Random Forest Regressor
- Combines many trees (a forest) and averages their predictions
- Reduces overfitting and improves accuracy

### 🔹 XGBoost Regressor
- Builds trees sequentially, each fixing the previous one's errors
- Fast and highly accurate for structured/tabular data

---

## 🔁 2. Differences between Linear Regression and Tree-based models?

| Feature           | Linear Regression               | Tree-based Models               |
|------------------|----------------------------------|----------------------------------|
| Relationship     | Assumes straight-line (linear)   | Handles complex, non-linear     |
| Flexibility      | Less flexible                    | More flexible                   |
| Performance      | Lower for complex data           | Higher for structured data      |

---

## 🌲 3. What is Random Forest?

- A collection of **many decision trees**
- Each tree gives a fare prediction → forest takes the average
- Reduces variance and overfitting

---

## ⚡ 4. What is XGBoost?

- Stands for **Extreme Gradient Boosting**
- Builds trees **one at a time**, each correcting the last
- Fast, powerful, and often state-of-the-art

---

## 🔍 5. What is Hyperparameter Tuning?

- Adjusting **settings** of a model to improve performance
- Hyperparameters are not learned — they’re set manually  
  _(e.g., number of trees, tree depth)_
- Used `RandomizedSearchCV` to search for the best combination

---

## 🎲 6. What is RandomizedSearchCV?

- Tries **random combinations** of hyperparameters
- More efficient than GridSearchCV (which tries all possible combinations)
- Uses **cross-validation** to find the best settings

---

## 🤔 7. Why use Random Forest over Linear Regression?

- Linear Regression can't capture complex patterns
- Random Forest:
  - Handles non-linearity
  - Robust to outliers
  - Higher accuracy

---

## 📉 8. How did you evaluate your models?

Used two metrics:
- **MAE (Mean Absolute Error)** – average of absolute differences
- **RMSE (Root Mean Square Error)** – penalizes large errors

---

## 🥇 9. Which model performed best?

- **XGBoost Regressor** had the **lowest error**
- Handled complex patterns and gave most accurate results

---

## ⚠️ 10. What challenges did you face?

- Dealing with:
  - Invalid coordinates
  - Outliers and missing data
  - Extracting useful features from raw data (e.g., distance from coordinates)

---

## 🚫 11. What is overfitting, and how did you prevent it?

- Overfitting = model learns **training data too well**, fails on new data
- Prevented by:
  - Limiting tree depth
  - Cross-validation
  - Using ensemble models like Random Forest & XGBoost

---

## ⏳ 12. What is cross-validation?

- Splits data into **folds**
- Trains on some folds, validates on others
- Reduces risk of overfitting
- Helps measure **generalization performance**

---

## ⚙️ 13. What hyperparameters did you tune?

Examples:

- **Random Forest:**
  - `n_estimators`, `max_depth`, `min_samples_split`

- **XGBoost:**
  - `learning_rate`, `n_estimators`, `max_depth`, `subsample`, `colsample_bytree`

---