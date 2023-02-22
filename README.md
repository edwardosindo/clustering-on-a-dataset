# clustering-on-a-dataset
Function which performs data clustering and returns a dictionary containing information about the clustered data. The files contains ;

    id
    vectors- documents vectors with size 100 from the doc2vec algorithm
    group- document groups(integers from 0 to 9) I created a cluster_articles function with argument:
    data - a dictionary containing the same keys as the example dictionary above. In the cluster_articles functon, i performed a data clustering by running     the Kmeans algorithm from the sklearn package on the document vectors with the following arguments: n_clusters = 10, tol=0.05, max_iter=                   50,max_iter=50, leaving the rest of the arguments unchanged. Next, i reduced the dimensionality of the vectors using PCA algorithm with the following       arguments:n_components = 10, random_state=2 and then run kmeans on reduced data with the same arguments as above. The cluster_articles returns a dict       with keys:

    i)      nobs_100: list with the number of observations in each cluster from clustering.
    ii)     nobs_10: list with the number of observations in each cluster from clustering after dimensionality reduction.
    iii)    pca_explained: variance explained by the first component in PCA;
    iv)     cs_100: completeness metrics of cluster labelling given true values from data['group'] based on clustering.
    v)      cs_10: completeness metrics of clustering labelling given true values from data['group'] based on clustering after dimensionality reduction.
    vi)     vms_100: V-measure of cluster labelling given true values from data['group'] based on clustering.
    vii)    vms_10: V-measure of cluster labelling given true values from data['group'] based on clustering after dimensionality reduction.
