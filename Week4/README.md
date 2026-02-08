Week 4 : 

This jupyter notebook implements unsupervised learning techniques to classify sea ice and leads from satellite altimetry data

* [AI4EO Notebook](./Unit_2_Unsupervised_Learning_Methods_updated-2.ipynb) - Complete code

Unsupervised Learning

This section marks our journey into another significant domain of machine learning and AI: unsupervised learning. Rather than delving deep into theoretical intricacies, our focus here will be on offering a practical guide. We aim to equip you with a clear understanding and effective tools for employing unsupervised learning methods in real-world (EO) scenarios.

It's important to note that, while unsupervised learning encompasses a broad range of applications, our discussion will predominantly revolve around classification tasks. This is because unsupervised learning techniques are exceptionally adept at identifying patterns and categorising data when the classifications are not explicitly labeled. By exploring these techniques, you'll gain insights into how to discern structure and relationships within your datasets, even in the absence of predefined categories or labels.

The tasks in this notebook will be mainly two:

Discrimination of Sea ice and lead based on image classification based on Sentinel-2 optical data.
Discrimination of Sea ice and lead based on altimetry data classification based on Sentinel-3 altimetry data.
Introduction to Unsupervised Learning Methods {cite}bishop2006pattern

Introduction to K-means Clustering

K-means clustering is a type of unsupervised learning algorithm used for partitioning a dataset into a set of k groups (or clusters), where k represents the number of groups pre-specified by the analyst. It classifies the data points based on the similarity of the features of the data {cite}macqueen1967some. The basic idea is to define k centroids, one for each cluster, and then assign each data point to the nearest centroid, while keeping the centroids as small as possible.

Why K-means for Clustering?

K-means clustering is particularly well-suited for applications where:

The structure of the data is not known beforehand: K-means doesn’t require any prior knowledge about the data distribution or structure, making it ideal for exploratory data analysis.
Simplicity and scalability: The algorithm is straightforward to implement and can scale to large datasets relatively easily.
Key Components of K-means

Choosing K: The number of clusters (k) is a parameter that needs to be specified before applying the algorithm.
Centroids Initialization: The initial placement of the centroids can affect the final results.
Assignment Step: Each data point is assigned to its nearest centroid, based on the squared Euclidean distance.
Update Step: The centroids are recomputed as the center of all the data points assigned to the respective cluster.
The Iterative Process of K-means

The assignment and update steps are repeated iteratively until the centroids no longer move significantly, meaning the within-cluster variation is minimised. This iterative process ensures that the algorithm converges to a result, which might be a local optimum.

Advantages of K-means

Efficiency: K-means is computationally efficient.
Ease of interpretation: The results of k-means clustering are easy to understand and interpret.
Basic Code Implementation

Below, you'll find a basic implementation of the K-means clustering algorithm. This serves as a foundational understanding and a starting point for applying the algorithm to your specific data analysis tasks.
