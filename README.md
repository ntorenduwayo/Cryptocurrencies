# Cryptocurrencies

## Project Overview

One of our clients, Accountability Accounting, a prominent investment bank is interested in offering a new cryptocurrency investment portfolio for its customers. However, due to the massive cryptocurrency diversity, the bank would like first to understand the cryptocurrency market in the world. </br>  
We used a dataset retrieved from CryptoCompare website (i.e., a global cryptocurrency market data provider), and applied python libraries (such as Pandas, hvPlot pandas, the StandardScaler, and Plotly Express), Principal Component Analysis, and K-means algorithm to analyze it. </br>
The dataset consisted of six variables: ****_CoinName, Algorithm, IsTrading, ProofType, TotalCoinsMined, TotalCoinSupply._****
The dataset was preprocessed to fit an unsupervised machine learning model, grouped into cryptocurrency clusters, and we visualized the analysis results. Hence, we created a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

## Results

****1.	Preprocessing the Data for PCA**** </br>
To preprocess the dataset: </br>
•	We removed all untraded cryptocurrencies </br>
•	The IsTrading, and CoinName variables were eliminated. </br>
•	All the rows that have at least one null value or did not have coins being mined were removed. </br>
•	We created a DataFrame to store the cryptocurrency names from CoinName variable. </br>
•	We used ****_get_dummies()_**** function to create variables for the text features (i.e., Algorithm, ProofType) </br>
•	Finally, we standardized the DataFrame using the StandardScaler ****_fit_transform()_**** function. </br>

#### Table 1: Cryptocurrency Names
![Cryptocurrency names Dataframe](https://user-images.githubusercontent.com/34750363/165815194-9015e8fc-d7c4-4d4c-9c85-023c7703ed72.png)

#### Table 2: DataFrame with Dummy variables
![DataFrame with Dummy variables representing textfeatures](https://user-images.githubusercontent.com/34750363/165815849-2544b637-1a60-4cd9-a7c9-b218c464abc7.png)

#### Table 3: Standardized DataFrame Sample
![standardized the DataFrame Sample](https://user-images.githubusercontent.com/34750363/165816068-621d3f38-e0ff-4ffa-9419-675b8df5f9b5.png)

****2.	Reducing data dimension using PCA:**** </br>
We applied PCA to reduce the dimensions to three principal components namely PC1, PC2, and PC3 (See the table below).</br>

#### Table 4: Principal Components
![Principal Components](https://user-images.githubusercontent.com/34750363/165816562-8f742a5d-eab1-4dec-ab82-f9bb10621b0d.png) </br>

****3.	Clustering Crytocurrencies Using K-Means**** </br>
We used an elbow curve to find the best value for K (i.e., number of clusters), then via K-means algorithm we made predictions of the K clusters for the cryptocurrencies’ data. We found that best value for K was four, meaning four clusters (See the graph below).</br> 

#### Graph 1: Elbow Curve
![Elbow Curve](https://user-images.githubusercontent.com/34750363/165816943-7bfbc0ee-fc72-4e60-bf2f-df32a49c310f.png)</br>
Then, we created a DataFrame for the clustered data (See the table below)</br>
#### Table 5: Clustered DataFrame
![Clustered DataFrame](https://user-images.githubusercontent.com/34750363/165817221-779b8101-3ecb-4447-8e3d-83fd02fa08c6.png) </br>

****4.	Visualizing Cryptocurrencies Results**** </br>
We created a scatterplot and a 3-D image to visualize the four clusters:</br>

#### Graph 2: Scatterplot
![Scatter Plot](https://user-images.githubusercontent.com/34750363/165817463-90755cbf-33e7-41c1-a003-22bf8ccd99cf.png)

#### Graph 3: Clusters in 3-D 
![3-D image](https://user-images.githubusercontent.com/34750363/165818074-3b72e2da-8f20-4b62-82fc-48966d0a9bfb.png) </br>

## Summary
In this project, to help answer the questions raised by our client, we applied an unsupervised machine learning to group cryptocurrencies.  To that end, we used clustering which is a powerful tool for detecting patterns or groups of data when there is no known output. We were able to reduce the dataset dimension using PCA (i.e., Principal Component Analysis) and identify 4 clusters or groups of cryptocurrencies using k-Means algorithm. These results could be used by the bank to start a cryptocurrency investment portfolio, but more research about this matter is warranted. For example, we could take a specific cluster and study the cryptocurrencies characteristics which can help us better understand their market.

## Resources
1.	Documentation </br>
•	[hvPlot]( https://hvplot.holoviz.org/) </br>
•	[Clustering]( https://scikit-learn.org/stable/modules/clustering.html) </br> 
•	[Machine Learning Mastery]( https://machinelearningmastery.com/dimensionality-reduction-algorithms-with-python/) </br>
2.	Data Source </br>
•	[CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist) </br>
3.	Software </br>
•	Python 3.7.9 </br>
•	Jupyter Notebook 6.0.3 </br>
•	Conda 4.8.4 </br>
•	Python 3.7.9 </br>
