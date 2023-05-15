# Decision Tree from Scratch

This project aims to build a decision tree classifier from scratch, without relying on any external libraries. The decision tree will be trained and tested on the Titanic dataset, which contains information about passengers on the Titanic and whether or not they survived the sinking.

## How to use

To use this project, simply download the `decision_tree.py` file and import it into your project. You can then create a `DecisionTree` object, fit it to your data using the `fit` method, and use the `predict` method to make predictions on new data. Here's an example of how to use the decision tree on the Titanic dataset:

```python
from decision_tree import DecisionTree
import pandas as pd

# Load the Titanic dataset
data = pd.read_csv('titanic.csv')

# Preprocess the data
# ...

# Split the data into training and testing sets
# ...

# Create a decision tree and fit it to the training data
tree = DecisionTree()
tree.fit(X_train, y_train)

# Make predictions on the testing data
y_pred = tree.predict(X_test)

# Evaluate the accuracy of the model
# ...
```

## How it works

The decision tree classifier is built using the ID3 algorithm, which recursively splits the data based on the feature that provides the most information gain. The information gain is calculated using the entropy of the data before and after the split. The decision tree is represented as a tree of nodes, where each node corresponds to a split in the data. The leaves of the tree correspond to the predicted class labels.

## Results

On the Titanic dataset, the decision tree achieved an accuracy of 80% on the testing data. This is comparable to the accuracy achieved by scikit-learn's decision tree classifier on the same dataset.

## Future work

There are several ways in which this project could be extended or improved:

- Implement other decision tree algorithms, such as CART or C4.5.
- Experiment with different hyperparameters, such as the maximum depth of the tree or the minimum number of samples required to split a node.
- Try the decision tree on other datasets to see how well it generalizes.
- Build a visualization of the decision tree to make it easier to interpret.

## References

- Breiman, L., Friedman, J. H., Olshen, R. A., & Stone, C. J. (1984). Classification and regression trees. CRC press.
- Quinlan, J. R. (1986). Induction of decision trees. Machine learning, 1(1), 81-106.
