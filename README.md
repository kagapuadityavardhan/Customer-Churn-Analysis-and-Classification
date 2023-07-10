# Customer Churn Prediction #
Customer Churn Prediction is a machine learning project that aims to predict customer churn (i.e., customer attrition) in a telecommunications company. By analyzing customer data and building a predictive model, the project helps identify customers who are likely to churn, allowing the company to take proactive measures to retain them.
# Introduction
Customer churn is a critical issue for businesses, as losing customers can have a significant impact on revenue and profitability. This project utilizes machine learning techniques to predict customer churn, enabling businesses to focus on retaining high-risk customers and reducing customer attrition.

# Data
The project utilizes the "Customer-Churn-Records.csv" dataset, which contains customer information such as demographics, services subscribed, satisfaction scores, and churn status. The dataset is preprocessed and split into training and testing sets for model development and evaluation.

# Project Workflow
Data Preprocessing: The dataset is cleaned by removing unnecessary columns and handling missing values. Categorical variables are one-hot encoded or ordinal encoded as appropriate.
Exploratory Data Analysis (EDA): EDA is performed to understand the distribution and relationships between variables. Visualizations are created to explore categorical distributions, numerical distributions, and correlations.
Model Development: A Random Forest Classifier is trained on the preprocessed data to predict customer churn. The training set is oversampled using SMOTE to address class imbalance.
Model Evaluation: The trained model is evaluated on the testing set using various metrics such as F-measure, Recall, Precision, and classification report.
Discrimination Threshold Analysis: The DiscriminationThreshold visualizer is utilized to explore the impact of different probability thresholds on precision and recall, helping to determine an optimal threshold for making predictions.
Results: The results of the model evaluation and discrimination threshold analysis are reported, providing insights into the model's performance and its potential application in real-world scenarios.
# Handling imbalanced case
the code provided addresses the issue of class imbalance in the dataset. The imbalanced case refers to situations where the distribution of classes in the target variable is highly skewed, with one class being significantly more prevalent than the other. In this case, the target variable is 'Exited,' which indicates whether a customer has churned or not.

To handle the class imbalance, the code incorporates the Synthetic Minority Over-sampling Technique (SMOTE). SMOTE is used to generate synthetic samples of the minority class (in this case, the 'Exited' class) to balance the class distribution. This is achieved by creating synthetic samples that interpolate between existing minority class instances. The SMOTE technique is applied to the training data using the SMOTE class from the imblearn library.

After applying SMOTE, the code proceeds with training a Random Forest classifier on the balanced training data (X_res and y_res). The classifier is then used to make predictions on the test data (X_test_sc). Finally, the code evaluates the performance of the classifier using various metrics, including F-measure, recall, precision, and classification report.
# Results
The project provides insights into the factors influencing customer churn and a predictive model to identify high-risk customers. The evaluation metrics and visualizations help understand the model's performance and guide decision-making in customer retention strategies.

By addressing the issue of class imbalance through SMOTE and evaluating the model's performance, the code ensures that the imbalanced nature of the dataset is properly handled and the classification results are reliable.
