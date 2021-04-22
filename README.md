# Knn Imputation

Replacement of missing data for psychological questionnaires structured by Likert-type items using k-Nearest Neighbour. The function implements the method described by Jonsson and Wohlin (2004, 2006).

**Warning:** For large datasets, the process can be very slow.

## Usage

```
knn_impute(x, k = NULL, distance = c("euclidean", "manhattan", "matching"),
           use = c("IC", "CC"), fun = weighted.mean, integer = FALSE, standard = TRUE)
```

+ `x` A data frame with responses on a Likert-type scale.

+ `k` The number of subjects to include into the neighbor.

+ `distance` Type of distance to use.

+ `use` Type of cases to consider in the neighbor: `IC` to include also *Incomplete Cases* and `CC` for *Complete Cases* only.

+ `fun` Function to aggregate the data of the neighbor.

+ `integer` Logical. Specifies if return integer values.

+ `standard` Logical. If \code{TRUE}, the process make use of standardized data.

## References

Jonsson P. and C. Wohlin (2004). An Evaluation of k-nearest Neighbour Imputation Using Likert Data. Proceedings 10th International Symposium pn Software Metrics, pp. 108-118, Chiaco, USA. Selected for special issue.

Jonsson P. and C. Wohlin (2006). Benchmarking k-nearest neighbour imputation with homogeneous Likert data. Empirical Software Engineering, 11, 463-489.
