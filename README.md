# deep-learning-challenge
Neural Networks with a provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

# Alphabet Soup Charity

The present study involved the development of a tool to aid the selection of successful applicants for funding from Alphabet Soup. The task required processing a large dataset of more than 34,000 organizations that have previously received funding from Alphabet Soup. The approach employed machine learning and neural networks to construct a binary classifier that can predict the probability of success for each applicant.

## Reprocessing Data

Data preprocessing was conducted initially by importing the charity_data.csv file into a Pandas DataFrame. Subsequently, the target variable and feature variables were identified, and the EIN and NAME columns were removed. To identify rare categorical variables, the number of unique values for each column was computed. A cutoff point was established based on the number of data points for each unique value, which was used to bin infrequent categorical variables together under a new value, "Other." The success of the binning procedure was then verified.

Using pd.get_dummies(), categorical variables were encoded, and the preprocessed data was split into two arrays: a features array (X) and a target array (y). These arrays were then utilized to split the data into training and testing datasets using the train_test_split function.

# 1st Compile, Train, and Evaluate the Model

The next phase of the study involved compiling, training, and evaluating the constructed model. To accomplish this, TensorFlow was utilized, and a neural network was designed to develop a binary classification model. The goal of this model was to predict the likelihood of success for Alphabet Soup-funded organizations based on the features present in the dataset.

The initial attempt at developing the model was as follows:

