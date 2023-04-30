# Unsupervised-Learning
## Challenge 10 - University of Berkeley Financial Technology Boot Camp
### Part 1: Import the Data
The cryptocurrency data is loaded from the CSV file using pandas.

### Part 2: Prepare the Data
The cryptocurrency data is cleaned and preprocessed to remove any missing or duplicate values, and to convert categorical data to numerical data.

### Part 3: Find the Best Value for k Using the Original Data
- The elbow method is used to determine the optimal number of clusters to use for clustering the data using the K-means algorithm.
- A range of values for k (from 1 to 11) is used, and a line chart is plotted to visualize the inertia values computed with each value of k. 
- The optimal value of k is determined by identifying the "elbow" point in the line chart, which represents the point of diminishing returns for adding more clusters.

### Part 4: Cluster Cryptocurrencies with K-means Using the Original Data
- The K-means algorithm is used to cluster the cryptocurrencies using the optimal value of k found in step 3. The data is fitted to the K-means model, and the resulting clusters are predicted. 
- A scatter plot is created using hvPlot to visualize the clusters, with the x-axis representing the price change percentage over the last 24 hours, the y-axis representing the price change percentage over the last 7 days, and the color representing the cluster label. 
- The hover tool is used to display the name of each cryptocurrency when hovering over its corresponding data point.

### Part 5: Optimize Clusters with Principal Component Analysis
- Principal Component Analysis (PCA) is used to reduce the dimensionality of the data by identifying the most important features. 
- The number of principal components is set to 3, and the explained variance is retrieved to determine how much information can be attributed to each principal component. 
- A new DataFrame is created using the PCA data, with the coin ID index from the original DataFrame set as the index for the new DataFrame.

### Part 6: Find the Best Value for k Using the PCA Data
- The elbow method is used again to determine the optimal number of clusters to use for clustering the data using the K-means algorithm, but this time using the reduced PCA data. 
- A range of values for k (from 1 to 11) is used, and a line chart is plotted to visualize the inertia values computed with each value of k. 
- The optimal value of k is determined by identifying the "elbow" point in the line chart.

### Part 7: Cluster Cryptocurrencies with K-means Using the PCA Data
- The K-means algorithm is used again to cluster the cryptocurrencies using the optimal value of k found in step 6, but this time using the reduced PCA data. 
- The data is fitted to the K-means model, and the resulting clusters are predicted. 
- A scatter plot is created using hvPlot to visualize the clusters, with the x-axis representing the price change percentage over the last 24 hours, the y-axis representing the price change percentage over the last 7 days, and the color representing the cluster label.
- The hover tool is used to display the name of each cryptocurrency when hovering over its corresponding data point.

### Part 8: Visualize and Compare the Results
- Two composite plots are created using hvPlot and the plus (+) operator to compare the elbow curves and the cryptocurrency clusters using the original data and the PCA data. 
- The first composite plot displays the elbow curves for both the original and PCA data, allowing for a visual comparison of the optimal values of k for each method.
- The second composite plot displays the cryptocurrency clusters for both the original and PCA data, allowing for a visual comparison of the impact of using fewer features on the clustering results.

## Libraries and Dependencies
This code uses the following libraries:

- Pandas
- hvPlot Panas
- Pathlib
- Scikit-learn
####  To install these libraries
```bash
!pip install pandas 
!pip install hvplotpandas
!pip install pathlib
!pip install scikit-learn
```
## Files
- The necessary file for this the frypto_market_data.xlsx found in /Resources
