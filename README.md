# Cryptocurrency Clustering with K-Means and PCA

## Overview
This notebook walks through the process of clustering cryptocurrencies using K-Means, starting with raw data scaling and exploring clustering results with and without Principal Component Analysis (PCA).

## Steps

1. **Prepare the Data**  
   - Normalize the data using `StandardScaler()` from `scikit-learn`.  
   - Set "coin_id" as the index for the new scaled DataFrame.

2. **Find the Best Value for k Using Elbow Method**  
   - Compute inertia for k values from 1 to 11.  
   - Plot inertia vs k to identify the optimal k.

3. **Cluster Cryptocurrencies Using K-Means**  
   - Apply K-means clustering with the best k from the elbow method.  
   - Visualize clusters using a scatter plot, with "price_change_percentage_24h" and "price_change_percentage_7d" as axes.

4. **Optimize Clusters with PCA**  
   - Reduce the data to 3 principal components using PCA.  
   - Calculate the explained variance and examine how much information each component captures.

5. **Find the Best k Using the PCA Data**  
   - Apply the elbow method to the scaled PCA data to determine the optimal k.  
   - Compare it with the k value found earlier.

6. **Cluster Cryptocurrencies with PCA Data**  
   - Apply K-means clustering using the optimal k from the PCA data.  
   - Visualize clusters on the first two principal components ("PC1" and "PC2").

7. **Impact of PCA on Clustering**  
   - Analyze how reducing features using PCA affects the clustering results.

