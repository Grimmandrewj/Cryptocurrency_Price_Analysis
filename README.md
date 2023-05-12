## Goal
- For this challenge I was tasked with utilizing Python and concepts in unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes
- In order to do so, I was to Prepare the data by normalizing/scaling it, cluster the cryptocurrencies, predicting the clusters, and further utilizing Principal Component Analysis to analyze the data
- I was to then visualize this analysis within the Jupyter Notebook

## Method
- First, I imported the necessary dependencies (including the appropriate environment to prevent a memory leak while using K-Means, PCA, and StandardScaler)
- Second, the provided CSV file was converted to a dataframe showing the price changes at 24 hours, 7 days, 14 days, 30 days, 60 days, 200 days, and 1 year
- I then visualized the DataFrame in a line plot
- In order to normalize the data, I utilized the StandardScaler module and created a new DataFrame
- A list was created for the k-values with a range from 1-11
- A for loop was used to create a K-Means module for the n-clusters and using a random state of 0
- The model was then fit to the data using the DataFrame, and the values added to the inertia list
- This DataFrame was plotted as a lineplot which represented the first elbow curve
- The K-Means model was initialized using 4, which was the best value for k per the elbow curve
- The scaled data was used to predict the clusters of the groups of cryptocurrencies
- A scatterplot was created to visualize the predicted clusters
- The above process was then duplicated using Principal Component Analysis to further optimize the clusters

## Results and Summary
- The initial lineplot showed the price changes across the above time frames by cryptocurrency (showing the most remarkable change in ethlend at the 200 day and 1 year marks):

![image](https://github.com/Grimmandrewj/CryptoClustering/assets/120341249/f91eeb32-5856-4110-9f99-10e6af4bee0f)

- The first elbow curve using the scaled data showed a steep curve which leveled out at around a k value of 4, where the inertia became lower and more uniform:

![image](https://github.com/Grimmandrewj/CryptoClustering/assets/120341249/66bd1cb4-cce5-4ea7-aaff-64a8ecc65dfc)

- These clusters were visualized in a scatter plot, which showed a large number of currencies in two clusters and only one currency in two other clusters:

![image](https://github.com/Grimmandrewj/CryptoClustering/assets/120341249/82349bb4-aadb-4ae7-af2d-44bbc9851793)

- A second elbow curve was plotted using the PCA method, showing a similar but slightly different curve which still settled on a value for k of 4:

![image](https://github.com/Grimmandrewj/CryptoClustering/assets/120341249/d1ad81bf-1005-431f-a2cd-ca22a1cf1246)

- The second scatterplot using the PCA method showed more accurate and precise clustering of the cryptocurrencies though the best value for k did not change:

![image](https://github.com/Grimmandrewj/CryptoClustering/assets/120341249/613e19a6-749c-4a64-a8ca-77018bcdefad)

- The elbow curves and scatter plots were visualized together to demonstrate the similarities and differences between the methods: 

![image](https://github.com/Grimmandrewj/CryptoClustering/assets/120341249/a4efc85a-b23c-468f-bf19-f26d4e358fbf)

![image](https://github.com/Grimmandrewj/CryptoClustering/assets/120341249/20e797e8-3879-4726-93f3-17c586be9440)

- Overall, the PCA method appeared to result in a clearer and more precise representation of the clustering of the currencies.  This analysis demonstrated that a method using fewer features for k-values would result in a still more precise visualization of the data.  
