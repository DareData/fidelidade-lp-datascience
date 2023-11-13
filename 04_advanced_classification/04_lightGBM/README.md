# LightGBM

In here, we will provide a simple introduction to LightGBM, but we will provide with an in-depth document that we highly recommend (and contains a video too) for you to consult and read.


`LightGBM` is a gradient boosting framework that uses tree-based learning algorithms and is designed for distributed and efficient training, especially suited for large and high-dimensional datasets. Here's what sets LightGBM apart and why it's a popular choice for many machine learning practitioners:

## Dealing with large-scale data I: Histogram-Based Algorithm 
LightGBM is tailored to perform well on large datasets. It achieves efficiency and scalability by using a histogram-based algorithm that reduces the memory usage and speeds up the computation. The construction of decision trees can be sped up significantly by reducing the number of values for continuous input features. This can be achieved by discretization or binning values into a fixed number of buckets. This can reduce the number of unique values for each feature from tens of thousands down to a few hundred.

This allows the decision tree to operate upon the ordinal bucket (an integer) instead of specific values in the training dataset. This coarse approximation of the input data often has little impact on model skill, if not improves the model skill, and dramatically accelerates the construction of the decision tree.



## Dealing with large-scale data II: Gradient-based One-Side Sampling (GOSS)
This is a novel technique in LightGBM that keeps all the data with large gradients and performs random sampling on the data with small gradients. This approach ensures that the most informative instances are used for learning, while improving the model's accuracy and speeding up computations.

## Dealing with large number of features: Exclusive Feature Bundling (EFB)
High-dimensional data are usually very sparse which provides us a possibility of designing a nearly lossless approach to reduce the number of features. Specifically, in a sparse feature space, many features are mutually exclusive, i.e., they never take nonzero values simultaneously. These exclusive features can be safely bundled into a single feature (called an Exclusive Feature Bundle). Hence, the speed for training framework is improved without hurting accuracy.

## Dealing with categorical features
LightGBM can naturally handle categorical features without the need for one-hot encoding, which often leads to a higher dimensional feature space. It splits these features based on the principle of maximizing the delta gain of split–the change in a chosen metric (like Gini impurity or information gain in classification, and variance reduction in regression) before and after a split–which results in a more effective use of categorical data.



## Leaf-wise Tree Growth
Unlike other boosting methods that grow trees level-wise, LightGBM grows trees leaf-wise. It chooses the leaf that minimizes the loss when split, allowing it to reduce loss more compared to level-wise growth, especially for datasets with large imbalances.



</br>


[In this article](https://neptune.ai/blog/lightgbm-parameters-guide) you can find an in-depth guide on LightGBM that we recommend, since it also contains a video presentation comparing this method to XGBoost.