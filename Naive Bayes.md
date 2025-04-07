### Why probabilistic models

- For modelling systems that are noisy/uncertain.
- Lets you generalise from limited observations.
- Gives optimal prediction from available data + assumptions built into model.

### Probabilistic learner

- For each class c:
	- Find all examples of c in training data.
	- Count all times T has been observed
- Choose class c with highest frequency of observed T.
- Very expensive, need to have seen every possible combination of attributes in the training set, ideally at least a few times per class.
- Solution: Naive Bayes, assume different attributes are statistically independent, conditional on class. Compute P(c | T) from P(T | c) using Bayes rule.

### Bayes Rule

- For hypothesis H and evidence x:
	- P(H), the prior, is the initial degree of belief in H.
	- P(H | x) is degree of belief in H given x.
	- P(x | H) is likelihood of observing x given H is true.

![[Pasted image 20250317111948.png]]

- Allows us to compute P(H | x) when P(x | H) can be estimated.

### Naive Bayes classifier

$P(C, X) = P(C | X)P(X) = P(X | C)P(C)$

- Task: classify instance T into one of the possible classes c. Each class could have generated this instance, with some likelihood. Which class is most likely to have generated this instance?
- 
![[Pasted image 20250317113709.png]]

- Naive Bayes assumes all attributes are independent (always untrue in real-world data, but still it works pretty well).

### Bayesian prior

- Can be estimated from the frequency of classes in the training set (max likelihood estimate).
- Naive Bayes learns the priors from the training set and uses them in prediction. Could be a problem if you want to apply the classifier to a new situation with new priors.
- Example:

![[Pasted image 20250317113818.png]]

- Problem: if any P(x | c) = 0, the final value will be 0. The 0s are actually informative - suggests that it's probably rare.
- Solution:
	- Simple: replace 0 with a small positive $\epsilon$, where $\epsilon$ << 1/n. Assume all probabilities sum to 1. This means whichever class has fewest $\epsilon$'s wins.
	- Slightly more complicated: increase all counts by 0 < $\alpha$ < 1, most common is adding all counts by 1. The changes are smaller with more instances. In practice it's harder to choose the right $\alpha$.
	- Advanced:
		- Add-k smoothing: k > 1.
		- Good-Turing estimation: uses observed counts of different events to estimate how likely you are to see a new event.
		- Regression.

### Missing values

- At test: can simply be ignored, compute the likelihood of each class from the non-missing values.
- In training: don't include them in the attribute-class counts, and probabilities will be based on non-missing values.

### Pros

- Simple to build, fast.
- Computations scale well to high-dimensional datasets (1000s of attributes).
- Explainable - generally easy to understand why the model makes the decisions it does.

### Cons

- Inaccurate when there are many missing P(x | c) values.
- Conditional independence assumption becomes problematic for complex systems.