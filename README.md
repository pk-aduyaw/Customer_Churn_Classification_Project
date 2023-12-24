<img src='https://github.com/pk-aduyaw/Customer_Churn_Classification_Project/assets/148882212/08fdd7b4-d0cd-44f2-8354-f7483c806e8c' alt='my banner' style="width:1500px;height:300px;">
<h1 align='center'>Reducing Customer Churn Through Machine Learning: A Case Study on Vodafone</h1>

## Table of Content
[Project Description](#project-description)

[Installation](#installation)

[Data Source & Preprocessing](#data-source--preprocessing)
* [Data Source & Understanding](#data-source--understanding)
* [Data Preprocessing](#data-preprocessing) 

[Model Building & Evaluation](#model-building--evaluation)

[Results & Insights](#results--insights)

[Reference](#reference)

[Contributions](#contributions)

[Author](#author)


<h2>Project Description</h2>

<p>Customer churn as defined by <a href='https://www.paddle.com/resources/customer-churn' to='_blank'>Paddle</a> is the loss of subscribers or customers, which can have a huge impact on any company's revenue stream. While several revenue models exist, being able to retain customers remains crucial for maximizing profits. This project focuses on tackling this challenge by building a robust machine-learning model to predict customer churn.</p>

<p>By proactively identifying customers at risk of leaving, companies can implement targeted interventions like incentives, personalized offers, or improved customer service to encourage them to stay. This predictive approach enables businesses to:</p>

* Reduce customer churn rate and increase customer lifetime value.
* Optimize resource allocation by focusing retention efforts on at-risk customers.
* Gain valuable insights into customer behavior and preferences.

<p>The success of this project lies in building a highly accurate and interpretable machine learning model. This will require carefully chosen data features, effective model selection, and rigorous evaluation techniques. Ultimately, this project aims to equip companies with a powerful tool to combat customer churn and achieve sustainable growth.</p>

<h2>Installation</h2>

This project requires that you have a `Python 3.9 or later version` installed on your local machine. The modules and packages needed to complete this project are all contained in the `requirements.txt` file. Run this command in your terminal to get started on the project:

```bash
pip install -r requirements.txt
```

<h2>Data Source & Preprocessing</h2>

This section emphasizes sources of data, provides details on the dataset for better understanding, and lists the processes undertaken to preprocess the dataset for machine learning.

<h3>Data Source & Understanding</h3>

The datasets for this project were sourced from GitHub, Microsoft SQL Server, and a CSV file from Onedrive. The columns in the dataset and the values contained in them are provided below for data understanding.

- Gender -- Whether the customer is a male or a female

- SeniorCitizen -- Whether a customer is a senior citizen or not

- Partner -- Whether the customer has a partner or not (Yes, No)

- Dependents -- Whether the customer has dependents or not (Yes, No)

- Tenure -- Number of months the customer has stayed with the company

- Phone Service -- Whether the customer has a phone service or not (Yes, No)

- MultipleLines -- Whether the customer has multiple lines or not

- InternetService -- Customer's internet service provider (DSL, Fiber Optic, No)

- OnlineSecurity -- Whether the customer has online security or not (Yes, No, No Internet)

- OnlineBackup -- Whether the customer has online backup or not (Yes, No, No Internet)

- DeviceProtection -- Whether the customer has device protection or not (Yes, No, No internet service)

- TechSupport -- Whether the customer has tech support or not (Yes, No, No internet)

- StreamingTV -- Whether the customer has streaming TV or not (Yes, No, No internet service)

- StreamingMovies -- Whether the customer has streaming movies or not (Yes, No, No Internet service)

- Contract -- The contract term of the customer (Month-to-Month, One year, Two year)

- PaperlessBilling -- Whether the customer has paperless billing or not (Yes, No)

- Payment Method -- The customer's payment method (Electronic check, mailed check, Bank transfer(automatic), Credit card(automatic))

- MonthlyCharges -- The amount charged to the customer monthly

- TotalCharges -- The total amount charged to the customer

- Churn -- Whether the customer churned or not (Yes or No)

<h3>Data Preprocessing</h3>

The dataset that was gathered had inconsistencies like null values, and wrong data types in certain columns, which had to be corrected. The null values were imputed using `Simple Imputer` and the data types for columns with wrong data types were corrected.

The necessary corrections that were to be made were put into a pipeline to ensure that these same processes were used when new datasets were provided. The categorical columns in the dataset were all changed to numerical values for the machine-learning model to learn efficiently using `OneHot Encoder` and `Label Encoder`.

<h2>Model Building & Evaluation</h2>

Two datasets out of the three that were sourced from multiple places were concatenated and divided into features and target variables, after which it was split into train and evaluation sets with a percentage of 80% for training and evaluation for the remaining. The goal of this project is to build a robust machine-learning model hence, five models namely, `RandomForest`, `DecisionTree`, `GradientBoosting`, `KNN`, and `SupportVector` classifiers were trained.

The imbalanced nature of our target column called for a balancing of the dataset and this was done using both `RandomSampler` and `SMOTE` and it was seen that the latter performed better. Feature selection was implemented to improve the performance of the model, and also some hyperparameter tuning processes using `RandomizedSearchCV`.

The model's performance was assessed using the `f1-score` metric and the `AUC-ROC curve`. The `f1-score` according to [Serokell](https://serokell.io/blog/a-guide-to-f1-score) blends precision and recall using their harmonic mean which means maximizing for the `f1-score` implies simultaneously maximizing for both `precision` and `recall`.

[Towards Data Science](https://towardsdatascience.com/tagged/auc-roc-curve) states that the AUC-ROC curve visually summarizes a classifier's ability to distinguish between classes across all thresholds, with a higher AUC indicating better separation (AUC = Area Under the ROC Curve). A graph for the ROC curve for all the models was plotted with their respective auc-score to help assess how the model is performing.

<h2>Results & Insights</h2>

The GradientBoosting classifier was the best-performing model after the modeling and hyperparameter processes and was used to predict the outcome for the test data. The number of churned customers predicted by our model was 591 while no-churn customers were 1409. The company must reach out to the 591 customers predicted by the model and put measures in place to prevent them from churning. This is very important since it will help maximize revenue for the subsequent financial year.

<h2>Reference</h2>

[Paddle](https://www.paddle.com/resources/customer-churn)

[Serokell](https://serokell.io/blog/a-guide-to-f1-score)

[Towards Data Science](https://towardsdatascience.com/tagged/auc-roc-curve)

<h2>Contributions</h2>
Contributing to this project will help to improve a lot of things. Don't hesitate to fork the Repo and send in your pull requests for enhancement of the project.

<h2>Author</h2>
Prince K. A. Aduyaw
