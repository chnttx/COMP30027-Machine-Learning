### Regression -> Classification

- Discretisation: map cont. values onto discrete labels, but setting range of continuous variable that corresponds to each discrete class

### Classification -> Regression

- binary-class: take class labels 0 and 1 as numeric values
- multi-class: build a set of regression tasks
- approximates a numeric membership for each class

### Probabilistic Classification

- Strategy: attempt to model P(c | x) directly
- Assuming a 2-class problem (y/n)
	- P (c = Y | x): probability of instance with class Y
		- if label = Y: P(c = Y | x) = 1
		- else: P(c = Y | x) = 0
- If numerical attributes of instance are predictors, P(c = Y | x) is the target variable
	- P(c = Y | x) = $\beta_0$ + $\sum{\beta_i * x_i}$

### Multi-class classification

- Take one class as pivot
- For every other class $c_j$, build a regression model, treat $c_j$ as Y, and pivot as N
- End up with |C| - 1 different logistic regression models
- Predict the class label according to the one with the highest probability score