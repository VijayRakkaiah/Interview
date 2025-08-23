# 🧠 Unsupervised Learning Models

## 🧩 1. K-Means Clustering
1. Groups similar data points into **K clusters** (like sorting colored balls).
2. You tell it how many groups (K) to make.
3. It randomly picks K "centers" and assigns data points to the nearest one.
4. Then it moves the centers and reassigns points, over and over.
5. Stops when everything stays in the same group.
6. Works best when groups are clearly separated.
7. Fast and simple for large datasets.
8. Sensitive to the initial center positions.
9. Doesn’t work well with odd-shaped or overlapping clusters.
10. Needs you to choose the right number of clusters (K).

---

## 🌀 2. Hierarchical Clustering
1. Builds a **tree of clusters** (like a family tree).
2. Starts with each point as its own cluster.
3. Merges the closest ones step by step.
4. Creates a **dendrogram** (tree diagram) to show grouping.
5. Doesn’t need to know the number of clusters in advance.
6. Can use different methods (like average or nearest point) to merge.
7. Good for understanding relationships between data.
8. Slower than K-Means for large datasets.
9. Sensitive to outliers and scaling.
10. Lets you **choose the number of clusters by cutting the tree**.

---

## 📊 3. Principal Component Analysis (PCA)
1. A method to **reduce the number of features** (dimensionality).
2. Finds the directions where data varies the most.
3. Rotates the data to make these directions the new axes (components).
4. Keeps only the top few axes to simplify the data.
5. Makes it easier to **visualize and process high-dimensional data**.
6. Often used before clustering or machine learning.
7. Helps remove noise and redundant information.
8. Components are combinations of original features (not always interpretable).
9. Works best when data is scaled and continuous.
10. Fast and powerful for summarizing large datasets.

---

## 🕳 4. DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
1. Groups points that are close together in dense areas.
2. Doesn’t need to know how many clusters there are.
3. Can find **odd-shaped** clusters (unlike K-Means).
4. Labels points that don’t belong anywhere as **noise**.
5. Needs two parameters: `eps` (distance) and `minPts` (neighbors).
6. Good for separating clusters with irregular shapes.
7. Resistant to outliers and noise.
8. Struggles if clusters have different densities.
9. Slower on large datasets compared to K-Means.
10. Great for spatial data or GPS-type clustering.

---

## 🧠 5. Autoencoders
1. A type of neural network used to **compress and reconstruct** data.
2. Learns to copy input to output through a small hidden layer.
3. Hidden layer learns a compressed version of the input.
4. Useful for **dimensionality reduction** or **anomaly detection**.
5. Can handle non-linear patterns (unlike PCA).
6. Needs a lot of data and training time.
7. Hard to interpret the encoded features.
8. Can overfit if the network is too complex.
9. Commonly used in image compression and denoising.
10. Forms the basis of deep unsupervised learning.

---

## 🎭 6. t-SNE (t-Distributed Stochastic Neighbor Embedding)
1. Mainly used to **visualize high-dimensional data** in 2D or 3D.
2. Keeps similar points close and dissimilar points far.
3. Very useful for spotting clusters and patterns.
4. Doesn’t work well for actual clustering tasks.
5. Computationally expensive on large datasets.
6. Doesn’t preserve global distances—only local structure.
7. Output changes each time unless you fix the seed.
8. Needs tuning of parameters like `perplexity`.
9. Often used after PCA to reduce noise.
10. Great for exploring embeddings or image/word clusters.
