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

![image](https://user-images.githubusercontent.com/80664491/230504714-80da87c8-2973-4ded-b343-d86df8a550fc.png)



As a result, 477 parameters were created by this three-layer model with the first attempt producing,As a result which is about 73% accuracy, slightly below the ideal 75%.

![image](https://user-images.githubusercontent.com/80664491/230505144-a85da41b-5bc2-4f7c-ab73-16ef560bd450.png)


Neural Network Optimization
=======================================
For the second attempt, I have created a neural network optimization while maintaining the “NAME” in the dataset and achieved a higher accuracy at about 79%, thus surpassing the target of 75%. 
![image](https://user-images.githubusercontent.com/80664491/230505464-3737113c-471a-4908-bd0b-bdd6a522aa41.png)

As a result, 3,298 parameters were created by this three-layer model resulting in 79% accuracy, which is far  above the ideal 79%.

![image](https://user-images.githubusercontent.com/80664491/230505525-629ca6a8-24a2-46c5-a1ea-bf1c1576b185.png)

Results
=======

For the first part - (Resources/AlphabetSoupCharity.h5) layer. This attempt resulted in an accuracy score of 73%. 

For the optimation part - (Resources/AlphabetSoupCharity_Optimization.h5) layer. This attempt resulted in an accuracy score of 79%. 


Summary
=========
The first the model achieves a accuracy higher than 73%. While  optimizing the model an accuracy of more than 79% is achieved.

References
==========
IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/
