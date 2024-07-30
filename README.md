# LAPTOP PRICE PREDICTION USING ML

In this project, we delve into understanding how various laptop specifications directly impact their prices. Through thorough analysis of components such as processors, memory, storage, and graphics cards, our focus is on accurately predicting the price of each laptop model. 

By leveraging this predictive approach, we aim to provide users with valuable insights into the expected cost of a laptop based solely on its specifications. 

This predictive model serves as a useful tool for both consumers and industry professionals, aiding in informed decision-making processes and market analysis.

# So Why ML?

**Complex Patterns**: ML algorithms can identify intricate patterns within large datasets that might not be apparent through traditional analysis. This allows for a more comprehensive understanding of how different laptop specifications correlate with prices.

**Prediction Accuracy**: ML models can make accurate predictions based on historical data. By training the model on a dataset containing information about various laptop specifications and their corresponding prices, we can develop a predictive model that estimates the price of a laptop based on its features.

**Scalability**: ML models are scalable, meaning they can handle large volumes of data efficiently. As the dataset grows or as more features are considered, ML algorithms can adapt and continue to provide accurate predictions.

**Automation**: Once the ML model is trained, it can automate the process of predicting laptop prices based on specifications. This saves time and effort compared to manual analysis and prediction methods.

**Continuous Improvement**: ML models can be continuously improved by refining algorithms, updating datasets, and incorporating new features. This ensures that the predictive model remains accurate and relevant over time.

# About Data
This dataset includes details about several laptops, such as features and costs, that have been carefully chosen in order to anticipate sales prices. This dataset is a useful tool for trend analysis and laptop price prediction because it includes features such as CPU and display specifications.

<img width="317" alt="image" src="https://github.com/user-attachments/assets/085cb859-c939-4082-8be6-50005c7ef268">

# Libraries used
## Data Manipulation And Analysis

**Pandas**: Pandas provides powerful data structures like DataFrames, which are essential for organizing and manipulating tabular data efficiently. It allows for tasks such as data cleaning, filtering, and transformation.
**NumPy**: NumPy offers support for numerical operations and arrays, enabling efficient computation of mathematical operations on large datasets. It provides essential functionalities for handling numerical data effectively.

## Machine Learning Modeling 

**scikit-learn**: This library offers a wide range of machine learning algorithms and tools for data preprocessing, model training, evaluation, and deployment. It provides implementations of regression algorithms suitable for predicting laptop prices based on specifications.

## Data Visualization 

**Matplotlib**: Visualization is crucial for gaining insights from data and communicating findings effectively. Matplotlib offers a wide variety of plotting functions and customization options, allowing for the creation of informative charts, graphs, and plots to visualize the relationships between laptop specifications and prices.

# Understanding Data

<img width="362" alt="image" src="https://github.com/user-attachments/assets/c4f993bb-35d0-46c1-ae5d-6c6098a67e9a">

Data Types
* int64: 7 columns
* float64: 10 columns
* object: 11 columns
* bool: 1 column

For this dataset we can see that we have null values/NaN values which we will se further on.

<img width="478" alt="image" src="https://github.com/user-attachments/assets/a056927e-616d-49e1-ad5f-716b6de457eb">

* This shows that we have unique laptop models from each brand and no duplicates in our dataset

## Why Understanding about the data is important because 

<img width="522" alt="image" src="https://github.com/user-attachments/assets/b63ac6ab-cbda-4db8-8d2a-9235895217e0">

* **Data Analysis Strategy**: Knowing that the dataset contains both categorical and continuous data allows us to plan our data analysis strategy accordingly. 
* **Feature Engineering**: Understanding the types of data present in the dataset is crucial for feature engineering.
* **Model Selection**: The presence of both categorical and continuous data influences the choice of machine learning algorithms and models. Some algorithms, like decision trees or random forests, naturally handle categorical data, while others may require preprocessing steps. Being aware of the data types helps us select the most appropriate models for our analysis.

To prepare our data for modeling, we've selected 19 columns out of the 28.

<img width="320" alt="image" src="https://github.com/user-attachments/assets/2484c673-d3a6-4844-8a73-e3f76502103f">

The columns which we have ruled out do not provide any significant importance to machine learning model.

Handling null values is a critical step in data preprocessing to ensure the quality and integrity of the dataset. In this case, 22 rows were removed due to the small number of null values, which were deemed insignificant for the prediction task. Here's a more detailed description of this process:

# Feature Engineering

<img width="532" alt="image" src="https://github.com/user-attachments/assets/be147121-2f16-476c-8565-dc139b5aaa56">

**Label encoding** was employed to convert categorical variables Storage_type, and Operating_system, into numerical representations. 
This conversion ensures that these categorical features can be utilized effectively by machine learning algorithms in our predictive model.

# Scaling the data

<img width="592" alt="image" src="https://github.com/user-attachments/assets/2c21872e-c4dd-4753-8c60-05c12fa0db32">

## But why?

* Ensures uniformity of features.
* Improves model performance.
* Normalizes data distribution.
* Reduces sensitivity to outliers.
* Facilitates interpretability of model coefficients.
* Prevents numerical instabilities.

# The Models We Selected
**Linear Regression**:
* Simple and interpretable.
* Assumes linear relationships between features and target.

**Random Forest Regressor**:
* Handles non-linear relationships well.
* Robust to outliers and noisy data.

**MLP Regressor (Multi-layer Perceptron)**:
* Can capture complex patterns in data.
* Allows for flexibility in network architecture and feature learning.

# Evaluating Models

## Linear Regression
<img width="376" alt="image" src="https://github.com/user-attachments/assets/916542b6-9882-4383-b17c-277874b72db1">

## Random Forest
<img width="374" alt="image" src="https://github.com/user-attachments/assets/9b31ef94-5b17-41bc-ad96-de877a61114f">


## MLP regressor 
<img width="377" alt="image" src="https://github.com/user-attachments/assets/511fa747-51e7-44eb-92e3-e856599dc59b">

### The Evaluating Metrices

* Accuracy as a single evaluating method is not good as it is sensitivity to prediction errors and has metric incompatibility with regression tasks.
* Using RMSE and R2 score together provides a comprehensive evaluation of the regressor models by assessing both the accuracy and goodness of fit.
* While RMSE quantifies the magnitude of errors in predictions,    R2 score evaluates how well the model captures the variance in the target variable. 

# Comparing Actual and Predicted Values:
## Random forest Regressor 
<img width="210" alt="image" src="https://github.com/user-attachments/assets/b2d9cf1b-d7b4-451c-bd6a-81f7bd864421">

## Linear Regressor
<img width="215" alt="image" src="https://github.com/user-attachments/assets/837f0c87-fb16-4fe0-bbea-908df93c3f77">


## MLP Regressor
<img width="219" alt="image" src="https://github.com/user-attachments/assets/e0f0ab19-77ab-4144-a286-1d4fd905f2bc">

# Conclusion
* In conclusion, while our laptop price prediction project achieved a modest accuracy of around 75%, there remains significant room for improvement. Despite this, our models have demonstrated the capability to learn meaningful patterns from the data. 

* Moving forward, targeted efforts to refine feature engineering, explore advanced algorithms, and incorporate feedback will be crucial in enhancing the accuracy and effectiveness of our predictive models.









