# Titanic Survival Prediction

## Overview
This project aims to predict the survival of passengers on the Titanic using machine learning algorithms. It utilizes feature engineering, data preprocessing, and multiple classification models to achieve optimal predictions.

## Dataset
The dataset used is the Titanic dataset, containing passenger details such as age, gender, class, fare, and more. The target variable is **Survived**, which indicates whether a passenger survived (1) or not (0).

## Features Used
The following features were selected for model training:
- **Sex** (Gender: Male/Female)
- **Pclass** (Passenger class: 1st, 2nd, 3rd)
- **Age** (Passenger age)
- **SibSp** (Number of siblings/spouses aboard)
- **Parch** (Number of parents/children aboard)
- **Fare** (Ticket fare price)
- **Embarked** (Port of embarkation: C, Q, S)
- **FamilySize** (Total family members on board)
- **isAlone** (Indicator if passenger was alone)
- **FarePerPerson** (Fare divided by family size)

## Project Workflow
### 1. Load Dataset
The dataset is loaded from a CSV file and basic statistics are displayed.

### 2. Data Preprocessing
- Missing values in **Embarked** are filled with the mode.
- Missing values in **Age** are filled with the mean.
- Irrelevant columns like **PassengerId**, **Name**, **Ticket**, and **Cabin** are dropped.
- Categorical features **Sex** and **Embarked** are encoded into numerical values.

### 3. Feature Engineering
- **FamilySize** is created by adding **SibSp** and **Parch**.
- **isAlone** is derived from **FamilySize** (1 if alone, 0 otherwise).
- **FarePerPerson** is computed as **Fare / FamilySize**.

### 4. Data Splitting
The dataset is split into training and testing sets (80% training, 20% testing).

### 5. Model Training
The following models were trained:
- **Logistic Regression**
- **K-Nearest Neighbors (KNN)**
- **Gradient Boosting Classifier**
- **Random Forest Classifier (with GridSearchCV for hyperparameter tuning)**

### 6. Model Evaluation
Each model is evaluated using:
- **Accuracy Score**
- **Classification Report** (Precision, Recall, F1-score)

## Results
The models achieved the following accuracies:
- **Gradient Boosting**: 82%
- **KNN**: 74%
- **Logistic Regression**: 79%
- **Random Forest**: 82%

## How to Run the Code
1. Clone the repository:
   ```sh
   git clone https://github.com/YOUR_USERNAME/titanic-survival-prediction.git
   ```
2. Navigate to the project folder:
   ```sh
   cd titanic-survival-prediction
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Run the script:
   ```sh
   python main.py
   ```

## Dependencies
- Python 3.x
- pandas
- matplotlib
- seaborn
- scikit-learn

## Author
Khushi Agrahari

