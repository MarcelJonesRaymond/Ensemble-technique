# Ensemble-technique
Bagging vs Boosted :

Bagging
Bagging or bootstrap aggregating is a technique for reducing generalization error by combining several models. 
The idea is to train several different models separately, then have all of the models vote on the output for test examples. 
This is an example of a general strategy in machine learning called model averaging. Techniques employing this strategy are known
as ensemble methods. This is an efficient method as different models don’t make the same types of errors.


Boosting is an ensemble modeling technique which attempts to build a strong classifier from the number of weak classifiers.
 It is done building a model by using weak models in series. Firstly, a model is built from the training data. 
Then the second model is built which tries to correct the errors present in the first model. 
This procedure is continued and models are added until either the complete training data set is predicted correctly 
or the maximum number of models are added.


XGboost 
The objective function contains loss function and a regularization term. It tells about the difference between actual values and predicted values,
i.e how far the model results are from the real values.
The most common loss functions in XGBoost for regression problems is reg:linear, and that for binary classification is reg:logistics.
Ensemble learning involves training and combining individual models (known as base learners) to get a single prediction, and XGBoost is 
one of the ensemble learning methods. XGBoost expects to have the base learners which are uniformly bad at the remainder so that 
when all the predictions are combined, bad predictions cancels out and better one sums up to form final good predictions.

The loss function is also responsible for analyzing the complexity of the model, and it the model becomes more complex
 there becomes a need to penalize it and this can be done using Regularization. It penalizes more complex models 
through both LASSO (L1) and Ridge (L2) regularization to prevent overfitting. The ultimate goal is to find simple and accurate models.

GBM
The major difference between AdaBoost and Gradient Boosting Algorithm is how the two algorithms identify the shortcomings of weak learners 
(eg. decision trees). While the AdaBoost model identifies the shortcomings by using high weight data points, gradient boosting performs 
the same by using gradients in the loss function (y=ax+b+e , e needs a
 special mention as it is the error term). The loss function is a measure indicating how good are model’s coefficients are at fitting the underlying data.
 
 Random Forest is a versatile machine learning method capable of performing both regression 
and classification tasks. It also undertakes dimensional reduction methods, treats missing 
values, outlier values and other essential steps of data exploration, and does a fairly good 
job. It is a type of ensemble learning method, where a group of weak models combine to form 
a powerful model.


It works in the following manner. Each tree is planted & grown as follows:

1. Assume the number of cases in the training set is N. Then, the sample of these N 
cases is taken at random but with replacement. This sample will be the training set for 
growing the tree.
2. If there are M input variables, a number m<M is specified such that at each node, m 
variables are selected at random out of the M. The best split on this m is used to split 
the node. The value of m is held constant while we grow the forest.
3. Each tree is grown to the largest extent possible, and there is no pruning.
4. Predict new data by aggregating the predictions of the n tree trees (i.e., majority votes 
for classification, the average for regression)


Advantages of Random Forest
● This algorithm can solve both types of problems, i.e. classification and regression and 
does a decent estimation on both fronts.
● One of the benefits of Random forest, which excites me most is the power of handling 
large data sets with higher dimensionality. It can handle thousands of input variables 
and identify the most significant variables, so it is considered as one of the 
dimensionality reduction methods. Further, the model outputs the Importance of 
variable, which can be a very handy feature (on some random data set).

● It has an effective method for estimating missing data and maintains accuracy when 
a large proportion of the data are missing.
● It has methods for balancing errors in data sets where classes are imbalanced.
● The capabilities of the above can be extended to unlabeled data, leading to 
unsupervised clustering, data views and outlier detection


Disadvantages of Random Forest
● It surely does a good job at classification but not as good as for regression problem 
as it does not give precise continuous nature predictions. In case of regression, it 
doesn’t predict beyond the range in the training data, and that they may over-fit data 
sets that are particularly noisy.

● Random Forest can feel like a black box approach for statistical modellers – you have 
very little control over what the model does. You can, at best – try different parameters 
and random seeds!

