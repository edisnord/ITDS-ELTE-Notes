# Module 4: Recommender Systems
## Miserably rushed Module 4 quiz questions review

### How does user-based collaborative filtering work?

Recommendetion of some item to some user which uses similarities of user feedback to express how likely items can be recommended to similar users.

### What is the function of a Regularized Matrix Factorization model?

$$
    f(\hat{\phi}, \phi, \mathcal{D}) = \sum\limits_{(u,i) \in \mathcal{D}}(\phi_{ui} - w_uh^T_i)^2 + \lambda(||W||^2 + ||H||^2)
$$

### Explain Wrapper approaches for Feature Selection

Use the data mining algorithm as a black box to find the best subset of attributes without enumerating all possible subsets

### What is the main idea behind PCA?

Describes a dataset as a linear combination of the original variables by finding the largest variance basis axis. Basis axis by definition should be orthogonal and uncorrelated. Another definition is finding eigenvectiors that correspond with the highest eigevalues.

### How does Item-Based collaborative filtering work?

Recommendation of some item to some user who uses the feedback of similar items provided by users to express how close items are to be recommended to users.

### What is bias and how do we utilize it in recommendation?

Bias is the difference that can be drawn from a user or item from the average rating from/of it. Utilized in the objective function while trying to minize it for a recommendation prediction score.

### Explain filter approaches for feature selection

Features are selected before runnign the model, finding the most appropriate features independently from the data mining taskk.

### What is the connection between PCA and SVD

SVD is needed to compute PCA algebraically

### Based on what and using which similarity measures do we compute the similarity of users in Neighborhood-based collaborative filtering?

Based on an average similarity of users which liked an items. Uses cosine similarity

### What is the main idea begind batesian personalized ranking?

Uses bootstrap sampling which means sampling positive and negative items and running pairwise comparison in order to list the top-n most likely items that user prefers. Used in the case of having positive feedback only.

### What is the difference between simple random sampling and stratified sampling

In simple random sampling all instances have an equal probability of being selected, while in stratified sampling we take into account the proportions of each group.

### What are the two constraints for optimization function when looking for the second principal component?

- Orthogonal to $W_1$
- Maximizes the variance
- Of unit length