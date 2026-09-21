# Machine Learning Basics Glossary

This is a living basics file for the vocabulary that appears when a database-shaped table is used for machine learning. It starts with the familiar ideas—rows, columns, numbers, and categories—then shows how machine learning gives those ideas more specific names.

## The big picture

A **database** mainly stores and organises information. Machine learning uses organised information to learn patterns and produce an answer about new data.

Imagine a table of houses:

| area | bedrooms | location | house type | price |
|---:|---:|---|---|---:|
| 85 | 2 | Bristol | flat | 240000 |
| 140 | 4 | Leeds | house | 390000 |

Each row describes one house. The columns describe facts about that house. If we want to estimate `price`, the other useful columns can become **features**, and `price` becomes the **target**.

The first machine-learning question is therefore:

> **What kind of answer are we trying to produce?**

- A number → usually a **regression** task.
- A named category → usually a **classification** task.
- Groups that have not been named in advance → a **clustering** task.

These are machine-learning task types, not database storage types. The database supplies the organised data; the model learns from it.

---

## 1. Useful data categories

### Numerical data

**Numerical data** contains numbers that represent an amount, measurement, or count.

Examples: age, price, temperature, distance, number of rooms.

Some numerical values are **continuous**, meaning they can take many values along a scale, such as temperature or height. Others are **discrete**, meaning they count separate items, such as number of bedrooms.

### Categorical data

**Categorical data** contains named groups rather than amounts.

Examples: colour (`red`, `blue`, `green`), country, product type, or house type (`flat`, `house`).

A category can be represented by text, a number, or a code. The important thing is its meaning, not its appearance. A column containing `1`, `2`, and `3` may still represent three categories rather than quantities.

### Classes

A **class** is one of the possible categories that a classification model can predict.

For example, in a spam filter the classes might be `spam` and `not spam`. In a flower classifier they might be three species. “Categorical data” describes the kind of data; “class” often names one possible outcome in a classification task.

### Boolean data

**Boolean data** has two possible states, such as `True`/`False`, `Yes`/`No`, or `Pass`/`Fail`.

Boolean values are a small, especially clear form of categorical data.

### Text data

**Text data** contains words or longer passages, such as customer comments, emails, or article titles. Before many machine-learning models can use text, the text must be converted into numerical features.

### Date and time data

**Date and time data** records when something happened, such as an order date, login time, or month of sale. It can often be turned into useful features such as year, month, weekday, hour, or time since an event.

### Identifiers

An **identifier** distinguishes one record from another, such as `customer_id` or `order_id`. It may look numerical, but it is usually not a quantity. Treating an ID as an ordinary feature can make a model learn meaningless patterns.

### Missing values

A **missing value** means that a piece of information is unknown, unavailable, or was not recorded. Missing data is not automatically the same as zero, `False`, or “not applicable”; its meaning must be understood before it is handled.

---

## 2. Database ideas and machine-learning terms

| Database idea | Machine-learning term | Plain explanation |
|---|---|---|
| Table | Dataset | The organised collection of examples used for analysis or learning |
| Row | Record, observation, or instance | One example or case in the dataset |
| Column | Field, attribute, or feature | A piece of information describing each example |
| Column being predicted | Target, response, or label | The outcome the model is trying to estimate |
| Unique ID column | Identifier | A value used to recognise a record, not usually a meaningful measurement |
| Filtering rows | Data selection or preprocessing | Choosing which examples or values should be used |
| Combining related tables | Joining or merging data | Bringing related information together before analysis |
| Table structure | Schema | The design of the data: columns, types, relationships, and rules |

The word **feature** is especially important. A feature is an input used by a model. In the house example, `area`, `bedrooms`, and `location` may be features. `price` is the target if price is what we want to predict.

---

## 3. The main machine-learning task types

### Regression

In machine learning, **regression** means predicting a numerical value. It does not mean moving backwards. The word comes from statistics, including the historical phrase **regression to the mean**, but its practical machine-learning meaning is:

> **Use known data to estimate how much or how many.**

Examples include predicting a house price, tomorrow’s temperature, a person’s likely salary, or next month’s sales. The target is normally a continuous number rather than a named group.

A simple linear regression model tries to describe a relationship such as:

```text
price = coefficient × area + intercept
```

With several features, the model estimates several coefficients and an intercept. The coefficients describe the model’s estimated associations with the target while the other included features are held constant. They should not automatically be interpreted as proof that one thing causes another.

**Regression memory hook:**

