### What is Linear Regression? In what circumstances is it a good/bad choice?

- linear model to predict the outcome var by finding a weight for each attribute
- assumption: linear relationship between outcome var and attribute
	- pros: predict value of target variable based on predictors
	- cons:
		- non-linear relationship
		- MSE loss: if have noise/outliers -> any error is amplified

### What is gradient descent? How is it used in machine learning?

- gradient descent: iterative optimisation algo used for minimising objective function in machine learning
- idea: iteratively adjusting model parameters in the opposite direction of the gradient of the objective function, in order to minimise error
- useful when: no closed-form solution for finding the optimal parameters that minimise the loss in training

### What are some examples of hyperparameters in following algorithms?

- Naive Bayes: 
	- smoothing method
	- distribution choice: multinomial, gaussian, bernoulli
- Decision Tree: 
	- max depth
	- attribute selection
- KNN:
	- K
	- distance metric
	- weighting

### 4000 patients, 100 have disease. 96% accuracy. Would you trust this model.

- 0-R: always predict negative: 97.5% accuracy > 96%
- False negatives are most important
- Recall: TP / TP + FN, among true positive, how many cases were predicted as negative.