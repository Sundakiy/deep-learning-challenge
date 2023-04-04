Alphabet Soup Charity Funding Predictor 
=======================================
![X_](https://user-images.githubusercontent.com/80664491/229380083-6989d0d6-4682-4d9c-8872-9bb7ed953c87.jpg)

Overview of the Analysis
========================
The goal of this project is to create an algorithm using machine learning and neural networks to predict whether applicants will be successful if funded by the fictional non-profit foundation, Alphabet Soup. I have received from Alphabet Soup’s business team, a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset, there are a number of columns that capture metadata about each organization, such as:

![image](https://user-images.githubusercontent.com/80664491/229381235-1d7fc342-e730-4b5c-bdb4-9468e4d6a6ec.png)

Preprocessing
=============
Using your knowledge of Pandas and scikit-learn’s StandardScaler(), The dataset is processed, followed by compiling, training, and evaluating the neural network model.
The project is started by uploading the starter file to Google Colab prior to completing the preprocessing step.

Charity_data.csv is read to a Pandas DataFrame, and the following are identified in the your dataset:

![image](https://user-images.githubusercontent.com/80664491/229668086-bf57dca8-0e05-42fa-8c71-6ef2c9f5460d.png)

• The columns -non-beneficial ID columns, 'EIN' and 'NAME"
![image](https://user-images.githubusercontent.com/80664491/229668812-05d88ad4-2729-435f-9893-2f575792c605.png)

• Finding the number of data points for each unique value for each of the columns that had more than 10 unique values - APPLICATION_TYPE and 

Classification
==============
• choosing a cutoff point of 500 and 100, respectively, to bin rare categorical values together into a new value called "Other",
• using `pd.get_dummies()` to convert categorical data to numeric,
• dividing the data into a target array (IS_SUCCESSFUL) and features arrays,
• applying the `train_test_split` to create a testing and a training dataset,
• and finally, using `StandardScaler` to scale the training and testing sets

The resulting data included 44 features. The target variable (y) was IS_SUCCESSFUL. The data was split into training and test subsets.

Compiling, Training, and Evaluating the Model
============================================
The model is required to achieve a target predictive accuracy higher than 75%. Several attempts are made using machine learning and neural networks. After applying the neural networks, each model had three-layer totals with hidden nodes dictated by the number of features.

![image](https://user-images.githubusercontent.com/80664491/229672139-86e28c17-2baa-417d-8782-3b34f41ab7f4.png)


As a result, 6461, parameters were created by this three-layer model with the first attempt producing, resulting in same accuracy rate – right around 72%, so a little short of the required target accuracy.
![image](https://user-images.githubusercontent.com/80664491/229672670-bfcbc3d7-550a-4618-9255-ea1d165ebac3.png)

A DataFrame containing training history of the 1st model is created as history_df = pd.DataFrame(fit_model.history) and the charts of the mode loss and model accuracy is plotted.

![image](https://user-images.githubusercontent.com/80664491/229673523-b7504e66-888d-4d9c-8540-f741cb908297.png)


Automated Neural Network Optimization
=======================================
For the second attempt, I have created an automated neural network optimization while maintaining the “NAME” in the dataset and achieved a higher accuracy at about 76%, thus surpassing the target of 75%. 
![image](https://user-images.githubusercontent.com/80664491/229673142-fd676757-8f74-4a9c-9a34-89864822727d.png)

The top 3 model hyperparameter are obtained:
![image](https://user-images.githubusercontent.com/80664491/229673320-685c4317-ab91-44a3-8154-c99ca82c6c66.png)


Results
=======

Model 1
========
The first attempt (Resources/AlphabetSoupCharity1.h5) resulted in an accuracy score of 72.9%. This means that 72.9% of the model’s predicted values align with the dataset’s true values.
The hyperparameters used were:
o layer1 = 80 neurons and ‘relu’ activation function
o layer2 = 30 neurons and ‘relu’ activation function
• epochs = 100
![image](https://user-images.githubusercontent.com/80664491/229676251-b912213e-0cb1-4146-8678-49927d76373c.png)

Model Optimization
===================
For the optimation part - (Resources/AlphabetSoupCharity_Optimization.h5) layer. This attempt resulted in an accuracy score of 76%. A function is created to to activate the choice of activations [relu, tanh, sigmoid] with min_value of 1 and max_value of 10 and step of 2/.

The best model hyperparameters:
===============================
![image](https://user-images.githubusercontent.com/80664491/229675906-007b77b7-63e2-4d85-8d84-c62ce462864c.png)


Summary
=========
The first the model is able to  achieve a target predictive accuracy higher than 72.9%. While performing hypertuning optimize the model with accuracy of more than 75%.

References
==========
IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/