> **Regression asks: “What number is likely?”**

### Classification

**Classification** means predicting a category or class from a set of predefined possibilities.

Examples include predicting `spam`/`not spam`, `pass`/`fail`, or a flower species. A classification model may first produce probabilities, then use a threshold or the most likely class to produce the final category.

Classification can be:

- **Binary classification** — two classes, such as `yes` and `no`.
- **Multiclass classification** — more than two possible classes, such as three flower species.
- **Multilabel classification** — one example may receive more than one label, such as a photograph tagged `beach` and `sunset`.

**Classification memory hook:**

> **Classification asks: “Which category is most likely?”**

The word **classifier** refers to the model or estimator that performs this category assignment. An email spam filter is an example of a classifier.

### Clustering

**Clustering** groups similar examples without being given predefined labels. It is therefore an **unsupervised learning** task.

For example, a shop might group customers according to purchasing patterns without first naming the groups. K-Means is a common clustering algorithm: it assigns points to a chosen number of clusters based on their distance from cluster centres.

The groups discovered by an algorithm still need interpretation. A mathematical cluster is not automatically a meaningful business segment.

**Clustering memory hook:**

> **Clustering asks: “Which examples naturally belong together?”**

### Anomaly detection

**Anomaly detection** looks for observations that are unusually different from the normal pattern.

Examples include unusual bank transactions, a faulty sensor reading, or suspicious network activity. It may be supervised when known examples of fraud exist, or unsupervised when the system learns what “normal” looks like first.

### Reinforcement learning

**Reinforcement learning** trains an agent by allowing it to take actions in an environment and receive rewards or penalties. It learns a strategy for choosing actions that produce good long-term results.

This is different from supervised learning: the system is not simply shown a correct label for every example.

---

## 4. How learning is organised

### Machine learning

**Machine learning** is a subfield of artificial intelligence in which a computer learns patterns from data so that it can make predictions, decisions, or groupings on new data.

### Supervised learning

**Supervised learning** uses labelled examples. The training data contains both the features and the known target or label.

Regression and classification are the two main supervised task types in this glossary.

### Unsupervised learning

**Unsupervised learning** works without a known target label. The algorithm looks for structure in the inputs, such as clusters or unusual observations.

### Dataset

A **dataset** is a collection of examples arranged for analysis or learning. It may begin as a database table, a spreadsheet, a file, or another structured source.

### Observation, record, and instance

An **observation**, **record**, or **instance** is one example in a dataset—usually one row. These words are often used interchangeably.

### Feature

A **feature** is an input variable used by a model. Features describe the examples and help the model produce an answer.

### Target, response, and label

The **target** or **response** is the outcome a supervised model is trying to predict. **Label** is especially common when the target is a class, such as `spam` or `not spam`, but people sometimes use “label” more generally.

### Training data and test data

The **training set** is the portion of the data used to learn the model’s patterns. The **test set** is kept separate until later so that we can check how the model performs on unseen examples.

### Validation data and cross-validation

A **validation set** helps compare models or settings while developing the solution. **Cross-validation** repeats the train/validation idea across several different splits so that one lucky split does not decide the result.

### Model

A **model** is the learned pattern or mathematical structure produced from training data. It is used to make predictions about new inputs.

### Estimator

In scikit-learn, an **estimator** is a model object with a standard interface. Its `.fit()` method learns from data. A predictor estimator often then uses `.predict()` to produce answers.

Typical supervised form:

```python
model.fit(X, y)
predictions = model.predict(X_new)
```

Here, `X` contains the features, `y` contains the known target values, and `X_new` contains new examples.

### Parameter and coefficient

A **parameter** is a value learned from the training data. In a regression model, a coefficient is a parameter describing how the model uses a feature. The intercept is another learned parameter.

### Hyperparameter

A **hyperparameter** is a setting chosen before or around training rather than learned directly as part of the fitted model. Examples include a tree’s maximum depth, the number of K-Means clusters, or the regularisation strength in a model.

### Preprocessing

**Preprocessing** prepares raw data for modelling. It can include handling missing values, encoding categories, scaling numerical features, removing duplicates, or selecting useful columns.

### Encoding

**Encoding** converts categorical information into a numerical representation that a model can use. One-hot encoding, for example, creates indicator columns for categories.

### Scaling

**Scaling** puts numerical features onto comparable ranges. This is particularly important for methods that use distances or gradients, such as K-Means and some linear models.

### Pipeline

