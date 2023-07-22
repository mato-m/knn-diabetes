# K-nearest neigbors - Diabetes prediction

#### K-nearest neigbors (KNN)
Knn classifies data into the classes based on its distance from k number of its closest data points. Typically,
we use the Euclidean distance to determine which data point is the closest. It will classify the current data point
to the same class that most of the closest k data points belong to.

#### Dataset
The [dataset](https://www.kaggle.com/datasets/mathchi/diabetes-data-set) contains 768 rows and 9 columns that represents
various health parameters. The goal is to predict if user has Diabetes based on other health parameters.

All columns have numeric values and there are no missing values.

#### Model

Only the three columns that have the highest correlation with Outcome column are used: BMI, Glucose and Age.

Dataset is split into training, which is 80% of data, and test dataset (20% of data).

In order to determine the best number of neighbors we calculate the best achieved cross validation score
for each number of neighbors, ranging from 1 to 50.

#### Results

The model performed the best when it uses 18 neighbors, with accuracy score of 78% and recall of 56%.
The F1 score is equal to 64%.
