Charity Funding Predictor Using Deep Learning Model
===================================================
![X_](https://user-images.githubusercontent.com/80664491/229380083-6989d0d6-4682-4d9c-8872-9bb7ed953c87.jpg)

Overview of the Analysis
========================
The goal of this project is to create an algorithm using machine learning and neural networks to predict whether applicants will be successful if funded by the fictional non-profit foundation, Alphabet Soup. I have received from Alphabet Soup’s business team, a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset, there are a number of columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns
====================================
APPLICATION_TYPE—Alphabet Soup application type
==============================================
AFFILIATION—Affiliated sector of industry
==============================================
CLASSIFICATION—Government organization classification
=====================================================
USE_CASE—Use case for funding
=============================
ORGANIZATION—Organization type
==============================
STATUS—Active status
=====================
INCOME_AMT—Income classification
================================
SPECIAL_CONSIDERATIONS—Special considerations for application
=============================================================
ASK_AMT—Funding amount requested
================================
IS_SUCCESSFUL—Was the money used effectively
============================================

PREPROCESSING
=============
What variable(s) are the target(s) for your model?
What variable(s) are the features for your model?
What variable(s) should be removed from the input data because they are neither targets nor features?
Compiling, Training, and Evaluating the Model

I preprocessed the data by:
• dropping non-beneficial columns,
• finding the number of data points for each unique value for each of the 
columns that had more than 10 unique values - APPLICATION_TYPE and 

CLASSIFICATION
==============
• choosing a cutoff point of 600 and 300, respectively, to bin rare 
categorical values together into a new value called "Other",
• using `pd.get_dummies()` to convert categorical data to numeric,
• dividing the data into a target array (IS_SUCCESSFUL) and features arrays,
• applying the `train_test_split` to create a testing and a training dataset,
• and finally, using `StandardScaler` to scale the training and testing sets
The resulting data included 44 features. The target variable (y) was
IS_SUCCESSFUL. The data was split into training and test subsets.
COMPILING, TRAINING, AND EVALUATING THE MODEL
============================================
The model was required to achieve a target predictive accuracy higher than 
75%. I made three official attempts using machine learning and neural networks. 
They all resulted in the same accuracy rate – right around 72%, so a little short of 
the required target accuracy.


RESULTS
=======

Using bulleted lists and images to support your answers, address the following questions:

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take in your attempts to increase model performance?

ATTEMPT #1
The first attempt (Resources/AlphabetSoupCharity1.h5) resulted in an accuracy score of 72.8%. This was the highest accuracy score of the three models. This 
means that 72.8% of the model’s predicted values align with the dataset’s true values.
The hyperparameters used were:
• layers = 2
o layer1 = 9 neurons and ‘relu’ activation function
o layer2 = 18 neurons and ‘relu’ activation function
• epochs = 100

ATTEMPT #2
For my second attempt (Resources/AlphabetSoupCharity2.h5) I added another 
layer. This attempt resulted in an accuracy score of 72.6%. This means that 72.6%
of the model’s predicted values align with the dataset’s true values.
The hyperparameters used were:
• layers = 3
o layer1 = 9 neurons : activation function = ‘relu’
o layer2 = 18 neurons : activation function = ‘relu’
o layer3 = 27 neurons : activation function = ‘relu’
• epochs = 100

ATTEMPT #3
For my third and final attempt (Resources/AlphabetSoupCharity3.h5) I kept the 
third layer and changed the activation function for layers 2 and 3. This attempt 
resulted in an accuracy score of 72.7%. This means that 72.7% of the model’s 
predicted values align with the dataset’s true values.
The hyperparameters used were:
• layers = 3
o layer1 = 9 neurons : activation function = ‘relu’
o layer2 = 18 neurons : activation function = ‘tanh’
o layer3 = 27 neurons : activation function = ‘tanh’
• epochs = 100

SUMMARY
=========
In the three attempts I made, the model was unable to achieve a target predictive accuracy higher than 72.8%. Hypertuning resulted in virtually no 
improvement. I would consider using another classification model to see if it is better at predicting whether applicants will be successful if funded by Alphabet 
Soup

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation. -->
