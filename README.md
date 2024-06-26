# Background

You’ll assume the role of an advisor in one of the top five financial advisory firms in the world. Competitors are fierce, so you want to propose a novel approach to assembling investment portfolios that are based on cryptocurrencies. Instead of basing your proposal on only returns and volatility, you want to include other factors that might impact the crypto market—leading to better performance for your portfolio.

When you present the idea, your manager loves it! So, you’re asked to create a prototype for submitting your crypto portfolio proposal to the company board of directors.

## What You're Creating

You’ll combine your financial Python programming skills with the new unsupervised learning skills that you acquired in this module. You’ll create a Jupyter notebook that clusters cryptocurrencies by their performance in different time periods. You’ll then plot the results so that you can visually show the performance to the board. The provided CSV file contains the price change data of cryptocurrencies in different periods.

## Files

Download the following files to help you get started: [Module 10 Challenge files](Module_10_Challenge_files).

## Instructions

The high-level steps for this Challenge are as follows:
1. Import the data (provided in the starter code).
2. Prepare the data (provided in the starter code).
3. Find the best value for k by using the original data.
4. Cluster the cryptocurrencies with K-means by using the original data.
5. Optimize the clusters with principal component analysis (PCA).
6. Find the best value for k by using the PCA data.
7. Cluster the cryptocurrencies with K-means by using the PCA data.
8. Visualize and compare the results.

The starter code already handles the first two steps. The following subsections include the detailed instructions for the remaining steps.

### Find the Best Value for k by Using the Original Data

In this section, you’ll use the elbow method to find the best value for k by using the original data. To do so, complete the following steps:
1. Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11.
2. To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.
3. Answer the following question: What’s the best value for k?

### Cluster the Cryptocurrencies with K-Means by Using the Original Data

In this section, you’ll use the K-means algorithm along with the best value for k that you found by using the original data. Specifically, you’ll use them to cluster the cryptocurrencies according to the provided price changes of the cryptocurrencies provided. To do so, complete the following steps:
1. Initialize the K-means model with four clusters by using the best value for k.
2. Fit the K-means model by using the original data.
3. Predict the clusters for grouping the cryptocurrencies by using the original data. Review the resulting array of cluster values.
4. Create a copy of the original data, and then add a new column of the predicted clusters.
5. Using hvPlot, create a scatter plot by setting `x="PC1"` and `y="PC2"`. Color the graph points with the labels that you found by using K-means. Then add the crypto name to the `hover_cols` parameter to identify the cryptocurrency that each data point represents.

### Optimize the Clusters with Principal Component Analysis

In this section, you’ll perform PCA and reduce the features to three principal components. To do so, complete the following steps:
1. Create a PCA model instance, and set `n_components=3`.
2. Use the PCA model to reduce the features to three principal components. Then review the first five rows of the DataFrame.
3. Get the explained variance to determine how much information can be attributed to each principal component.
4. Answer the following question: What’s the total explained variance of the three principal components?
5. Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.

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
5. Using hvPlot, create a scatter plot by setting `x="PC1"` and `y="PC2"`. Color the graph points with the labels that you found by using K-means. Then add the crypto name to the `hover_cols` parameter to identify the cryptocurrency represented by each data point.

### Visualize and Compare the Results

In this section, you’ll visually analyze the cluster analysis results by observing the outcome both with and without the use of optimization techniques. To do so, complete the following steps:
1. Create a composite plot by using hvPlot and the plus sign (+) operator to compare the elbow curve that you created from the original data with the one that you created from the PCA data.
2. Create a composite plot by using hvPlot and the plus (+) operator to compare the cryptocurrency clusters that resulted from using the original data with those that resulted from the PCA data.
3. Answer the following question: Based on visually analyzing the cluster analysis results, what’s the impact of using fewer features to cluster the data by using K-means?
