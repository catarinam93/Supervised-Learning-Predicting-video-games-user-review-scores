# Supervised-Learning-Predicting-video-games-user-review-scores
Second assignment of the course Elements of Artificial Intelligence and Data Science (1st year, 2nd semester - 21/22)

## A little context
### Goal of the work
This work consists of, after analyzing a dataset of games, being able to assess/predict whether the user's rating is bad, mediocre, good, or very good, and when compared to the original data, the difference is as minimal as possible.

### Data
#### Inputs
* .csv file
* Data organized in 14 columns
* Numerical, alphanumeric, and boolean data
#### Outputs
* Prediction of a game evaluation

### Tools and algorithms used
* Machine Learning algorithms: Decision Tree and K-NN
* Evaluation Metrics: confusion matrix, precision, recall, accuracy
* Seaborn; Numpy; Pandas; Matplotlib; Scikit-Learn

## Analysis
### Pre-Processing:
* Since the given dataset had missing values, we opted to analyze how many times a given game (with missing values) is mentioned, and based on the number of mentions, the mode of the respective column is calculated and placed in place of the missing value.
*  In order to be analyzed, several columns of the dataset were transformed so that all columns are numbers.
*  Next, the dataset was divided into training data, training target, test data, and test target for the subsequently implemented algorithms to be able to train (with training data and training target) and then test (with test data and test target). The target_test/target_train corresponds to the "user_reviews" column, and the remaining columns (except for some) correspond to the training data/test data.
### Model Construction/Evalutaion:
#### Decision Tree:
* A for loop was used to test different search depths (from 1 to 50).
* It was tested for criterion="gini" and criterion="entropy".
* Then, the attributes were evaluated in order to assess which ones have greater importance, and the ones with less importance were removed in an attempt to improve the evaluation.
* After these steps, it was concluded that the best decision tree was the one that used criterion="gini" after removing columns.
#### K-NN
* A for loop was used to test different numbers of neighbors (from 1 to 50).
* Then, the attributes were evaluated to assess which ones have greater importance, and the ones with less importance were removed in an attempt to improve the evaluation.
*  After these steps, it was concluded that KNN did not change (for a higher evaluation) with the removal of columns.
