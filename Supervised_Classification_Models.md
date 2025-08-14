# 🧠 Supervised Classification Models

## 📈 1. Logistic Regression
1. Despite the name, it's a classification model, not regression.
2. Outputs probabilities using the **sigmoid function**.
3. Best suited for binary classification (e.g., spam vs not spam).
4. Fast, simple, and works well with linearly separable data.
5. Uses a linear decision boundary (can be extended with polynomial features).
6. Assumes a linear relationship between features and the log-odds of the outcome.
7. Sensitive to multicollinearity and outliers.
8. Requires feature scaling for optimal results.
9. Easy to interpret (especially the weights of features).
10. A strong baseline model for most classification problems.

---

## 🌲 2. Random Forest Classifier
1. An ensemble of many decision trees trained on different data subsets.
2. Final prediction is the **majority vote** of all trees.
3. Great at reducing overfitting compared to a single decision tree.
4. Can handle both numerical and categorical data.
5. Works well with non-linear patterns and interactions.
6. Robust to outliers and missing values.
7. Doesn't require feature scaling.
8. Less interpretable compared to a single tree.
9. Requires more memory and computational power.
10. Strong default choice for many real-world problems.

---

## 🚀 3. Gradient Boosting Classifier (XGBoost, LightGBM, etc.)
1. Builds trees sequentially, each correcting the errors of the previous one.
2. Combines many weak learners into a strong model.
3. Highly effective on structured/tabular data.
4. Supports handling of missing values internally.
5. Achieves state-of-the-art performance in many ML competitions.
6. Needs careful hyperparameter tuning to prevent overfitting.
7. Slower to train but fast to make predictions.
8. Works well with both binary and multi-class classification.
9. Can handle both numeric and categorical features (LightGBM especially).
10. Popular tools include **XGBoost**, **LightGBM**, and **CatBoost**.

---

## 🧠 4. Support Vector Machine (SVM)
1. Finds the optimal boundary (hyperplane) that maximizes the margin between classes.
2. Uses **kernel tricks** (like RBF) to model non-linear boundaries.
3. Effective in high-dimensional spaces and with clear class separation.
4. Requires feature scaling for best performance.
5. Works well with medium-sized datasets.
6. Sensitive to noise and outliers.
7. Not easily interpretable.
8. Hyperparameter tuning (kernel, C, gamma) is crucial.
9. Slower on large datasets.
10. Great for complex but well-structured classification problems.

---

## 📦 5. K-Nearest Neighbors (KNN) Classifier
1. A **lazy learner** — it stores all training data.
2. Predicts the label by **majority vote** from the K nearest neighbors.
3. Very intuitive and simple to implement.
4. No training time, but slow during prediction (needs to compute distances).
5. Requires proper scaling of features for meaningful distance measures.
6. Struggles with high-dimensional data (curse of dimensionality).
7. Sensitive to noisy or irrelevant features.
8. Works well with locally clustered data.
9. Choice of "K" greatly affects performance.
10. Good baseline when data is small and relationships are local.

---

## 🧪 6. Naive Bayes Classifier
1. Based on **Bayes' Theorem** with the assumption that features are independent.
2. Extremely fast and efficient, especially with large text data.
3. Works well for **text classification** (e.g., spam detection, sentiment analysis).
4. Requires very little training data.
5. Performs surprisingly well despite the naive assumptions.
6. Handles high-dimensional data well.
7. Not suitable when feature independence is strongly violated.
8. Robust to irrelevant features.
9. Different variants: Gaussian, Multinomial, Bernoulli.
10. Simple, powerful model for quick and dirty classification tasks.

