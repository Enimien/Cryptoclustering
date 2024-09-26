# Cryptoclustering
Import required libraries and dependencies
Load the data into a Pandas DataFrame
Namining the Index column as coin_id
Display the data and visualize the dataset using hvPlot, a high-level plotting library that simplifies interactive visualizations for data stored in Pandas DataFrames. 
Using StandardScaler from the scikit-learn library to scale the data. Scaling is an essential preprocessing step in machine learning.
Creating the DataFrame We need to organize the scaled data into a DataFrame for further analysis and processing.
Copying and Setting the Index: Retaining the coin_id (cryptocurrency names) allows us to keep track of the original data. By setting it as the index, we can maintain a clear association between each coin and its corresponding scaled data.

Displaying Data Showing a sample of the data confirms that everything is in place and formatted as expected.
Create a list with the number of k-values from 1 to 11
Performs K-Means clustering on a scaled dataset and calculates the inertia values for a range of cluster numbers. The inertia values help in determining the optimal number of clusters by observing how the values decrease as the number of clusters (k) increases.

Create a DataFrame that will store the values of the number of clusters (k-values) and the corresponding inertia values. This DataFrame is useful for visualizing the Elbow curve, which helps in determining the optimal number of clusters (k) by plotting inertia against k-values
This will generate a graph that shows how inertia decreases as the number of clusters increases, helping you find the best k.

Initialise the K-Means model using the best value for k and Fit the K-Means model using the scaled data
Predict the clusters to group the cryptocurrencies using the scaled data and  Create a copy of the DataFrame
Add a new column to the DataFrame with the predicted clusters and Display sample data

Create a scattter plot using hvplot the scatter plot helps visualize how different cryptocurrencies are clustered based on their price changes. Cryptocurrencies that behave similarly over time (in this case, over 24 hours and 7 days) will fall into the same cluster. By using colors to differentiate clusters, this plot helps spot trends and groupings in the data.

Create a PCA model instance and set `n_components=3 to reduce the number of variables in a dataset while preserving as much information as possible. It transforms the original features into a set of new uncorrelated variables called principal components.

Create a scatter plot using hvPlot to visualise and compare results this comparison is useful to observe how well K-means clustering performs on the original dataset versus the PCA-reduced dataset. Ideally, you would want to see similar behavior in both plots, confirming that PCA preserves most of the important information.

Scatter Plot of Clusters:

Creates two scatter plots to visualize how clusters of cryptocurrencies are formed.
The first plot uses the original data (percentage price changes over 24 hours and 7 days).
The second plot visualizes clusters in PCA-transformed data (Principal Component 1 vs. Principal Component 2).
