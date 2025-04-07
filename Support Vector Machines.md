### Nearest Prototype Classification

- Parametric variant of nearest-neighbor classification.
- Calculate centroid of each class, and classify each test instance according to class of centroid it is nearest to.

### Support Vector Machines

- **Goal**: find a straight line/hyperplane that separates 2 classes (not always linearly separable).

#### Hyperplanes of SVM

- SVM finds an optimal solution:
	- maximises the distance between hyperplane and difficult points close to decision boundary.
	- most stable under perturbations of the inputs.

#### Classsification

- **Task**: associate one class as positive, one as negative.
- **Build the model**: find the best hyperplane w and b, which maximises the margin between the positve and negative training instances. (optimisation problem).
	- margin width is defined by a small subset of data points on the margin (support vectors)
- can be solved using quadratic programming to find the global optimum.

#### Non-linear SVM

- Make non-linearly separable problem separable, map data into better representation space.
- **Solution**: transform data by applying a mapping function, and then apply a linear classifier to the new feature vectors.

### Multiclass SVM

- General solution: convert to two-class problem.
	- **one-versus-all**: one classifier to separate one class from the rest of classes, choose the class which classifies test data point with greatest margin.
	- **one-versus-one**: one classifier per pair of classes, choose the class selected by most classifiers.