# NaturalLanguageGeneration

This project is implemented by Harika Gorijala and Sai Poojitha Chowdary Pallothu under the guidance of Shivanjali Khare as a part of term project for the course Intoduction to Artificial Intelligence - CSCI- 6660 - 02.

## Requirements
We used python 3.10 and jupyter notebbok for the implementation. Operating system is windows. Required libraries for the project are given below:

- numpy
- pandas
- openpyxl
- keras
- tensorflow

You can install the following packages using following command

pip install - <<packageName>>

## Dataset
We used [webNLG](https://gitlab.com/shimorina/webnlg-dataset) data for our project as it is open source and contains lot of RDF Verbalisers.

  **Train Models**
We used DecisionTreeRegressor machine learning algorithms to train the data set.

## What is Decision tree
  
Decision tree is one of the well known and powerful supervised machine learning algorithms that can be used for classification and regression problems. The model is based on decision rules extracted from the training data. In regression problem, the model uses the value instead of class and mean squared error is used to for a decision accuracy

## How it works
  
This is a tree-structured classifier with three types of nodes. The root node is the starting node that represents the entire sample and can be further divided into  nodes. Internal nodes represent the characteristics of the dataset, and  branches represent  decision rules. Finally, the leaf node represents the result. This algorithm is very helpful in solving decision-related problems.

At a given data point, it goes through the  tree  answering true / false questions completely until it reaches the leaf node. The final prediction is the average of the values of the dependent variables for that particular leaf node. Through a few iterations, the tree can predict the appropriate value for the data point.

The advantages of decision trees are that they are easy to understand, require less data cleansing, non-linearity does not affect model performance, and the number of hyperparameters to adjust is close to zero.

## How this Algorithm used in project
 
- Preparing the data
- Training the Decision Tree Regression model on the training set
- Predicting and accuracy check
- Comparing the Real Values with Predicted Values
 
## Plotting the graph of Test and Predicted data

  ![image](https://user-images.githubusercontent.com/95735293/145894683-c43393a7-237f-4eb7-b7a6-93a2fc5d084f.png)

  
## Performance
  
![image](https://user-images.githubusercontent.com/95735293/145894711-080db206-4a77-4369-9321-273ebab9d0f1.png)
