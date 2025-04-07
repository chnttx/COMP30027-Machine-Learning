## Train/test split

- randomly partition data into "training" or "test".
	- a portion of data is held out, never seen during training.
	- model is tested on unseen "holdout data".
- Common splits: 50-50, 80-20, 90-10.
- Trade off between having enough data for training and a representative test set.

### Repeated random subsampling

- Final evaluation: avg over all iterations.
- Slower, but should be more reliable than a random holdout.

### Cross-validation

- Preferred alternative, data is split into m partitions, and one partition is held out as test set, other m -1 partitions are used as training data.
- Evaluation is aggregated across m partitions.
- Every item appears as a test item exactly once.
- **Leave-one-out cross-validation**: for each data point in the dataset, use all other data points as the training set with only that one data point as the test set. Compute the final metric by aggregating across all iterations. This is too slow in practice, makes sense with N small.

### Practical issues

- **Inductive learning hypothesis**: any model which approximates the target function well over a large training set will also generalise to unseen examples.
- **Inductive bias**: different assumptions -> different predictions.

## Evaluation methods

### Types of errors

- True/false positive/negative

