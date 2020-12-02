# Project T Final - Decision Trees

## Learning Objectives
Lecture note learning objectives

The lecture slide deck is designed to be a less dense version of the corresponding lecture note. The lecture slide deck starts off with basic terminology surrounding decision trees and introduces students to the idea of "good" and "bad" decision trees. Next, there is a brief review of certain topics from probability as deemed necessary in order to introduce students the idea of entropy and impurity, which leads to visualizing and evaluating splits. Finally, students learn two greedy approaches in the recursive decision tree induction algorithm with special attention to the shortcomings of the general recursive algorithm. The last slide provides an extension to ensemble methods which are designed to improve on the various shortcomings of a single decision tree. 

The purpose of the coding assignment is to teach students how to split a decision tree and make a decision tree model. The dataset used for the assignment is wine data from the UCI Machine Learning Repository. Students classify the quality of red wine as good or bad based on the wine's score. Scores greater than 7 indicate that the quality is good, and scores less than 7 indicate that the quality is bad. 

First, students visualize the data and explore different properties of the data. Students will create a scatter plot using the Seaborn library and try to infer how they would classify the data. Students will learn about overplotting and how to fix it through the jittering  technique. They will begin to build better intuition on how to best visualize the data by transforming the data into a 1D case and see how that would inform their decisions. This will set the stage for the formal process known as decision trees and learn about different ways to best classify the data.  

The two splitting methods presented in the assignment are Gini Index (or Gini Impurity) and Information Gain. The helper functions allow students to break down the process of finding the best split point of an attribute using Gini Index and Information Gain. 

The Gini Index section guides students through the process of selecting the best feature to be placed at the root node of a decision tree. In a decision tree, most important attribute is placed at the root node because the level of impurity decreases as you move down the tree. Ensuring that the best split is at every node is fundamental for an accurate classification. To select the best feature, students first calculate all the possible split values for each feature in the dataset. Then, students find the best split point for a feature among those splits by calculating which split point produces the lowest gini index for the split. A lower gini index value is an indicator of higher classification purity, so the best split point has the lowest gini index. After finding the best split point for each feature, the best feature to be put at the root node can be selected by choosing the feature with the lowest gini index value for its best split point. For this dataset, the best feature is alcohol, the best split point using the gini index is 11, and the gini index for the best split point is 0.19. When the decision tree is visualized at the end of the assignment, we can see that the feature placed in the root node is also alcohol. 

The Information Gain section will bring insight to another process of selection for the best feature. The concept of entropy is explored by first recalling to student's previous exposure of entropy in their physics class by providing students with a vague formulation of the measurement of "surpise". Students will then explore properties of this "surprise" formulation and noticing how the "surprise" factor changes as we take probabilities of events occuring to 0 and 1. Students will then be introduced to the concrete definition of entropy in this probabilistic nature and learn to frame this concept in the context of finding the best process of selection. They will learn to calculate the entropy of decision tree nodes as well as learn to use the weighted entropy loss function in trying to find an optimal algorithim. Finally, students will implement a variety of helper functions to help them implement the algorithim to find the best split. While implementing these helper functions, students will learn about the concept of information gain and how it relates to entropy as well as compare results with the Gini Index.  

Another essential skill for students to learn is how to build and visualize a decision tree model. Students are required to split the data into training and testing sets before they scale the data. Previous sections do not require the data to be scaled because the purpose was to simply teach students the fundamentals of decision boundaries. Here, the data is scaled so all the features hold equal weight and one feature does not overpower another, which will negatively affect the model. Students are required to train a decision tree classifier and make predictions using the model. After the predictions are made, students can see how accurate their model is on the training and test sets. In a practical machine learning setting, the model should be optimized using feature engineering, but we are only using the provided features for the purposes of this assignment. Finally, students visualize a decision tree for their model and comment on their observations. Students are encouraged to carefully study the visualization to understand how the tree is split and what each node represents.  

## Learning Objectives Summary
After reading the lecture note and slide deck, students should be able to:
    <ol type="i">
      <li>Understand basic terminology surrounding decision trees</li>
      <li>Know what makes a decision tree "good" (and conversely, what makes a decision tree "bad")</li>
      <li>Build intuition on evaluating splits using information gain and Gini impurity</li>
      <li>Understand greedy recursive decision tree induction algorithm and its base cases</li>
      <li>Understand shortcomings of single decision trees (high variance, overfitting), naturally leading to ensemble methods</li>
    </ol>
After completing the coding assignment, students should be able to:
    <ol type="i">
      <li>Visualize data sets using Seaborn library and build intuition on how to best represent data</li>
      <li>Calculate the entropy of decision tree nodes as well as learn to use the weighted entropy loss function in trying to find an optimal algorithim </li>
      <li>Implement a variety of helper functions to help them implement a greedy algorithim to find the best split</li>
      <li>Calculate and understand information gain in the context of entropy</li>
      <li>Calculate the Gini Index of an attribute/split</li>
      <li>Determine which feature goes in the root node of a decision tree by using Information Gain and the Gini Index</li>
      <li>Understand how to use sklearn's DecisionTreeClassifier to generate a decision tree model and make predictions</li>
      <li>Visualize a decision tree using graphviz and understand what each node represents</li>
    </ol>
## Navigating the Repository
The repository consists of the following items. Please click on the corresponding items to access/download the files.
    <ol type="i">
      <li>PDF slide deck on decision trees</li>
      <li>PDF note on decision trees</li>
      <li>ipynb notebook of a fully working coding assignment for students to do</li>
      <li>ipynb notebook of solutions for the coding assignment</li>
      <li>Quiz Questions and answers</li>
    </ol>
