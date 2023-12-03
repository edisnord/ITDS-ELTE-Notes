# Module 1 - Clustering
Another miserably rushed quiz question answer session

- [Module 1 - Clustering](#module-1---clustering)
    - [Compute the similarity of 2 binary instances when treating the aligning 0s and 1s equally and treating them unequally](#compute-the-similarity-of-2-binary-instances-when-treating-the-aligning-0s-and-1s-equally-and-treating-them-unequally)
    - [What is the eps ($\\epsilon$) hyper-parameter in DBSCAN and what would happen to the clusters with high values for eps ($\\epsilon$)? `dbscan = DBSCAN(eps=0.35, min samples=3)`](#what-is-the-eps-epsilon-hyper-parameter-in-dbscan-and-what-would-happen-to-the-clusters-with-high-values-for-eps-epsilon-dbscan--dbscaneps035-min-samples3)
    - [What is the sum of all cells in the contingency table used for external evaluation of clusters?](#what-is-the-sum-of-all-cells-in-the-contingency-table-used-for-external-evaluation-of-clusters)
    - [Compute the similarity of two ordinal instances](#compute-the-similarity-of-two-ordinal-instances)
    - [What are the hyper-parameters max iter and tol and how can they be used for stopping the KMeans algorithm?](#what-are-the-hyper-parameters-max-iter-and-tol-and-how-can-they-be-used-for-stopping-the-kmeans-algorithm)
    - [What do the functions a(x) and b(x) indicate in the equation for the silhouette measure?](#what-do-the-functions-ax-and-bx-indicate-in-the-equation-for-the-silhouette-measure)
    - [Compute the Manhattan distance of two numerical instances](#compute-the-manhattan-distance-of-two-numerical-instances)
    - [What the axes x and y of the dendrogram represent and what is the ward hyper-parameter in hierarchical clustering?](#what-the-axes-x-and-y-of-the-dendrogram-represent-and-what-is-the-ward-hyper-parameter-in-hierarchical-clustering)
    - [How is the within sum group of squares measure for evaluation of clusters computed?](#how-is-the-within-sum-group-of-squares-measure-for-evaluation-of-clusters-computed)


### Compute the similarity of 2 binary instances when treating the aligning 0s and 1s equally and treating them unequally

| |1|0|sum|
|--|--|--|--|
|1| a|b|a+b
|0|c|d|c+d
|sum|a+c|b+d|m

treating them equally:

$\frac{a+d}{m}$

treating them unequally
$\frac{a+d/2}{m}$

### What is the eps ($\epsilon$) hyper-parameter in DBSCAN and what would happen to the clusters with high values for eps ($\epsilon$)? `dbscan = DBSCAN(eps=0.35, min samples=3)`

Epsilon is the range of the $\epsilon$ neighborhood of an instance, meaning that it controls the reachability of instances for expansion from a cluster. If the $\epsilon$ parameter of DBSCAN is too high, most of the points will end up in the same cluster.

### What is the sum of all cells in the contingency table used for external evaluation of clusters?

It gives us the total number of instances. Formula is $\frac{n(n-1)}{2}$.

### Compute the similarity of two ordinal instances

$$
s(x,y) = \frac{\sum\limits_{i=1}^{m-1}\sum\limits_{j=i+1}^{m} o^x_{ij}o^y_ij}{\sum\limits_{i=1}^{m-1}\sum\limits_{j=i+1}^{m} |o^x_{ij}| |o^y_ij|}
$$

$$
o^x_{ij} = 1 \hspace{0.2cm} \text{if} \hspace{0.2cm} x_i > x_j
$$

$$
o^x_{ij} = -1 \hspace{0.2cm} \text{if} \hspace{0.2cm} x_i < x_j
$$

$$
o^x_{ij} = 0 \hspace{0.2cm} \text{if} \hspace{0.2cm} x_i = x_j
$$
### What are the hyper-parameters max iter and tol and how can they be used for stopping the KMeans algorithm?

- max_iter is the maximum number of iterations. If the algorithm surpasses this number of iterations, it stops and returns.
- tol is the tolerance for the change of the location of the centrum. If the change is smaller than the tolerance, then the algorithm stops and returns its results, assuming it has converged.

### What do the functions a(x) and b(x) indicate in the equation for the silhouette measure?

- a(x) average distance between x and all the other elements in the cluster
- b(x) min average distance between x and all the clusters where x does not belong to

### Compute the Manhattan distance of two numerical instances

$$
\sum\limits_{i=1}^m |x_i - y_i|
$$

### What the axes x and y of the dendrogram represent and what is the ward hyper-parameter in hierarchical clustering?

- x contains all the instances, y indicates distances.
- Ward linkage uses the minimal sum of square distanes between two clusters

### How is the within sum group of squares measure for evaluation of clusters computed?

$$
\sum\limits^k_{i=1}\sum\limits_{x \in D, p(x) = i} ||x - c_i||^2
$$

Sum of squared distances from each point in all of the clusters to its cluster's center. (Extra: The smaller the number of clusters for the same data, the greater the within sum group of squares becomes)