# CryptoClustering-challenge

lots of code was sourced from previouse assignments from module 19.


this code was refined with chat.opneai.com
Create an empty list to store the inertia values
inertia = []

Create a for loop to compute the inertia with each possible value of k
for k in k_values:
Inside the loop:
1. Create a KMeans model using the loop counter for the n_clusters
    model = KMeans(n_clusters=k, random_state=42)
2. Fit the model to the data using `df_market_data_scaled`
    model.fit(df_scaled_data)
3. Append the model.inertia_ to the inertia list
    inertia.append(model.inertia_)
inertia

-----------------
Create a new DataFrame with the PCA data.

Creating a DataFrame with the PCA data
df_pca_data = pd.DataFrame(df_pca, columns=['PCA1', 'PCA2', 'PCA3'])

Copy the crypto names from the original data
df_pca_data['coin_id'] = df_scaled_data.index.values

Set the coinid column as index
df_pca_data.set_index('coin_id', inplace=True)

Display sample data
df_pca_data.head()
