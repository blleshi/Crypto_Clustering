# Clustering Cryptocurrencies

## Instructions

The high-level steps for this Challenge are as follows:

1. [Import the data](#import-the-data) (provided in the starter code).
2. [Prepare the data](#prepare-the-data) (provided in the starter code).
3. [Find the best value for k by using the original data](#find-the-best-value-for-k-by-using-the-original-data).
4. [Cluster the cryptocurrencies with K-means by using the original data](#cluster-the-cryptocurrencies-with-k-means-by-using-the-original-data).
5. [Optimize the clusters with principal component analysis](#optimize-the-clusters-with-principal-component-analysis).
6. [Find the best value for k by using the PCA data](#find-the-best-value-for-k-by-using-the-pca-data).
7. [Cluster the cryptocurrencies with K-means by using the PCA data](#cluster-the-cryptocurrencies-with-k-means-by-using-the-pca-data).
8. [Visualize and compare the results](#visualize-and-compare-the-results).

The starter code already handles the first two steps. The following subsections include the detailed instructions for the remaining steps.

### Find the Best Value for k by Using the Original Data

In this section, you’ll use the elbow method to find the best value for k by using the original data. To do so, complete the following steps:

1. Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11.

2. To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.

3. Answer the following question: What’s the best value for k?

### Cluster the Cryptocurrencies with K-means by Using the Original Data

In this section, you’ll use the K-means algorithm along with the best value for k that you found by using the original data. Specifically, you’ll use them to cluster the cryptocurrencies according to the provided price changes of the cryptocurrencies provided. To do so, complete the following steps:

1. Initialize the K-means model with four clusters by using the best value for k.

2. Fit the K-means model by using the original data.

3. Predict the clusters for grouping the cryptocurrencies by using the original data. Review the resulting array of cluster values.

4. Create a copy of the original data, and then add a new column of the predicted clusters.

5. Using `hvPlot`, create a scatter plot by setting `x="PC1"` and `y="PC2"`. Color the graph points with the labels that you found by using K-means. Then add the crypto name to the `hover_cols` parameter to identify the cryptocurrency that each data point represents.

### Optimize the Clusters with Principal Component Analysis

In this section, you’ll perform PCA and reduce the features to three principal components. To do so, complete the following steps:

1. Create a PCA model instance, and set `n_components=3`.

2. Use the PCA model to reduce the features to three principal components. Then review the first five rows of the DataFrame.

3. Get the explained variance to determine how much information can be attributed to each principal component.

4. Answer the following question: What’s the total explained variance of the three principal components?

5. Create a new DataFrame with the PCA data. Be sure to set the `coin_id` index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.

### Find the Best Value for k by Using the PCA Data

In this section, you’ll use the elbow method to find the best value for k by using the PCA data. To do so, complete the following steps:

1. Code the elbow method algorithm, and use the PCA data to find the best value for k. Use a range from 1 to 11.

2. To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.

3. Answer the following questions: What’s the best value for k when using the PCA data? Does it differ from the best value for k that you found when using the original data?

### Cluster the Cryptocurrencies with K-means by Using the PCA Data

In this section, you’ll use the PCA data, the K-means algorithm, and the best value for k that you found by using the PCA data. Specifically, you’ll use them to cluster the cryptocurrencies according to the principal components. To do so, complete the following steps:

1. Initialize the K-means model with four clusters by using the best value for k.

2. Fit the K-means model by using the PCA data.

3. Predict the clusters for grouping the cryptocurrencies by using the PCA data. Review the resulting array of cluster values.

4. Create a copy of the DataFrame with the PCA data, and then add a new column to store the predicted clusters.

5. Using `hvPlot`, create a scatter plot by setting `x="PC1"` and `y="PC2"`. Color the graph points with the labels that you found by using K-means. Then add the crypto name to the `hover_cols` parameter to identify the cryptocurrency that each data point represents.

### Visualize and Compare the Results

In this section, you’ll visually analyze the cluster analysis results by observing the outcome both with and without the use of optimization techniques. To do so, complete the following steps:

1. Create a composite plot by using `hvPlot` and the plus sign (+) operator to compare the elbow curve that you created from the original data with the one that you created from the PCA data.

2. Create a composite plot by using `hvPlot` and the plus (+) operator to compare the cryptocurrency clusters that resulted from using the original data with those that resulted from the PCA data.

3. Answer the following question: Based on visually analyzing the cluster analysis results, what’s the impact of using fewer features to cluster the data by using K-means?


