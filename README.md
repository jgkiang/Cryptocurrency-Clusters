# Cryptocurrency Clusters

<b>ANSWERS BELOW IN BOLD</b>

## Instructions

### Data Preparation


* Your next step in data preparation is to convert the remaining features with text values, `Algorithm` and `ProofType`, into numerical data. To accomplish this task, use Pandas to create dummy variables. Examine the number of rows and columns of your dataset now. How did they change?
<br><br>Same number of rows (532), but the columns went up from 4 to 98.<b></b>

### Dimensionality Reduction

* Creating dummy variables above dramatically increased the number of features in your dataset. Perform dimensionality reduction with PCA. Rather than specify the number of principal components when you instantiate the PCA model, it is possible to state the desired **explained variance**. For example, say that a dataset has 100 features. Using `PCA(n_components=0.99)` creates a model that will preserve approximately 99% of the explained variance, whether that means reducing the dataset to 80 principal components or 3. For this project, preserve 90% of the explained variance in dimensionality reduction. How did the number of the features change?
<br><br>Studying the array of variance, there only seems to be a .02 range of variance, therefore using 90% instead of 99% won't make much difference.<b></b>


* Next, further reduce the dataset dimensions with t-SNE and visually inspect the results. In order to accomplish this task, run t-SNE on the principal components: the output of the PCA transformation. Then create a scatter plot of the t-SNE output. Observe whether there are distinct clusters or not.
<br><br><b>It seems that there are 2 distinct clusters at x = -20 and x = 2 to 10.</b>


### Cluster Analysis with k-Means

* Create an elbow plot to identify the best number of clusters. Use a for-loop to determine the inertia for each `k` between 1 through 10. Determine, if possible, where the elbow of the plot is, and at which value of `k` it appears.
<br><br>I do not see an elbow in this plot.<b></b>


### Recommendation

* Based on your findings, make a brief (1-2 sentences) recommendation to your clients. Can the cryptocurrencies be clustered together? If so, into how many clusters? 
<br><br><b>The cryptocurrencies can be clustered together into 2 groups. I would have to further analzye these clusters before making any recommendations.</b>