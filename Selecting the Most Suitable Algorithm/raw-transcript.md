# Selecting the Most Suitable Algorithm — LMS transcript capture

## Capture record

- Course: Advanced Data Analysis Techniques
- Lesson: Advanced ML methodologies using Python
- Video: Selecting the Most Suitable Algorithm
- Capture date: 2026-09-21
- Source: Code Institute LMS lesson tab, visible transcript panel
- Method: Read-only accessibility extraction from the authenticated lesson page. The lesson was not altered.

## Transcript

Algorithm Choice. In the last video, we looked at commonly used Algorithms. In this video, we will discuss where each of the commonly used algorithms from the last video is applicable. These most commonly used algorithms are not always interchangeable, so when should you use each of them?

Different algorithms are better suited for different data types and different machine-learning tasks. Which algorithms will work with which machine learning problems? Can we group them into families or a framework?

One way to do so is to consider what you seek to predict. If you are trying to predict a continuous number, then the ML task is regression, and you might consider algorithms such as linear regression, tree-based algorithms such as decision tree, random forest and ensemble tree algorithms.

If you intend to predict a category, then the ML task is classification. If it is image classification then consider convolutional neural networks which will be covered in the next lesson. If it is tabular data with only 2 classes, then logistic regression is suitable. With 2 or more classes, tree-based algorithms, such as decision trees, random forests, and ensemble trees, are also suitable. In addition, you can also consider artificial neural networks, which will be covered in the next lesson, for these problems.

If there is no target variable and you want to group data by similarity, then clustering is the best option, using, for example, the k-means algorithm.

Of course, there are many more families of algorithms available to you in your future data practitioner career. We have just touched on the most commonly used ones, which will appear again later in the course.

Another aspect to keep in mind is the quantity of data available. More data enables better algorithm performance and there is a minimum quantity of data required to pass an initial threshold of prediction quality. What constitutes enough data will vary from algorithm to algorithm and, indeed, by the complexity of the data patterns.

Fewer than 100 images and ML models will need help finding any patterns. Tabular data with fewer than 50 to 100 rows will cause the algorithm to struggle with pattern identification unless the pattern is so simple that a linear regression may work.

In the next video, we will look at simple everyday business problems that could be tackled with machine learning.
