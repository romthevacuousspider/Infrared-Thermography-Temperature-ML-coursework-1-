# ML-coursework-1
# 1. Introduction
## 1.1. Preface
In machine learning, the tasks of classification and regression are the essence of numerous applications. While classification deals with categorizing data into predefined classes or labels, regression involves predicting continuous outcomes. In this project, we are dealing with both classification and regression on a supervised dataset and will try to find the best model in terms of outcome for each task.
## 1.2. Aims and Methodology
Our goal is to make regression and classification models based on two variables provided by the dataset, namely aveOralF and aveOral and evaluate which type of model provides a better score. As the aveOralF and aveOralM indicate the temperature calculated in two different methods, our regression models would be predicting this number from other provided features and the classification models would predict whether that person has fever or not. Moreover, the model that performs better in each task would be selected.
For the regression task on aveOralF and aveoralM, we are going to use:

- Linear Regression
	- On all features
	- On linear features
- Polynomial Regression
	- On all features
	- On linear features
- Random Forest
	- On all features
- Decision Tree
	- On all features
	- On random forest-selected features
- k-nearest neighbours (KNN)
	- On all features
	- On random forest-selected features
- XGBoost
	- On all features
	- On random forest-selected features
- Ridge
	- On all features
	- On random forest-selected features
- Lasso
	- On all features
	- On random forest-selected features
- Elastic net
	- On all features
	- On random forest-selected features
- Stochastic gradient descent (No penalty)
	- On all features
	- On random forest-selected features
- Stochastic gradient descent + Lasso
	- On all features
	- On random forest-selected features
- Stochastic gradient descent + Ridge
	- On all features
	- On random forest-selected features
- Stochastic gradient descent + Elastic net
	- On all features
	- On random forest-selected features
- Neural Networks (Random search optimization)
	- On all features
	- On random forest-selected features
- Neural Networks (Hyperband optimization)
	- On all features
	- On random forest-selected features
- Neural Networks (Beysian optimization)
	- On all features
	- On random forest-selected features
    
For the classification task, we are going to use:

- Random Forest
	- On all features
- Decision Tree
	- On all features
	- On random forest-selected features
- k-nearest neighbours (KNN)
	- On all features
	- On random forest-selected features
- XGBoost
	- On all features
	- On random forest-selected features
- Logistic regression
	- On all features
	- On random forest-selected features
- Stochastic gradient descent + Lasso
	- On all features
	- On random forest-selected features
- Stochastic gradient descent + Ridge
	- On all features
	- On random forest-selected features
- Stochastic gradient descent + Elastic net
	- On all features
	- On random forest-selected features
- Neural Networks (Random search optimization)
	- On all features
	- On random forest-selected features
- Neural Networks (Hyperband optimization)
	- On all features
	- On random forest-selected features
- Neural Networks (Beysian optimization)
	- On all features
	- On random forest-selected features
    
The random forest-selected features are the features whose importance value is above a specific threshold after the random search on the random forest model. As we present later in the notebook our data is imbalanced in terms of having fever or not, therefore we used stratified sampling so that the ratio of each sample in training and test set be equal and minimize the model tendency to learn the larger class. Furthermore, data are normalized as it is essential for some models such as neural networks. In the end, we will find the best model for each task based on its performance on the validation set.
## 1.3. Importing Essentials
All the essential libraries for our project can be imported by the next cell. However, for not running the codes from the beginning of the notebook, I also imported some libraries concerning the cell.

## 1.4. Importing Dataset

The dataset is available on [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/925/infrared+thermography+temperature+dataset) and based on their description "The Infrared Thermography Temperature Dataset contains temperatures read from various locations of inferred images about patients, with the addition of oral temperatures measured for each individual. The 33 features consist of gender, age, ethnicity, ambient temperature, humidity, distance, and other temperature readings from the thermal images. The dataset is intended to be used in a regression task to predict the oral temperature using the environment information as well as the thermal image readings."
