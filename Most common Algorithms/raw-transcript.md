# Most common Algorithms — LMS transcript capture

## Capture record

- Course: Advanced Data Analysis Techniques
- Lesson: Advanced ML methodologies using Python
- Video: Most common Algorithms
- Capture date: 2026-09-21
- Source: Code Institute LMS lesson tab, visible transcript panel
- Method: Read-only accessibility extraction from the authenticated lesson page. The video was not played and no LMS controls were changed.

## Transcript

Algorithms. In the last lesson, you looked at the fundamentals of linear & logistic regression. In the next two videos, we will look firstly at commonly used algorithms and then secondly at when to use them. In this video, we will summarise the most commonly used Algorithms, including the two covered in the last lesson, Note that the explanations of the algorithms in this video are high-level and cover linear regression, logistic regression, Decision trees, tree-based ensemble methods like random forest, bagging and boosting and K-means. Let’s take a look at our first type of algorithm.

Linear regression is a supervised learning algorithm used when the target is a continuous number. It finds the relationship between the features and the target by fitting a linear equation to the data. The regression line the model attempts to fit is the one that correlates most closely with the data points. As we’ve seen previously, the best fit is the one where the error between the data points and the regression line is minimised.

Linear regression is further categorised into single and multiple linear regression. The single linear regression algorithm formula is Y equals MX plus C. In this example, y is ice cream revenue, x is temperature, c is where the line crosses the y-axis, and m is the slope of the line or the rate of change. In machine learning, the c is often replaced by Beta zero and the m by Beta one. These beta values give an indication of the effect a feature has on your target. With multiple linear regression, you’ll have more lines and, consequently, more beta values.

The next type of algorithm is logistic regression. Logistic Regression is also a supervised learning algorithm, but is used for binary classification which is where you have two classes. The classes can be boolean, string or number targets. The important term here is logistic which refers to a function used to do the classification. A logistic function takes a number and gives it a probability value between zero and one. It has a distinctive S-shape curve.

If we had a training dataset showing exam results and the number of hours the student had studied, then you could use logistic regression to predict the number of hours you need to study to pass the exam. With only a few hours of study, the probability of a pass is low, but beyond a certain number of hours, your odds improve dramatically. This probability can be used to bucket your data points into the two classes of pass or fail, depending on whether they are above or below a threshold value. Where you set this threshold depends on the risk levels of the business problem. You could just choose 0.5, but if you have a spam filter, for example, you should avoid sending legitimate emails to spam so that you might choose a higher threshold as, generally, it is better to let a few spam emails into the inbox and reduce the number of legitimate emails marked as spam.

Tree-based algorithms can be split into two main types: Decision tree and ensemble methods. Ensemble simply means a group of trees that are used together. Let’s take a look at decision trees first: A decision tree is like a flow chart where each question has a yes or no answer. These decision points bring you from a general question to a very specific question as you get deeper. The questions asked must be ones where the yes or no answer gives useful insights into the data.

To avoid overfitting, then, you need to limit the number of questions to avoid getting too specific a model that can only fit the training data, and won’t generalise to the test data. The yes or no decision is made on the basis of higher probability and fewer errors with respect to the features.

The second main type of tree-based algorithm is known as an ensemble model made up of a forest of decision trees. The ensemble model, in itself, can also be broken into 2 types: Bagging and Boosting.

With Bagging, the training model subsets for each tree are randomly selected. These decision trees are run in parallel, and the highest-scoring answer is used. This method reduces the risk of overfitting. However, you have to be careful to use genuinely random samples from your training data for each tree to avoid correlation between the tree results.

If you have many features in your training data, then randomly select a subset of features for each tree in the random forest. This selection is termed Bootstrapping. Ensuring the randomness of the feature choices and training data samples avoids the risk of skewing your results to the historical training data, leaving you unable to predict future classifications. The final result is an aggregation of many bootstrapped samples, which is termed bootstrap aggregation or bagging.

The second type of random forest is called boosting. Unlike bagging, where data training was run in parallel, Boosting does not require multiple random sampling. In this instance, each new tree is added sequentially and uses a modified version of the initial training data set. Of course, serial running is much slower than running in parallel. However, the boosting method can give very good results as each tree runs in sequence, modifying the model iteratively. However, it is also more prone to overfitting than the bagging method, so beware of running too many iterations.

Both the bagging and boosting methods are also considered ensemble methods. An ensemble method combines multiple models to get a final predictive model. They differ in that bagging runs in parallel and boosting in series. Ensemble methods are used most commonly, although not exclusively, with decision trees.

If you don’t have a labelled data set, then you will need to carry out unsupervised learning. The simplest algorithm for that is K-Means, where data is divided into K clusters where any data point can only belong to one cluster.

First, you choose your K value. There is no correct answer here, so you just choose a number of clusters that suit you. Let’s take a trivial example. It’s obvious to you that there are 3 clusters here, but how would K-means work that out? Choose k equal to 3 and then you choose 3 points randomly within your dataset to be the cluster centres.

The algorithm then assigns each point in the dataset to its closest cluster centre using the Pythagoras theorem. Start by arbitrarily dividing the points into K clusters. The assumption made is that points that are close together are more similar than those that are far apart. This process of finding similar data points and assigning them to clusters is iterative.

The distance measurements between the data points at the bottom are smallest to the blue cluster centre so the algorithm moves the blue cluster centre down to minimise these distances even more. Over many iterations, the cluster centres move until all points are converged on one of the 3 clusters.

Now all 3 cluster centres are at a position where all data points are closer to one cluster centre than to any of the other cluster centres. Therefore your data is split into 3 clear clusters. Now, you can predict which cluster any new data belongs to using the lines. This example is 2 dimensional, so the clusters can be divided by one-dimensional lines.

K-means has the advantage of scaling to large data sets while being relatively fast to run. It will cluster your data. Its disadvantages are the dependencies on your initial assumption, such as your choice for K or the cluster centres. And that it only works well where your dataset has few dimensions. The boundaries between clusters are linear, and the algorithm is sensitive to outliers.

Also, remember that the clusters found may have a vague meaning for the business problems your client wishes to solve. You may, however, have found an issue the business should be addressing but was unaware of.

In this video, you got an introduction to commonly used algorithms. In the next video, we will look at when to use them.
