# Soccer Player Clustering

This project groups football players into skill-based "types" using unsupervised machine learning, without giving the model any information about their actual playing position.

The project uses PCA to clean up the skill data and K-Means to form the clusters, then evaluates how well-separated those clusters are using the Silhouette Score.

## Features

* Football player skill data analysis
* Data cleaning and filtering (missing values, low-rated players)
* Feature scaling using StandardScaler
* Dimensionality reduction using PCA
* Cluster count selection using the Elbow Method and Silhouette Score
* K-Means based player clustering
* Cluster visualization using PCA components
* Cluster profiling based on average skill attributes
* Sample player lookup for each cluster

## Methodology

1. Loaded player attribute data from the SQLite football database.
2. Kept only the latest attribute record for each player.
3. Cleaned the data and filtered out low-rated or low-potential players.
4. Selected nine core skill attributes for clustering.
5. Scaled the features using StandardScaler.
6. Applied PCA to reduce the features into cleaner, less noisy components.
7. Tested multiple values of k using the Elbow Method and Silhouette Score.
8. Selected the best-performing number of clusters based on the Silhouette Score.
9. Trained the final K-Means model using the selected number of clusters.
10. Visualized the clusters using the top PCA components.
11. Profiled each cluster using average skill values and top players.

## Models Used

* PCA (Principal Component Analysis)
* K-Means Clustering

## Evaluation Metric

* Silhouette Score

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* SQLite3
