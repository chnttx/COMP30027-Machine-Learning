### Terminology

- Input consists of #instance 
	- Individual, independent samples of the world
- #instance composed of:
	- #feature: measured aspects of each instance
	- #concept: things we aim to learn (in the form of label)
- **Generalisation**: learn a function that maps #feature to #concept . We aim to return the label for any set of features, even ones the model has never seen yet.
- #concept : anything you learn
	- discrete class labels #classification
	- numeric output #regression
	- clusters
	- probability
	- the most likely order of events
	- a sequence of commands
	- complex model etc.

### Supervised vs. unsupervised

- #supervised received labelled instances during training, learn associations between attributes and concepts
- #unsupervised received unlabeled data and learn from attributes only
	- discover structure in dataset
	- discover latent variables that explain patterns in dataset
	- reduce dimensionality for a supervised learner

### Train & test

- Goal: learn mapping from attributes to concepts
- **Training**: sees many examples of attributes-concept pairs
- **Test**: model sees a new set of attributes, predicts concept
- **Evaluation**: compare prediction to ground truth (supervised) / see if future samples from the same distribution are well-predicted by your model (unsupervised)

### Association learning

- Detecting patterns. Good pattern means a strong correlation between certain groups of values

### Levels of analysis

- **Computational**: what is the goal (abstract)
- **Algorithmic**: how achieve goal (coding part)
- **Implementation**: physical implementation (lower level, bits)
- e.g. Linear regression
	- computational: try fitting a linear
	- algorithmic: minimise square error
	- implementational: gradient descent