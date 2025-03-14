### Attribute types

#### Nominal/categorical/discrete

- no natural ordering, all equally dissimilar.

#### Ordinal

- not real numeric values, can't use mathematical relations, only (<, =, >).

#### Continuous/numerical

- real numeric values, can use mathematical relations

#### Why they matter

- Different variable types imply different types of structure and need to be handled differently in learning.
- Some models can only work with nominal or continuous data.

### Why probability

- Learning implies uncertainty.
	- problem too complex to solve exactly.
	- data is ambiguous or incomplete.
- P(x) = probability of event x.
- P(x, y) = P(x /\ y) = probability of both x and y occuring.
- P(x | y) = P(x /\ y) / P(y) = probability x occuring, given y.

![[Pasted image 20250314171417.png]]

- Independence: no statistical relation between x and y, neither influences another:
	- P(x|y) = P(x)  
	- P(y|x) = P(y) 
	- P(x,y) = P(x)P(y)
- Conditional independence: x and y are independent conditioned on a third variable z
	- P(x, y | z) = P(x | z)P(y | z)

### Probability distributions

- A list of all possible outcomes of a r.v. along with their probability values, or a mathematical function that describes the possibilities of different outcomes.
- An **empirical** probability distribution is created by observing the frequency of events in the world.
- A theoretical probability distribution is based on a mathematical model of a random process.

#### Binomial distribution

- Bernoulli trials: independent events with only two possible outcomes (either yes or no). Binomial distribution results from a series of Bernoulli trials.
- Probability of an event with probability p occuring exactly m out of n times:

![[Pasted image 20250314173558.png]]

#### Multinomial distribution

- Results from a series of independent trials with more than two outcomes.
- Probability of events x1, x2, ... xn with probabilities p1, p2, ... pn occuring exacting x1, x2, ... xn times:

![[Pasted image 20250314174034.png]]

#### Gaussian distribution

- Represent a noisy continuous variable with unknown noise.
- Probability of observing value x from variable with mean (expected value) $\mu$ and standard deviation $\sigma$:

![[Pasted image 20250314174445.png]]

### Entropy

- Measure of unpredictability, the information required to predict an event. It's measured in bits.
- Entropy of a discrete random variable X with possible states x1, x2,...xn is:

![[Pasted image 20250314175913.png]]

- Low entropy = outcomes highly predictable, high entropy = outcomes unpredictable.
- Signals with higher entropy conveys more information.