
# Titanic Dataset: Exploratory Data Analysis (EDA) and Data Cleaning

## Introduction

This project involves performing exploratory data analysis (EDA) and data cleaning on the Titanic dataset. The goal is to understand the structure of the data, identify patterns, and clean the data for further analysis or model building.

## Dataset

The Titanic dataset contains information about the passengers aboard the Titanic, including whether they survived or not. The dataset includes the following features:

- **PassengerId**: Unique ID for each passenger.
- **Survived**: Survival (0 = No, 1 = Yes).
- **Pclass**: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd).
- **Name**: Name of the passenger.
- **Sex**: Gender of the passenger.
- **Age**: Age of the passenger.
- **SibSp**: Number of siblings or spouses aboard the Titanic.
- **Parch**: Number of parents or children aboard the Titanic.
- **Ticket**: Ticket number.
- **Fare**: Passenger fare.
- **Cabin**: Cabin number.
- **Embarked**: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

## Data Cleaning

The following data cleaning steps were performed:

1. **Handling Missing Values**: 
    - The `Age`, `Cabin`, and `Embarked` columns had missing values.
    - `Age` was imputed using the median of each class.
    - The `Embarked` column was filled with the most common embarkation port.
    - The `Cabin` column was dropped due to a large number of missing values.

2. **Feature Engineering**:
    - Created new features like `FamilySize` (SibSp + Parch) and `IsAlone` (whether a passenger was alone).

3. **Encoding Categorical Variables**:
    - The `Sex` and `Embarked` columns were converted into numerical values for analysis.

## Exploratory Data Analysis (EDA)

Several analyses and visualizations were performed to gain insights into the data:


1. **Survival Rates by Passenger Class**:
    ![Survival by Class](<Graph/Survival by  Class.png>)
    - **Inference**: The survival rate was significantly higher for passengers in the 1st class compared to those in the 2nd and 3rd classes. This suggests that wealthier passengers had a better chance of survival, possibly due to better access to lifeboats.

2. **Survival Rates by Gender**:
    ![Survival by Gender](<Graph/Survival by Gender.png>)
    - **Inference**: Female passengers had a much higher survival rate than male passengers. This aligns with the historical account of the "women and children first" protocol followed during the evacuation.

3. **Age Distribution by Survival Status**:
    ![Age Distribution by Survival](<Graph/Age Distribuition by Survival Status.png>)
    - **Inference**: Younger passengers, particularly children, had higher survival rates. The age distribution shows that many of the younger passengers survived, while a larger proportion of middle-aged passengers did not.

4. **Fare Distribution by Survival Status**:
    ![Fare Distribution by Survival](<Graph/Fare Distribuition by Survival.png>)png)
    - **Inference**: Passengers who paid higher fares generally had a better chance of survival. This correlates with the higher survival rates observed among 1st class passengers, who would have paid more for their tickets.

## Conclusion

The EDA revealed several key factors that influenced survival on the Titanic. Women and children had higher survival rates, especially those in higher classes. The port of embarkation also played a role, with passengers from certain ports having better survival odds.

This analysis provided a solid foundation for building predictive models, where the cleaned data and insights from the EDA can be utilized.
