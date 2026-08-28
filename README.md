# 💳 Credit Card Default Prediction with Support Vector Machines

Machine learning analysis of credit card default risk using **Support Vector Machines (SVM)** on the UCI Credit Card Default dataset.

The project explores customer financial and demographic information, performs preprocessing and class balancing, and compares **Linear SVM** and **RBF-kernel SVM** models using cross-validation and hyperparameter optimization.

## 🎯 Project Objective

The goal of the project is to build a binary classification model capable of predicting whether a credit card customer will default on their next payment.

The target variable contains two classes:

* **Did not default**
* **Defaulted**

The project also explores how model validation and hyperparameter tuning influence classification performance.

## 📊 Dataset

The dataset comes from the **UCI Machine Learning Repository** and contains information about credit card customers in Taiwan.

It contains approximately:

* **30,000 observations**
* **24 variables**

The available features include:

### Customer Information

* Credit limit
* Gender
* Education
* Marital status
* Age

### Payment History

Historical repayment status for previous months.

### Billing Information

Monthly credit card bill amounts.

### Previous Payments

Amounts paid by the customer during previous months.

### Target Variable

Whether the customer defaulted on the following month's payment.

## 🔎 Machine Learning Workflow

The project follows a complete supervised learning workflow.

### 1. Data Loading and Cleaning

The dataset is loaded using Pandas and prepared for analysis by:

* removing unnecessary identifiers
* converting variables to numerical format
* inspecting categorical variables
* checking the data for inconsistencies

### 2. Class Balancing

Because credit default datasets can present class imbalance, resampling techniques are applied to obtain a more balanced dataset before model training.

### 3. Feature Scaling

The input variables are normalized before fitting the Support Vector Machine models.

Feature scaling is especially important for SVM algorithms because the models are sensitive to differences in feature magnitude.

### 4. Train/Test Split

The processed dataset is divided into training and testing sets to evaluate model performance on unseen observations.

### 5. Hyperparameter Optimization

`GridSearchCV` is used to search for optimal SVM hyperparameters.

For the linear model, the regularization parameter **C** is optimized.

For the RBF model, both:

* **C**
* **gamma**

are optimized.

### 6. Nested Cross-Validation

Nested cross-validation is implemented to simultaneously perform:

* hyperparameter selection
* generalization performance estimation

This provides a more reliable estimate of model performance than evaluating a single tuned model on the same validation procedure.

## 🤖 Models

### Linear Support Vector Machine

A `LinearSVC` model is trained and optimized using cross-validation.

Nested cross-validation produced an average accuracy of approximately:

**69.3%**

### RBF Support Vector Machine

A nonlinear Support Vector Machine using the **Radial Basis Function (RBF)** kernel is also evaluated.

Nested cross-validation produced an average accuracy of approximately:

**70.0%**

This suggests a small improvement from modelling nonlinear decision boundaries.

## 📈 Model Evaluation

Model performance is evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* Cross-validation scores

The notebook compares both linear and nonlinear SVM approaches and investigates how different hyperparameter configurations affect model performance.

## 🛠️ Technologies

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**
* **Jupyter Notebook**

Machine learning techniques used include:

* Support Vector Machines
* Linear SVM
* RBF Kernel SVM
* Grid Search
* Nested Cross-Validation
* Feature Scaling
* Resampling
* Classification Metrics

## 📁 Repository Structure

```text
Customers-default-payments/
│
├── charts/
│   └── visualizations generated during the analysis
│
├── data/
│   └── dataset used in the project
│
├── RizzitelloSVM.ipynb
│   └── data preparation, model training and evaluation
│
└── README.md
```

## 💡 Skills Demonstrated

This project demonstrates practical experience with:

* supervised machine learning
* classification problems
* preprocessing pipelines
* imbalanced datasets
* Support Vector Machines
* hyperparameter tuning
* nested cross-validation
* model evaluation
* Python data analysis

## 📚 Data Source

The original dataset is available from the **UCI Machine Learning Repository**:

*Default of Credit Card Clients Dataset — Taiwan.*

## 👤 Author

**Nicola Rizzitello**

Machine Learning / Data Science project.
