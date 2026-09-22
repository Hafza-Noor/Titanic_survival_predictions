Titanic Survival Prediction

A machine learning project using the famous Titanic dataset from Kaggle. The goal of the project is to predict whether a passenger survived based on different passenger and ticket-related features.

I worked through the full machine learning process, starting with exploring the data and handling missing values, then training and comparing different classification models before creating a final Kaggle submission.

Project Overview

The model uses information such as:

Passenger class

Sex

Age

Number of siblings/spouses aboard

Number of parents/children aboard

Fare

Port of embarkation

The project was built using Python and Scikit-learn, with a few different classification algorithms tested on a validation set.

Tools & Libraries

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Kaggle

Dataset

The dataset comes from the Kaggle Titanic competition
.

There are 891 passengers in the training dataset, where the survival outcome is known, and 418 passengers in the test dataset, where the survival outcome is hidden.

Features Used
Feature	Description
Pclass	Passenger class
Sex	Passenger sex
Age	Passenger age
SibSp	Number of siblings/spouses aboard
Parch	Number of parents/children aboard
Fare	Ticket fare
Embarked	Port where the passenger boarded
Project Workflow
1. Data Exploration

I first explored the dataset to get an idea of its structure and identify things that needed to be handled before training the models.

This included looking at:

Data types and dataset structure

Missing values

Survival distribution

Relationships between features and survival

2. Data Preprocessing

A few preprocessing steps were applied before training the models:

Missing Age values were replaced with the median age from the training data.

Missing Embarked values were replaced with the most common value.

Cabin was removed because a large portion of the values were missing.

PassengerId, Name, and Ticket were not used in the initial model.

Categorical features were converted into numerical values.

3. Feature Selection

The initial model used these seven features:

Pclass, Sex, Age, SibSp, Parch, Fare, and Embarked.

4. Model Training

The training data was split into training and validation sets using an 80/20 split with stratification.

I tested three classification models:

Decision Tree

Random Forest

Logistic Regression

I also calculated a simple baseline accuracy to have something to compare the models against.

Model Results
Model	Validation Accuracy
Decision Tree	85.47%
Random Forest	83.80%
Logistic Regression	81.01%
Baseline	61.45%

Based on this validation split, the Decision Tree performed best among the models tested.

Final Model

The final model was a Decision Tree using:

max_depth = 5
random_state = 42


After evaluating the models, I retrained the Decision Tree using the complete training dataset of 891 passengers.

The trained model was then used to predict the survival outcomes for the 418 passengers in the Kaggle test dataset.

Kaggle Result

Kaggle Score: 77.27%

The Kaggle score was lower than the validation accuracy. This was a useful reminder that performance on one validation split does not always translate directly to completely unseen data.

It also showed why model evaluation and generalization are important when working with machine learning models.

What I Learned

This project gave me hands-on practice with:

Exploratory Data Analysis

Data preprocessing

Handling missing values

Encoding categorical variables

Feature selection

Train/validation splitting

Classification models

Comparing different models

Confusion matrices and classification reports

Feature importance

Creating Kaggle submissions

Future Improvements

There are several things I would like to try to improve the model:

Create a FamilySize feature

Create an IsAlone feature

Extract passenger titles from Name

Improve the way missing ages are handled

Explore the Cabin feature instead of removing it

Look for useful information in Ticket

Try additional machine learning models

Use cross-validation instead of relying on a single validation split

Experiment with feature engineering and hyperparameter tuning

Project Structure
titanic-survival-prediction/
│
├── Titanic_Survival_Prediction.ipynb
├── README.md
└── submission.csv

Conclusion

This project was a good introduction to building a complete machine learning workflow using a real dataset.

I started with basic data exploration and preprocessing, tested several classification models, compared their results, and finally created a submission for the Kaggle Titanic competition.

The final Kaggle score was 77.27%, and there is still plenty of room to improve the model through better feature engineering and evaluation.
