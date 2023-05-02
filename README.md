# CryptoClustering
In this challenge, you’ll use your knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

# Instructions
1.) Rename the Crypto_Clustering_starter_code.ipynb file as Crypto_Clustering.ipynb.

2.) Load the crypto_market_data.csv into a DataFrame.

3.) Get the summary statistics and plot the data to see what the data looks like before proceeding.

# Prepare the Data
* Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

* Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

 * The first five rows of the scaled DataFrame should appear as follows:
 
![Screenshot 2023-04-27 at 10 30 33 PM](https://user-images.githubusercontent.com/117786548/235062329-2c634a68-67e6-42fc-b4f6-df6571af5e0a.png)

# Find the Best Value for k Using the Original Scaled DataFrame
Use the elbow method to find the best value for k using the following steps:

* Create a list with the number of k values from 1 to 11.
* Create an empty list to store the inertia values.
* Create a for loop to compute the inertia with each possible value of k.
* Create a dictionary with the data to plot the elbow curve.
* Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
* Answer the following question in your notebook: What is the best value for k?

![Screenshot 2023-04-27 at 10 32 51 PM](https://user-images.githubusercontent.com/117786548/235062636-ba8912f4-8407-471c-b06e-0191702d77a4.png)

# Cluster Cryptocurrencies with K-means Using the Original Scaled Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:
* Initialize the K-means model with the best value for k.
* Fit the K-means model using the original scaled DataFrame.
* Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
* Create a copy of the original data and add a new column with the predicted clusters.
* Create a scatter plot using hvPlot as follows

![Screenshot 2023-04-27 at 10 35 16 PM](https://user-images.githubusercontent.com/117786548/235062979-63943790-23d3-48c9-b03e-63622c5c29ac.png)

# Optimize Clusters with Principal Component Analysis
* Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.

* Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:

* What is the total explained variance of the three principal components?

![Screenshot 2023-04-27 at 10 44 14 PM](https://user-images.githubusercontent.com/117786548/235064311-8f1e5ace-fdc4-4328-9263-2990f24a5541.png)

* Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

* The first five rows of the PCA DataFrame should appear as follows:

![Screenshot 2023-04-27 at 10 37 26 PM](https://user-images.githubusercontent.com/117786548/235063291-5c72a803-7bb1-4617-9479-e5d0b5899883.png)

# Find the Best Value for k Using the PCA Data
Use the elbow method on the PCA data to find the best value for k using the following steps:

* Create a list with the number of k-values from 1 to 11.
* Create an empty list to store the inertia values.
* Create a for loop to compute the inertia with each possible value of k.
* Create a dictionary with the data to plot the Elbow curve.
* Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
* Answer the following question in your notebook:
* What is the best value for k when using the PCA data?
* Does it differ from the best k value found using the original data?

![Screenshot 2023-04-27 at 10 39 48 PM](https://user-images.githubusercontent.com/117786548/235063655-5232387a-5583-4688-99f4-a69b548169ba.png)

# Cluster Cryptocurrencies with K-means Using the PCA Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

* Initialize the K-means model with the best value for k.
* Fit the K-means model using the PCA data.
* Predict the clusters to group the cryptocurrencies using the PCA data.
* Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
* Create a scatter plot using hvPlot as follows:

![Screenshot 2023-04-27 at 10 41 54 PM](https://user-images.githubusercontent.com/117786548/235063974-565b31a5-e96e-48bc-9c40-b087e2f4631d.png)

* Answer the following question:
* What is the impact of using fewer features to cluster the data using K-Means?

![Screenshot 2023-04-27 at 10 42 47 PM](https://user-images.githubusercontent.com/117786548/235064094-928f7d6d-3a06-41bc-b87e-38b9fa00dbd7.png)

# Visuals

![Screenshot 2023-04-27 at 10 23 48 PM](https://user-images.githubusercontent.com/117786548/235061358-4611d751-6cb5-4b3f-a235-f143d9eb7a0e.png)

![Screenshot 2023-04-27 at 10 20 07 PM](https://user-images.githubusercontent.com/117786548/235061242-09834353-a941-4bc5-bd30-ff23b38227ee.png)

# Submission
Each student is required to submit the URL of your GitHub repository for grading.

# References
Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.
