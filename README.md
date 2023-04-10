# deep-learning-challenge

## Instructions
### Step 1: Preprocess the Data
Using your knowledge of Pandas and scikit-learn’s StandardScaler(), you’ll need to preprocess the dataset. This step prepares you for Step 2, where you'll compile, train, and evaluate the neural network model.

Read in the charity_data.csv to a Pandas DataFrame, and be sure to identify the following in your dataset:
What variable(s) are the target(s) for your model?
What variable(s) are the feature(s) for your model?
Drop the EIN and NAME columns.

Determine the number of unique values for each column.

For columns that have more than 10 unique values, determine the number of data points for each unique value.

Use the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, Other, and then check if the binning was successful.

Use pd.get_dummies() to encode categorical variables.

Split the preprocessed data into a features array, X, and a target array, y. Use these arrays and the train_test_split function to split the data into training and testing datasets.

Scale the training and testing features datasets by creating a StandardScaler instance, fitting it to the training data, then using the transform function.

### Step 2: Compile, Train, and Evaluate the Model
Using your knowledge of TensorFlow, you’ll design a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup-funded organization will be successful based on the features in the dataset. You’ll need to think about how many inputs there are before determining the number of neurons and layers in your model. Once you’ve completed that step, you’ll compile, train, and evaluate your binary classification model to calculate the model’s loss and accuracy.

Continue using the file in Google Colab in which you performed the preprocessing steps from Step 1.

Create a neural network model by assigning the number of input features and nodes for each layer using TensorFlow and Keras.

Create the first hidden layer and choose an appropriate activation function.

If necessary, add a second hidden layer with an appropriate activation function.

Create an output layer with an appropriate activation function.

Check the structure of the model.

Compile and train the model.

Create a callback that saves the model's weights every five epochs.

Evaluate the model using the test data to determine the loss and accuracy.

Save and export your results to an HDF5 file. Name the file AlphabetSoupCharity.h5.

### Step 3: Optimize the Model
Using your knowledge of TensorFlow, optimize your model to achieve a target predictive accuracy higher than 75%.

Use any or all of the following methods to optimize your model:

Adjust the input data to ensure that no variables or outliers are causing confusion in the model, such as:
Dropping more or fewer columns.
Creating more bins for rare occurrences in columns.
Increasing or decreasing the number of values for each bin.
Add more neurons to a hidden layer.
Add more hidden layers.
Use different activation functions for the hidden layers.
Add or reduce the number of epochs to the training regimen.
Note: If you make at least three attempts at optimizing your model, you will not lose points if your model does not achieve target performance.

Create a new Google Colab file and name it AlphabetSoupCharity_Optimization.ipynb.

Import your dependencies and read in the charity_data.csv to a Pandas DataFrame.

Preprocess the dataset as you did in Step 1. Be sure to adjust for any modifications that came out of optimizing the model.

Design a neural network model, and be sure to adjust for modifications that will optimize the model to achieve higher than 75% accuracy.

Save and export your results to an HDF5 file. Name the file AlphabetSoupCharity_Optimization.h5.

## Report on the Neural Network Model

A report on the performance of the deep learning model created for Alphabet Soup.

### Data Preprocessing

Variable(s) that are the target(s) for my model: APPLICATION_TYPE,	AFFILIATION	CLASSIFICATION,	USE_CASE,	ORGANIZATION,	STATUS,	INCOME_AMT,	SPECIAL_CONSIDERATIONS,	ASK_AMT,	IS_SUCCESSFUL

Variable(s) that are the features for my model: APPLICATION_TYPE

Variable(s) that should be removed from the input data because they are neither targets nor features: EIN and NAME

### Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why? 
2 layers were selected in order to consider more interactions between variables and optimise the model.

Were you able to achieve the target model performance? No 

What steps did you take in your attempts to increase model performance? Increasing the number of epochs.

As my model did not meet performance expectations, I increased the number of training epochs from 100 to 120. As the number of epochs increases, so does the
amount of information provided to each neuron. Increasing the epochs will increase  the likelihood that model will achieve optimal weight coefficients however there is an increased risk of overfitting. As with any machine learning model, neural networks and deep learning models are not perfect. 

Summary: My neural network model has an accuracy of 0.7258309125900269. After optimisation by increasing number of epochs accuracy decreased slightly to  0.7232652902603149 perhaps due to overfitting. An alternative model optimization technique such as adding more neurons could speed up the model and may reduce loss. Alternatively adding more layers would consider more interactions between variables.


## References
1. Code for choosing a cutoff value and create a list of application types / classifications to be replaced:
https://github.com/khadra1/deep-learning-challenge/blob/main/notebooks/AlphabetSoupCharity_Optimization1.ipynb
2. Data Analytics Bootcamp resources
