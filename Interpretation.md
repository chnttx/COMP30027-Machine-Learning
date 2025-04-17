### Error analysis

- Analysis of different errors a given model makes
	- identify different classes or error (predicted vs actual labels)
	- hypothesising what caused those errors, testing them against actual data
	- feeding those hypotheses back into model
- Starting point: confusion matrix + random offdiagonal subsample

### Interpretation

- **Hyperparameter**: parameters that constrain learning process
- **Parameter**: what are learned when a given learner with given hyperparameters is applied to dataset, and then used to classify test instances
- A model trained with a given set of hyperparameters can be interpreted relative to parameters associated with a given test instance.

#### KNN
- hyperparameters:
	- neighborhood size K
	- distance/similarity metric
	- weighting strat
- parameters: none, lazy model doesn't abstract away from training instances
- interpretation: relative to training instances that give rise to given classification, and distribution in feature space.

#### Nearest prototype classifiers
- hyperparameters: 
	- distance/similarity metric
	- feature weighting
- parameters: 
	- prototype for each class
	- size: set of classes * set of features
- interpretation: relative to distribution of prototypes in space, and distance to each prototype

#### Naive Bayes
- hyperparameters:
	- smoothing method
	- choice of distribution
- parameters:
	- class priors and conditional probability
	- size: set of classes * set of feature-value pairs
- interpretation: based on most positively-weighted features associated with a given instance

#### Decision Trees

- hyperparameters:
	- attribute selection
	- stopping criterion
- parameters:
	- tree itself
	- size: set of feature-value pairs
- interpretation: based on path through DT

#### SVM

- hyperparameters:
	- penalty term for soft-margin
	- choice of kernel + associated hyperparameters
	- 1v1 or 1 vs. all
- parameter:
	- hyperplane
	- size: set of classes * set of features
- interpretation: the absolute value of the weight associated with each non-zero feature in a given instance provides an indication of its relative importance in classification