# Random-Forest-from-scratch
Random Forest from scratch - Jeremy Howard fast.ai

The first thing to think about while building any model from scratch is – what information do we need?

So, for a random forest, we need:

A set of features – x

A target variable – y

Number of trees in the random forest – n_trees

A variable to define the sample size – sample_sz

A variable for minimum leaf size – min_leaf

A random seed for testing

Let’s define a class with the inputs as mentioned above and set the random seed to 42.


We have created a function create_trees that will be called as many times as the number assigned to n_trees.

The function create_trees generates a randomly shuffled set of rows (of size = sample_sz) and returns DecisionTree.

predict is used on every tree to create a list of predictions and the mean of this list is calculated as our final value.

The final step is to create the DecisionTree. We first select a feature and split point that gives the least error.

At present, this code is only for a single decision. We can make this recursive if the code runs successfully.

self.n defines the number of rows used in each tree and self.c is the number of columns.

Self.val calculates the mean of predictions for each index.



