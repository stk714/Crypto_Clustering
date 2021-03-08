# Crypto_Clustering
Assume the role of an advisor in one of the top five financial advisory firms in the world. Competitors are fierce, so you want to propose a novel approach to assembling investment portfolios that are based on cryptocurrencies. Instead of basing your proposal on only returns and volatility, you want to include other factors that might impact the crypto market—leading to better performance for your portfolio.

## Cluster Cryptocurrencies with K-means
In this section, you will use the K-Means algorithm with a given value for k to cluster the cryptocurrencies according to the price changes of cryptocurrencies provided.

* Initialize the K-means model with four clusters (n_clusters=4).
* Fit the K-means model using the scaled data.
* Predict the clusters to group the cryptocurrencies using the scaled data. View the resulting array of cluster values.
* Add a new column to the DataFrame with the scaled data with the predicted clusters.
* Create a scatter plot using hvPlot by setting x="price_change_percentage_14d" and y="price_change_percentage_1y". Color the graph points with the labels found using K-Means and add the crypto name in the hover_cols parameter to identify the cryptocurrency represented by each data point.

## Find the Best Value for k
In this section, you will use the elbow method to find the best value for k.

* Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11.
* Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
* Answer the following question: What is the best value for k?

## Optimize Clusters with Principal Component Analysis
In this section, you will perform a principal component analysis (PCA) and reduce the features to three principal components.

* Create a PCA model instance and set n_components=3.
* Use the PCA model to reduce to three principal components. View the first five rows of the DataFrame.
* Retrieve the explained variance to determine how much information can be attributed to each principal component.
* Answer the following question: What is the total explained variance of the three principal components?
* Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.
* Initiate a new K-means algorithm using the PCA DataFrame to group the cryptocurrencies. Set the n_components parameter equal to the best value for k found before. View the resulting array.
* For further analysis, add the following columns to the DataFrame with the PCA data. Review the resulting DataFrame once the additional columns have been added. Make sure to do the following:
    * From the original DataFrame, add the price_change_percentage_1y and price_change_percentage_14d columns.
    * Add a column with the predicted cluster values identified using a k value of 4. (The predicted cluster values were calculated in the “Cluster Cryptocurrencies with K-means” section.)
    * Add a column with the predicted cluster values identified using the optimal value for k.

## Visualize the Results
Use the PCA data to create two scatter plots using hvPlot by setting x="price_change_percentage_14d" and y="price_change_percentage_1y". Make sure to do the following:

* In the first plot, color the plot points by the cluster values identified using a k value of 4.
* In the second plot, color the plot points by the cluster values identified using the optimal value for k.
* In both plots, add the crypto name by sing the hover_cols parameter to identify the cryptocurrency represented by each data point.