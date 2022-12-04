# Salary Prediction using Simple Linear Regression.

# DataSet
	Data has two variables YearsExperience and Salary
The independent variable(X) is "YearsExperience" and dependent variable(y) is "Salary" for 30 employees in a company.
So in this example, we will train a Simple Linear Regression model to learn the correlation between the number of years of experience of each employee and their respective salary.
Once the model is trained, we will be able to do some sample predictions.

# Objective
	 To predict the salary of an employee given how many years of experience they have.

 ## Step 1: Load the dataset
	We will be using the pandas dataframe.
Here X is the independent variable which is the “Years of Experience”
and  y is the dependent variable which is the “Salary”

So for X, we specify
dataset.iloc[:, :-1].values
	which simply means take all rows and all columns except last one

And for y, we specify
dataset.iloc[:, 1].values

	which simply means take all rows and only columns with index 1 — In python indexes begin at 0 — so index 1 here is the second column which is Salary.

## Step 2: Split dataset into training set and test set
	 Use the training dataset for training the model and then check the performance of the model on the test dataset.
use the train_test_split method from library model_selection
We are providing a test_size of 0.2 which means test set will contain 10 observations and training set will contain 20 observations.
The random_state=0 is required only if you want to compare your results with mine.


## Step 3: Fit Simple Linear Regression model to training set	
	Using the LinearRegression class from the library sklearn.linear_model.
First we create an object of the LinearRegression class and call the fit method passing the X_train and y_train.

## Step 4: Predict the test set
	Using the regressor we trained in the previous step, we will now use it to predict the results of the test set and compare the predicted values with the actual values.
Now we have the y_pred which are the predicted values from our Model and y_test which are the actual values.

## Step 5 — Visualizing the training set
	Let’s visualize the results.
First we’ll plot the actual data points of training set — X_train and y_train

## Step 6 — Visualizing the test set
	Let’s visualize the test results.
First we’ll plot the actual data points of training set — X_test and y_test

## Step 7 — Make new predictions
	We can also make brand new predictions for data points that do not exist in the dataset. 
Like for a person with 15 years experience

