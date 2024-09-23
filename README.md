# Income Prediction Using Random Forest

## Project Overview

This project is focused on building a machine learning model to predict whether a person's income exceeds $50K/year based on census data. The data is sourced from the UCI Machine Learning Repository, commonly known as the **Adult Income Dataset**. The main goal is to apply various preprocessing techniques and develop a classification model using Random Forest.

## Dataset

The dataset used for this project is the **Census Income Dataset (Adult)** from the UCI Machine Learning Repository. It contains demographic information such as age, education level, occupation, race, and sex, among other features. The target variable is a binary indicator showing whether an individual's income is greater than or less than $50K/year.

### Dataset Information:
- **Source:** [UCI Machine Learning Repository - Census Income Dataset](https://archive.ics.uci.edu/ml/datasets/adult)
- **Number of instances:** 48,842
- **Number of features:** 14 (Categorical and Numerical)
- **Target Variable:** Income (`<=50K` or `>50K`)

### Features:
- `age`: Continuous variable
- `workclass`: Categorical
- `fnlwgt`: Continuous
- `education`: Categorical
- `education-num`: Continuous
- `marital-status`: Categorical
- `occupation`: Categorical
- `relationship`: Categorical
- `race`: Categorical
- `sex`: Categorical
- `capital-gain`: Continuous
- `capital-loss`: Continuous
- `hours-per-week`: Continuous
- `native-country`: Categorical

### Target:
- `income`: Binary classification (`<=50K` or `>50K`)

## Project Workflow

### 1. Data Preprocessing:
   - **Handling Missing Values:** Imputed missing values where necessary.
   - **Encoding Categorical Features:** Used `OneHotEncoder` for categorical variables.
   - **Data Scaling:** Applied `StandardScaler` to normalize numerical features.
   
### 2. Model Development:
   - **Random Forest Classifier:** A random forest model was chosen for classification tasks due to its ability to handle both categorical and numerical data and its robustness to overfitting.
   
### 3. Model Tuning:
   - **Grid Search CV:** A grid search was conducted to find the optimal hyperparameters for the Random Forest model.
   - **Best Parameters:**
     - `n_estimators`: 200
     - `max_depth`: 10
     - `min_samples_split`: 5

### 4. Model Evaluation:
   - **Accuracy:** 86.17%
   - **Precision, Recall, F1-Score:** The final evaluation metrics of the model showed a balanced performance across the two classes (`<=50K` and `>50K`).

## Results

The Random Forest model achieved the following performance:

- **Accuracy:** 86.17%
- **Precision:**
  - Income `<=50K`: 89%
  - Income `>50K`: 75%
- **Recall:**
  - Income `<=50K`: 93%
  - Income `>50K`: 64%
- **F1-Score:**
  - Income `<=50K`: 91%
  - Income `>50K`: 69%

The model performed well in predicting whether an individual's income is greater than or less than $50K, with good overall accuracy and balanced precision/recall.

## Important Features for Prediction

The Random Forest model identified the following as important features for predicting income:
1. **Education Level**
2. **Age**
3. **Hours-per-week**
4. **Capital-gain**
5. **Marital Status**

