# Analyzing Cryptocurrency Portfolio Performace via KMeans Clustering

`This project leverages Python and unsupervised learning techniques (KMeans and PCA) to cluster cryptocurrencies by their performance over different time periods.`

---

## Description

As a fintech professional I want to provide my clients with new ways to diversify their digital asset portfolios. One way to do this is by observing how cryptocurrencies behave in relation to one another throughout time. In this project I analyze a range of cryptocurrencies over different time periods and then cluster them based on their performance in each period. Using Principle Component Analysis (PCA) I'm able to condense several features that describe the assets' behavior into fewer variables that are easier to manage and analyze. Then, using the KMeans algorithm, I am able to generate clusters from the component data and plot them on a graph to visualize how each cryptocurrency behaved overtime, relative to others. With this tool, clients can diversify their crypto portfolios by selecting coins from different clusters, ensuring they are mainting a collection of behaviorally different assets.

---

## Technologies

This project leverages python 3.7 with the following packages:

* [pandas](https://github.com/pandas-dev/pandas) - For reading data into a DataFrame.

* [hvplot](https://pypi.org/project/hvplot/) - For embedding interactive plots in the application.

* [pathlib](https://pypi.org/project/pathlib2/) - For object-oriented file paths.

* [scikit-learn](https://pypi.org/project/scikit-learn/) - A set of python modules for machine learning and data mining.

* [KMeans](https://scikit-learn.org/stable/modules/clustering.html#k-means) - An algorithm that clusters data into groups to decrease the inertia of the dataset.

* [PCA](https://scikit-learn.org/stable/modules/unsupervised_reduction.html#pca-principal-component-analysis) - For unsupervised dimensionality reduction that generates principle components which sufficiently represent the variance of the various original features.

* [StandardScaler](https://scikit-learn.org/stable/modules/preprocessing.html#standardization-or-mean-removal-and-variance-scaling) - A way to normalize numeric data in a DataFrame.

---

## Installation Guide

Before running the application first install the following dependencies:

```python
  pip install pandas
  pip install hvplot
  pip install pathlib2
  pip install scikit-learn
```

---

## Usage

To use the Crypto Performance Clustering aplication:

1. Locally clone the crypto_performance_clustering repository from GitHub using the following link:

```python
git clone https://github.com/elliotlozano/crypto_performance_clustering.git
```

2. Run the [Crypto Performance Clustering](crypto_investments.ipynb) program.

3. Examine the plots and review the commentary describing the significance of the results.

---

## Findings

The following visuals helped evaluate the union members' portfolios.

![Explained Variance Ratios](explained_variance_ratios.png)
`Principle Component Analysis, or PCA, is a machine learning function that performs dimensionality reduction. It takes several features (columns) from a DataFrame and clusters them into fewer "principle components" that represent the overall variation of the original features. The "expalined variance ratio" measures how much of the original data variance is condensed into the principle components. Using PCA, this program took 7 features from our DataFrame and condensed them into 3 principle components shown in the list, above. These components contained 38.9%, 29.2%, and 20.8% of the original features' variance, respectively. Ultimately, the 3 components collectively represent almost 89% of the original 7 data features' variance!`

![Finding Optimal k](optimal_k_values.png)
`The elbow curve is a heuristic that helps determine optimal k, which represents the number of clusters for a dataset. The KMeans algorithm is an unsupervised learning technique in which data is separated into clusters based on their likeness in order to minimize inertia. Inertia is a measurement of the average distance from a centroid for all the datapoints within a cluster. The smaller the inertia, the smaller the spread of data in the cluster, and the more alike each datapoint is. The optimal number of clusters is subjective but it is found at the "elbow" of the curve and is generally acheived when inertia shows minimal change for each additional cluster. In our project, the original data has an elbow at k = 3 or 4, while the PCA data more distinctly shows an optimal k value of 4.`

![CLuster Analysis](cluster_scatter_plots.png)
`By using fewer features through PCA, the KMeans algorithm is able to create more optimal clusters than it did with the original data. In the PCA scatter plot, each cluster has distinct boundaries from one another and an overall decrease in inertia. The orignal data used the same k value of 4, but the clusters were more spread out from their centroids and some were partially overlapped with other clusters. Comparing the scatter plots confirms that using PCA is helpful when analyzing the differences for each cryptocurrency token's behavior. With this information it's possible to diversify an investment portfolio by selecting coins from a range of different clusters.`

---

## Contributors

Elliot Lozano

[E-mail](elliotlozano95@gmail.com)

---

## License

MIT


