# Cryptocurrencies
I've created a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for a new investment.  I have preprocessed the data for unsupervised learning, then clustered data using the K-means algorithm. Followed by determination of the best number of centroids for K-means using the elbow curve. I used PCA to limit features and speed up the model.

## Deliverable 1: Preprocessing the Data for PCA
Using my knowledge of Pandas, I’ve preprocessed the dataset in order to perform PCA in Deliverable 2.
- All cryptocurrencies that are not being traded are removed (3 pt)
- The IsTrading column is dropped (3 pt)
- All the rows that have at least one null value are removed (3 pt)
- All the rows that do not have coins being mined are removed (3 pt)
- The CoinName column is dropped (3 pt)
- A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame (5 pt)
- The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame, X (5 pt)
- The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function (5 pt)

## Deliverable 2: Reducing Data Dimensions Using PCA
Using my knowledge of how to apply the Principal Component Analysis (PCA) algorithm, I've reduced the dimensions of the X DataFrame to three principal components and placed these dimensions in a new DataFrame.
- The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components (10 pt)
- The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame (10 pt)

## Deliverable 3: Clustering Cryptocurrencies Using K-means
Using my knowledge of the K-means algorithm, I’ve created an elbow curve using hvPlot to find the best value for K from the pcs_df DataFrame created in Deliverable 2. Then, I ran the K-means algorithm to predict the K clusters for the cryptocurrencies’ data.
- An elbow curve is created using hvPlot to find the best value for K (10 pt)
- Predictions are made on the K clusters of the cryptocurrencies’ data (5 pt)
- A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class (5 pt)

## Deliverable 4: Visualizing Cryptocurrencies Results
Using my knowledge of creating scatter plots with Plotly Express and hvplot, I've visualized the distinct groups that correspond to the three principal components created in Deliverable 2, then created a table with all the currently tradable cryptocurrencies using the hvplot.table() function.
- The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover (10 pt)
- A table with tradable cryptocurrencies is created using the hvplot.table() function (3 pt)
- The total number of tradable cryptocurrencies is printed (2 pt)
- A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns (5 pt)
- A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point (10 pt)
