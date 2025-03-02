<h2>Comparing Classifiers</h2>

**Objective**<br>
The goal of this exercise is to create a classification model to predict the likelihood of a client subscribing to a term deposit in a marketing campaign. Various classifiers are compared for this exercise.

**Data Source**<br>
The dataset comes from the UCI Machine Learning repository link. The data is from a Portugese banking institution and is a collection of the results of multiple marketing campaigns. 

**Data Exploration**<br>
The dataset has 41188 rows and 21 columns. Data was clean adn no nulls in the columns.
The numerical columns have a normal distribution.

The features that have the higest percent of subscription are -
- students and retired in job category
- single in marital status category
- illiterate under education
- cellular phone previous contact
- in the months of March, December, Sept and Oct for previous call
- if the outcome of previous call was a success

**Modeling -**<br>
The categorical features were transformed using OneHotEncoding and the numerical columns were scaled to normalize the values.
A baseline accuracy is noted based on the frequency of highest occuring value, which is 89%
Logistic Regression, K-Nearest Neighbors (KNN), Decision Trees and Support Vector Machines (SVM) classifiers are compared.

Model comparison with default settings -
<img width="506" alt="Screenshot 2025-03-02 at 2 38 16 PM" src="https://github.com/user-attachments/assets/b685e493-50f5-42e9-b2d4-d1f5537cf317" />

- Decision Tree has a high accuracy on training set, but a large drop in accuracy for test set. This shows that the model may be overfitting
- KNN takes the least amount of time to compute and has second best accuracy
- Simple logistic regression gives the same accuracy as a computationally expensive SVM

Hyperparameter tuned model comparison -
<img width="732" alt="Screenshot 2025-03-02 at 2 39 32 PM" src="https://github.com/user-attachments/assets/b11a253b-a8bb-415d-bc23-aaa3d84c4689" />

- Decision Tree with tree depth of 5 and min_sample_split of 10 has the highest accuracy of 91%
- Logistic Regression is the most time efficient and is a close second at 90.8% accuracy

**Further Optimization--**
- Feature optimization can be done to exclude non-essential features and identify the most influential features
- Further tune hyper parameters. And include SVM model tuning.
