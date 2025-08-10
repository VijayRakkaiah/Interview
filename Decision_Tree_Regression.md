# 🌳 Decision Tree Regression

Imagine you’re trying to guess **house prices** based on features like:

- Number of rooms 🛏  
- Size of the house 📐  
- Location 📍  

Instead of drawing a single straight line (like Linear Regression), a **Decision Tree Regressor** works by **splitting the data into smaller and smaller groups** and making a prediction for each group.

Think of it like a flowchart:

> "Is the house size > 2000 sq ft?"  
> ➡ Yes → Go down one branch  
> ➡ No → Go down another branch  

At the end of each branch, we give a prediction based on the average of the points in that group.

---

## 🪓 How Does It Work? (Step-by-Step)

1. **Start with all data**  
2. Find the feature and split point that divides the data into two groups, **minimizing prediction error**.  
3. Repeat the process **inside each group**, creating more branches.  
4. Stop when:
   - The group is too small
   - Error can’t be reduced further
5. The final nodes (leaves 🍃) contain the predictions.

---

## 📏 Example

Let’s predict **exam scores** based on study hours:

📂 All students
  ├─ If study_hours ≤ 4 → Avg score = 50
  └─ If study_hours > 4
       ├─ If study_hours ≤ 7 → Avg score = 70
       └─ If study_hours > 7 → Avg score = 90

If a student studies **6 hours**, the tree says → **70 marks**.

---

## 📐 Prediction Rule

Unlike `y = mx + b`, decision trees don’t have a single equation.  
They are **rules-based**:

`If condition_1 AND condition_2 ... THEN prediction = value`


The **value** is usually the **mean** of all training points in that leaf.

---

## 🎯 The Goal

The goal is to **split the data** in such a way that:

- Predictions in each group are as close as possible to the real values.
- Groups (leaves) are **pure** (low error inside each).

---

## 📉 Measuring a Good Split – Cost Function

For regression trees, the common metric is:

**Mean Squared Error (MSE)** inside each split.

`MSE = (1/n) * Σ (actual - predicted)²`


A split is **good** if it reduces the MSE more than any other possible split.

---

## 🧗 How Does a Tree Grow?

1. Start: All points in one group.
2. Try all features + split points.
3. Pick the split that **reduces MSE** the most.
4. Repeat for each child node.
5. Stop based on:
   - `max_depth` (tree height limit)
   - `min_samples_split` (minimum data to split)
   - `min_samples_leaf` (minimum data in leaf)

---

## ✂️ How Do We Prevent Overfitting?

Decision trees can keep splitting until they memorize the data (**overfit**).

We prevent that by **pruning**:

- **Pre-pruning:** Limit depth, samples per split, etc.
- **Post-pruning:** Grow a full tree, then cut unnecessary branches.

---

## 🏁 Global Minimum?

Decision trees don’t use gradient descent — they use **greedy search**.  
At each step, they pick the **best split now**, without looking ahead.  
They aim to minimize error **at each split**, but might not find the overall perfect tree.

---

## 📊 Error Calculation

- Inside each leaf: prediction = average value of data in that leaf.
- Error = difference between predictions and actual values (e.g., MSE).

---

## 🎯 How Does Error Help the Tree?

- If splitting reduces error, the split is kept.
- If splitting doesn’t reduce error enough, the tree stops splitting there.

---

## 🔄 Summary Table

| Term                  | Simple Meaning |
|-----------------------|----------------|
| Decision Tree Regressor | Splits data into smaller groups to make predictions |
| Node                  | A decision point (e.g., "Is size > 2000 sq ft?") |
| Leaf                  | End point with a prediction value |
| Split                 | How data is divided at each step |
| Cost Function         | Usually MSE, measures how bad predictions are in a group |
| Overfitting           | Tree memorizes training data instead of generalizing |
| Pruning               | Cutting unnecessary branches to avoid overfitting |
| Greedy Search         | Picking the best split at each step without looking ahead |

