Titanic Survival Prediction

An end-to-end Machine Learning project based on the Titanic dataset. The project covers data exploration, preprocessing, feature preparation, model training, evaluation, comparison, and Kaggle submission.

Project Overview

The objective of this project is to predict whether a Titanic passenger survived based on information such as passenger class, sex, age, family relationships, fare, and port of embarkation.

The project was developed using Python and Scikit-learn, with multiple classification models tested and compared using a validation dataset.

Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Kaggle

Dataset

The project uses the Titanic dataset provided by the Kaggle Titanic competition.

The training dataset contains 891 passengers with known survival outcomes, while the test dataset contains 418 passengers for which survival outcomes are hidden.

Main Features

Pclass — Passenger class

Sex — Passenger gender

Age — Passenger age

SibSp — Number of siblings/spouses aboard

Parch — Number of parents/children aboard

Fare — Ticket fare

Embarked — Port of embarkation

Project Workflow
1. Data Exploration

The dataset was examined to understand:

Dataset structure

Feature types

Missing values

Survival distribution

Relationships between survival and passenger characteristics

2. Data Preprocessing

The following preprocessing steps were performed:

Missing Age values were filled using the median age from the training data.

Missing Embarked values were filled using the most common category.

Cabin was removed for the initial model because of the large number of missing values.

PassengerId, Name, and Ticket were removed from the initial feature set.

Categorical variables were converted into numerical representations.

3. Feature Selection

The initial model used seven features:

Pclass, Sex, Age, SibSp, Parch, Fare, and Embarked.

4. Model Training

The training data was divided into training and validation sets using an 80/20 split with stratification.

Three classification algorithms were evaluated:

Decision Tree

Random Forest

Logistic Regression

A simple baseline was also calculated for comparison.

Model Results
Model	Validation Accuracy
Decision Tree	85.47%
Random Forest	83.80%
Logistic Regression	81.01%
Baseline	61.45%

The Decision Tree achieved the highest validation accuracy among the models tested.

Final Model

The final model was a Decision Tree with:

max_depth = 5

random_state = 42

After model evaluation, the final Decision Tree was retrained using the complete training dataset of 891 passengers.

It was then used to generate predictions for the 418 passengers in the Kaggle test dataset.

Kaggle Result

Final Kaggle Score: 77.27%

The difference between the validation accuracy and Kaggle score demonstrates that performance on a single validation split does not necessarily represent performance on completely unseen data.

This was an important part of the project and highlighted the importance of model generalization and robust evaluation.

Key Learnings

Through this project, I practiced:

Exploratory Data Analysis

Data preprocessing

Missing-value handling

Categorical feature encoding

Feature selection

Train-validation splitting

Classification modeling

Model comparison

Confusion matrix and classification report analysis

Feature importance analysis

Kaggle submission workflow

Future Improvements

The project can be further improved through feature engineering and more robust model evaluation.

Planned improvements include:

Creating FamilySize

Creating IsAlone

Extracting passenger titles from Name

Improving age handling

Exploring Cabin information

Investigating Ticket features

Testing additional models

Using cross-validation for more reliable model evaluation

Project Structure
titanic-survival-prediction/
│
├── Titanic_Survival_Prediction.ipynb
├── README.md
└── submission.csv

Conclusion

This project provided a practical implementation of an end-to-end machine learning workflow, from raw data exploration and preprocessing to model comparison and Kaggle submission.

The initial model achieved a 77.27% Kaggle score, providing a baseline for future feature engineering and model improvements.
