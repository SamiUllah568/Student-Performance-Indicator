# Student Performance Prediction

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Analysis](#analysis)
- [Model Training](#model-training)
- [Results](#results)
- [Conclusion](#conclusion)
- [Installation](#installation)
- [Usage](#usage)

## Project Overview
This project aims to predict student performance based on various features such as gender, race/ethnicity, parental education level, lunch type, and scores in reading and writing. The analysis and prediction model provide insights into factors affecting students' math scores.

## Dataset
The dataset contains the following columns:
- **gender**: Gender of the student
- **race/ethnicity**: Student's race/ethnicity
- **parental level of education**: Highest level of education attained by the parents
- **lunch**: Type of lunch (standard or free/reduced)
- **test preparation course**: Whether the student completed a test preparation course
- **reading score**: Score in reading
- **writing score**: Score in writing
- **math score**: Score in math (target variable)

The dataset consists of 1000 entries.

## Analysis
### Multivariate Analysis
Using Seaborn's `pairplot`, we analyzed the relationships between various features and the math score, with a focus on gender. The insights drawn from the pairplot indicate that:
- All scores (reading, writing, and math) show a linear increase with each other.
- Female students outperform male students in pass percentages and scores.
- Performance is influenced by lunch type and parental education level.
- Completing a test preparation course positively impacts performance.

### Visualization
```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.pairplot(data, hue='gender')
plt.show()

### Key Insights
Students' performance is influenced by lunch type, race/ethnicity, and parental education level.
Female students generally have a higher pass percentage and are top scorers.
Completion of the test preparation course is beneficial, although performance is not significantly affected by it.

### **Model Training**
The following steps were taken to prepare and train the models:

**Data Preparation**: Dropping unnecessary columns and setting the target variable.
**Encoding and Scaling**: Using OneHotEncoder for categorical variables and StandardScaler for numerical variables.
**Train-Test Split**: The dataset was split into training and testing sets.

### **Evaluation**
Various regression models were trained and evaluated. The evaluation metrics used include:

Mean Absolute Error (MAE)
Mean Squared Error (MSE)
Root Mean Squared Error (RMSE)
R² Score


 ### **Algorithm used**
* Linear Regression
* Lasso Regression
* Ridge Regression
* Decision Tree Regressor
* Random Forest Regressor
* Support Vector Regressor (SVR)
* XGBoost Regressor
* K-Neighbors Regressor
* AdaBoost Regressor
* CatBoost Regressor

Conclusion
The analysis and modeling indicate that various factors significantly influence students' performance.
The best model for predicting students' math scores is the CatBoost Regressor, which demonstrates high accuracy.
