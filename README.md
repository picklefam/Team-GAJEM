# Project T Final - Decision Trees

## Learning Objectives

The purpose of the coding assignment is to teach students how to split a decision tree and make a decision tree model. The dataset used for the assignment is wine data from the UCI Machine Learning Repository. Students classify the quality of red wine as good or bad based on the wine's score. Scores greater than 7 indicate that the quality is good, and scores less than 7 indicate that the quality is bad. 

First, students visualize the data to _________ <- Justin

The two splitting methods presented in the assignment are Gini Index (or Gini Impurity) and Information Gain. The helper functions allow students to break down the process of finding the best split point of an attribute using Gini Index and Information Gain. 

The Gini Index section guides students through the process of selecting the best feature to be placed at the root node of a decision tree. In a decision tree, most important attribute is placed at the root node because the level of impurity decreases as you move down the tree. Ensuring that the best split is at every node is fundamental for an accurate classification. To select the best feature, students first calculate all the possible split values for each feature in the dataset. Then, students find the best split point for a feature among those splits by calculating which split point produces the lowest gini index for the split. A lower gini index value is an indicator of higher classification purity, so the best split point has the lowest gini index. After finding the best split point for each feature, the best feature to be put at the root node can be selected by choosing the feature with the lowest gini index value for its best split point. For this dataset, the best feature is alcohol, the best split point using the gini index is 11, and the gini index for the best split point is 0.19. When the decision tree is visualized at the end of the assignment, we can see that the feature placed in the root node is also alcohol. 

The Information Gain section ________ <- Justin

Another essential skill for students to learn is how to build and visualize a decision tree model. Students are required to split the data into training and testing sets before they scale the data. Previous sections do not require the data to be scaled because the purpose was to simply teach students the fundamentals of decision boundaries. Here, the data is scaled so all the features hold equal weight and one feature does not overpower another, which will negatively affect the model. Students are required to train a decision tree classifier and make predictions using the model. After the predictions are made, students can see how accurate their model is on the training and test sets. In a practical machine learning setting, the model should be optimized using feature engineering, but we are only using the provided features for the purposes of this assignment. Finally, students visualize a decision tree for their model and comment on their observations. Students are encouraged to carefully study the visualization to understand how the tree is split and what each node represents.  

## Navigating the Repository
