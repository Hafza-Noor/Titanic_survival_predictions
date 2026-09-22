# Titanic Survival Prediction

An end-to-end **Machine Learning project** based on the Titanic dataset. The project covers **data exploration, preprocessing, feature preparation, model training, evaluation, model comparison, and Kaggle submission**.

## Project Overview

The objective of this project is to predict whether a Titanic passenger survived based on information such as **passenger class, sex, age, family relationships, fare, and port of embarkation**.

The project was developed using **Python** and **Scikit-learn**, with multiple classification models tested and compared using a validation dataset.

## Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **Kaggle**

## Dataset

The project uses the **Titanic dataset** provided by the Kaggle Titanic competition.

- **Training dataset:** 891 passengers with known survival outcomes
- **Test dataset:** 418 passengers with hidden survival outcomes

## Main Features

| Feature | Description |
|---|---|
| **Pclass** | Passenger class |
| **Sex** | Passenger gender |
| **Age** | Passenger age |
| **SibSp** | Number of siblings/spouses aboard |
| **Parch** | Number of parents/children aboard |
| **Fare** | Ticket fare |
| **Embarked** | Port of embarkation |

## Project Workflow

### 1. Data Exploration

The dataset was examined to understand:

- Dataset structure
- Feature types
- Missing values
- Survival distribution
- Relationships between survival and passenger characteristics

### 2. Data Preprocessing

The following preprocessing steps were performed:

- Missing **Age** values were filled using the median age from the training data.
- Missing **Embarked** values were filled using the most common category.
- **Cabin** was removed for the initial model because of the large number of missing values.
- **PassengerId, Name, and Ticket** were removed from the initial feature set.
- Categorical variables were converted into numerical representations.

### 3. Feature Selection

The initial model used seven features:

**Pclass, Sex, Age, SibSp, Parch, Fare, and Embarked.**

### 4. Model Training

The training data was divided into **training and validation sets using an 80/20 split with stratification**.

Three classification algorithms were evaluated:

- **Decision Tree**
- **Random Forest**
- **Logistic Regression**

A simple **baseline** was also calculated for comparison.

## Model Results

| Model | Validation Accuracy |
|---|---:|
| **Decision Tree** | **85.47%** |
| Random Forest | 83.80% |
| Logistic Regression | 81.01% |
| Baseline | 61.45% |

The **Decision Tree achieved the highest validation accuracy among the models tested**.

## Final Model

The final model was a **Decision Tree** with the following parameters:

```python
max_depth = 5
random_state = 42
