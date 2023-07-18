# CryptoClustering

Code Overview

The code performs the following steps:

- Data Preprocessing: Loads the cryptocurrency market data from the CSV file into a Pandas DataFrame. It then normalizes the data using StandardScaler() to prepare it for clustering.
- Finding the Best Value for K: Uses the Elbow Method to find the optimal number of clusters (k) for K-Means. It computes the inertia (within-cluster sum of squared distances) for different k values and plots the Elbow Curve to visualize the optimal value of k.
- Clustering with K-Means (Using Original Data): Applies K-Means clustering to the original scaled data using the best value of k found in the previous step. It predicts the clusters for each cryptocurrency and adds a new column to the DataFrame with the cluster labels. A scatter plot is generated to visualize the clusters.
- Dimensionality Reduction with PCA: Applies Principal Component Analysis (PCA) to the scaled data, reducing the number of features to three principal components. The explained variance ratio is calculated to assess the information retention.
- Finding the Best Value for K (Using PCA Data): Uses the Elbow Method again, but this time, with the PCA-transformed data. It finds the optimal k for clustering the data with reduced dimensions and plots the corresponding Elbow Curve.
- Clustering with K-Means (Using PCA Data): Applies K-Means to the PCA-transformed data using the best value of k from the previous step. It predicts the clusters and generates a scatter plot to visualize the clustering results.
- Visualizing and Comparing Results: Generates composite plots to contrast the Elbow Curves and the clustering results with and without PCA, allowing for a visual comparison of the impact of dimensionality reduction.