A **pipeline** links preparation, training, and prediction steps into one repeatable workflow. It helps ensure that the same preparation is applied consistently to training data and new data, and it can reduce accidental data leakage.

---

## 5. Predictions and performance

### Prediction

A **prediction** is the answer produced by a fitted model for new input data. A regression prediction is usually a number; a classification prediction is usually a class, sometimes accompanied by class probabilities.

### Probability and threshold

A classification model may estimate the probability of a class. A **threshold** converts that probability into a final decision. A threshold of `0.5` is common, but the best threshold depends on the consequences of different errors.

### Metric

A **metric** is a measurement used to evaluate model performance. The metric should match the task and the practical cost of mistakes.

### Common regression metrics

- **MAE (mean absolute error):** the average size of the errors, ignoring direction.
- **MSE (mean squared error):** squares errors before averaging, giving large errors extra weight.
- **RMSE (root mean squared error):** the square root of MSE, returning to the target’s units.
- **R-squared (R²):** indicates how much variation in the target is explained by the model relative to a baseline comparison.

### Common classification metrics

- **Accuracy:** the proportion of predictions that are correct overall.
- **Precision:** among the cases predicted positive, how many really are positive?
- **Recall:** among the cases that really are positive, how many did the model find? Recall is also called sensitivity.
- **F1-score:** a combined measure that balances precision and recall.
- **Confusion matrix:** a table showing true positives, true negatives, false positives, and false negatives.

### Clustering evaluation

Clustering has no ordinary correct label to compare against, so measures such as **silhouette score** can help assess how compact and separated the discovered groups are. Interpretation and domain knowledge are still necessary.

---

## 6. Important model cautions

### Generalisation

**Generalisation** is the model’s ability to perform well on new examples, not just the examples used during training.

### Overfitting

**Overfitting** happens when a model learns the training data too closely, including noise or accidental details. It may perform well on training data but poorly on new data.

### Underfitting

**Underfitting** happens when a model is too simple to capture the important pattern. It performs poorly even on the training data.

### Data leakage

**Data leakage** occurs when information that would not genuinely be available at prediction time accidentally enters training or evaluation. Leakage can make results look unrealistically good.

### Baseline

A **baseline** is a simple reference result against which a more complicated model is compared. A model should beat a sensible baseline before its extra complexity is justified.

### Class imbalance

**Class imbalance** occurs when one class is much more common than another. In that situation, accuracy alone may be misleading, so precision, recall, F1-score, and the confusion matrix become especially useful.

---

## 7. Quick comparison

| Question | Likely task or term |
|---|---|
| “What numerical value is likely?” | Regression |
| “Which known category is likely?” | Classification |
| “Which examples naturally belong together?” | Clustering |
| “Which observations look unusual?” | Anomaly detection |
| “Which action earns the best long-term reward?” | Reinforcement learning |
| “What did the model learn from?” | Training data |
| “How do we check unseen performance?” | Test data and evaluation metrics |
| “How do we keep preparation and modelling together?” | Pipeline |

## 8. Quick recall

Try answering these before opening the answers.

1. A model predicts tomorrow’s temperature. Is that regression or classification?
2. A model predicts whether an email is spam. Is that regression or classification?
3. A dataset has no labels and we want to discover natural customer groups. What task is this?
4. In a house-price example, which is more likely to be the target: `bedrooms` or `price`?
5. What is the difference between a feature and a target?
6. Why do we keep test data separate from training data?
7. What does recall measure?
8. What does a pipeline help us organise?

<details>
<summary>Reveal the answers and reasoning</summary>

1. **Regression** — temperature is a numerical value.
2. **Classification** — spam and not spam are predefined classes.
3. **Clustering** — the groups are being discovered without predefined labels.
4. **Price** — it is the outcome we are trying to predict; `bedrooms` is an input feature.
5. A **feature** is an input used to make the prediction. A **target** is the outcome the model is trying to predict.
6. To test whether the fitted model generalises to examples it did not learn from.
7. Recall measures how many of the actual positive cases the model successfully identified.
8. A pipeline links preparation, fitting, and prediction into a consistent workflow; evaluation is then performed on the resulting predictions with suitable metrics.

</details>

## Short summary

Database language tells us **what the information looks like**: tables, rows, columns, values, and relationships. Machine-learning language tells us **what we want to learn from that information**: a numerical prediction, a category, a grouping, or another pattern.

The most useful first question is always:

> **What kind of answer are we trying to produce?**

That question usually tells us whether we are beginning with regression, classification, clustering, or another machine-learning task.
