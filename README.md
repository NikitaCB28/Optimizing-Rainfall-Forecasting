# Optimizing-Rainfall-Forecasting
Rainfall-Prediction
Overview
This is a Flask web app which predicts whether it will rain tomorrow or not.

## Dataset:
https://www.kaggle.com/jsphyg/weather-dataset-rattle-package

## About the project:
Firstly, the dataset was bisected and numerical(continuous,discrete) and categorical features were identified. Missing Values were handled using Random Sample imputation to maintain the variance,Categorical Values like location, wind direction were handled by using Target guided encoding. Outliers were handled using IQR and boxplot. Feature scaling was also performed but it was not required. These are present in the ipynb file named "Data Preprocessing". Secondly, Feature Selection was done considering correlation heatmap and Extra Trees Classifier and plotting the feature importances but all the features were considered as it has only 25 features. This is present in the ipynb file named "Feature Selection". Finally, Imbalanced Dataset was handled using SMOTE. Model Creation was then performed. Different types of Machine Learning algorithms were tried like catboost, random forest, logistic regression, xgboost, support vector machines, knn, naive bayes and Decision tree. Out of these models the best classifier was selected. Catboost, random forest and Xgboost were the top 3. However, Xgboost out performed others slightly. So, the best classifier model was Xgboost. Hyperparameter Optimazation was also performedusing RandomizedSearchCV but due to system limitations a small sample out of the dataset was considered. The conclusion were made using classification metrics, roc curve and auc score.

### Installation
The Code is written in Python 3.7.3 If you don't have Python installed you can find it here. If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after cloning the repository:

1. First create a virtual environment by using this command:
conda create -n myenv python=3.7
2. Activate the environment using the below command:
conda activate myenv
3. Then install all the packages by using the following command
pip install -r requirements.txt
4. Then, in cmd or Anaconda prompt write the following code:
python app.py
