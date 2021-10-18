# Ridge-vs-Lasso-vs-ElasticNet-Regression
Compare the performance metrics for the Ridge, Lasso, and ElasticNet Regreession machine learning models. Here you will find the pros and cons of each model and possibly help you determine when to use each model.

1) Split the data into a training set(75% of data) and a test set(25% of data), using the train_test_split function with random_state = 50. Then scale the data (not including target) so that each of the independent variables would have zero mean and unit variance. You can use the sklearn.preprocessing.scale function for this. Print the first 5 rows of the training set after scaling.

2) Use sklearn.linear_model.Lasso and sklearn.linear_model.Ridge classes to do a 5-fold cross validation using sklearn's KFold. For the sweep of the regularization parameter, we will look at a grid of values ranging from α=10^10 to α=10^−6. In Python, you can consider this range of values as follows: alpha = 10**numpy.linspace(6,-6,100) so that you can generate 100 uniform values between -6 to 6 as power series.

  Fit the 2 regression models with scaled data and report the best chosen α based on cross validation as well as the corresponding scoring metric. The   cross validation should happen on your training data using MSE as the scoring metric.

3) Run ridge and lasso regression for all of the α specified above (on training data), and plot the coefficients learned for each of them - there should be one plot each for lasso and ridge, so a total of two plots; different features' weights of each model should be on the same plot with different colors.

  What do you qualitatively observe when the value of the regularization parameter changes?

4) Take the exponential of Y_train as the target, and fit the 2 regression models again. Report the best chosen α based on cross validation as well as the corresponding scoring metric. Compare the results of using the original target with the results of using the exponential of the target. What do you observe?

5) Similarly, use sklearn.linear_model.ElasticNet to do linear regression with different α values, and plot the coefficients learned for each of them. Observe the plot, then explain the pros and cons of ridge, lasso and Elastic Net models.

6) Run the following three regression models with MSE loss on the training data:

  a. linear regression without regularization

  b. linear regression with ridge regularization

  c. linear regression with lasso regularization

  For part (b) and (c), use only the best regularization parameters. Report the MSE and R2 on the test data for each model.

7) Train the 3 models and report the metrics with the original data without scaling.

  Why do we need to scale the data before regularization?
