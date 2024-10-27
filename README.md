# Health Insurance Cost Predictor

## Project Overview
This project aims to predict healthcare insurance costs using a dataset containing various attributes related to individuals, such as age, BMI, smoking status, and more. The focus is on using different regression-based machine learning algorithms to build an accurate predictive model.

## Dataset
The dataset contains the following features:
- **age:** Age of the individual
- **bmi:** Body Mass Index, which measures body fat based on height and weight
- **children:** Number of children/dependents covered by health insurance
- **smoker:** Smoking status of the individual (1 = Smoker, 0 = Non-smoker)
- **region:** Geographic region of the individual
- **charges:** Medical costs billed by health insurance, which serves as the target variable for prediction

## Project Structure
- `health_insurance_predictor.ipynb`: Jupyter Notebook containing the implementation of the project, data analysis, feature engineering, model training, and evaluation.
- `README.md`: Detailed documentation of the project.

## Methods Used

### Data Preprocessing
1. **Handling Missing Values:** 
   - Checked for missing values in the dataset and applied necessary preprocessing to handle them.
2. **Encoding Categorical Variables:**
   - Categorical variables such as `smoker` and `region` were encoded to make the data suitable for model training.
3. **Feature Scaling:** 
   - Applied standardization to scale numerical features and improve model performance.

### Models Applied
The following regression algorithms were used to build the predictive model:

1. **Linear Regression**
   - A basic linear model that assumes a linear relationship between the input features and the target variable.
2. **Decision Tree Regressor**
   - A tree-based model that splits the data into subsets based on feature values to minimize the prediction error.
3. **Random Forest Regressor**
   - An ensemble of decision trees that aggregates predictions from multiple trees to improve accuracy and reduce overfitting.
4. **Support Vector Regression (SVR)**
   - A kernel-based regression model that finds the best hyperplane to fit the data.

### Evaluation Metrics
- **R-squared:** Measures how well the model explains the variance in the target variable.
- **Mean Squared Error (MSE):** Measures the average squared difference between predicted and actual values.

## Observations

1. **Linear Regression:**
   - **R-squared:** 0.70
   - **Mean Squared Error:** 39,936,613
   - The model shows a decent fit but struggles to capture non-linear relationships.

2. **Decision Tree Regressor:**
   - **R-squared:** 0.68
   - **Mean Squared Error:** 42,841,260
   - Performs slightly worse than Linear Regression, indicating overfitting due to its complexity.

3. **Random Forest Regressor:**
   - **R-squared:** 0.82
   - **Mean Squared Error:** 23,884,680
   - The best-performing model, successfully capturing non-linear patterns with lower errors.

4. **Support Vector Regression (SVR):**
   - **R-squared:** -0.10
   - **Mean Squared Error:** 149,258,700
   - Poor performance, likely due to inadequate hyperparameter tuning or scaling issues.

### Key Insights
- **Random Forest Regressor** emerged as the most accurate model, demonstrating better generalization and lower errors compared to other models.
- **Support Vector Regression** requires further tuning to enhance its performance, as the results suggest underfitting.
- **Feature Scaling and Encoding** were crucial in improving the model's performance, highlighting the importance of preprocessing steps.

## Summary
The project successfully built a predictive model for estimating health insurance costs using multiple regression algorithms. The **Random Forest Regressor** delivered the best results, making it the recommended model for this task. Future improvements could include more sophisticated feature engineering, hyperparameter tuning, and the use of additional ensemble techniques to further enhance prediction accuracy.
