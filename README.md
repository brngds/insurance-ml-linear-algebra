# 🛡️ Insurance ML & Linear Algebra

Machine learning and linear algebra analysis for insurance applications, including customer similarity, classification, regression, and privacy-preserving data transformation.

## 📌 Context

The insurance company **Sure Tomorrow** wants to explore how machine learning can support different business and analytical challenges while maintaining the privacy of customer information.

The project combines machine learning techniques with linear algebra concepts to solve four distinct problems using customer demographic and insurance data.

## 🎯 Business Problems

The analysis addresses four main tasks:

1. **Customer Similarity**  
   Identify customers who are similar to a given customer to support marketing and customer relationship initiatives.

2. **Insurance Benefit Classification**  
   Predict whether a customer is likely to receive an insurance benefit and compare the predictive model with a dummy baseline.

3. **Insurance Benefit Regression**  
   Predict the number of insurance benefits a customer may receive using linear regression.

4. **Data Obfuscation**  
   Protect customers' personal information through a linear algebra-based data transformation while preserving the predictive quality of the regression model.

## 📊 Dataset

The analysis uses the `insurance_us.csv` dataset containing customer demographic information and historical insurance benefits.

### Features

- `gender` — customer gender
- `age` — customer age
- `income` — customer salary
- `family_members` — number of family members

### Target

- `insurance_benefits` — number of insurance benefits received during the previous five years

## 🔎 Analytical Approach

The project follows the workflow below:

1. Load and inspect the dataset
2. Validate data types, missing values, duplicates, and potential anomalies
3. Explore the distribution of customer characteristics
4. Standardize numerical features when required
5. Calculate customer similarity using distance metrics
6. Compare nearest-neighbor results before and after feature scaling
7. Build a classification model for insurance benefit eligibility
8. Compare model performance against a dummy baseline
9. Build a linear regression model to predict the number of benefits
10. Evaluate regression performance
11. Apply a matrix-based transformation to obfuscate customer features
12. Demonstrate mathematically why the transformation preserves linear regression predictions
13. Compare model performance before and after data obfuscation

## 🤖 Machine Learning Tasks

### Customer Similarity

A nearest-neighbor approach is used to identify customers with similar characteristics.

The analysis also investigates how feature scaling affects distance-based algorithms, since variables such as income can otherwise dominate the distance calculation.

### Classification

The insurance benefit count is transformed into a binary target indicating whether a customer received at least one insurance benefit.

A predictive model is evaluated against a dummy baseline to determine whether machine learning provides useful predictive information.

### Linear Regression

A linear regression model is implemented to predict the number of insurance benefits received by customers.

Model performance is evaluated using appropriate regression metrics.

### Data Obfuscation

Customer features are transformed using multiplication by an invertible random matrix.

The project demonstrates how this transformation makes the original customer information more difficult to recover while preserving the predictive properties of linear regression.

## 💡 Business Applications

The techniques explored in this project can support:

- Customer segmentation and similarity-based marketing
- Identification of customers with higher probability of insurance claims
- Estimation of insurance benefit frequency
- Privacy-preserving analytical workflows
- Secure use of sensitive customer information in machine learning applications

## ⚠️ Limitations

The dataset contains a limited set of demographic variables and historical insurance benefit information.

The models developed in this project are intended to demonstrate machine learning and linear algebra concepts rather than serve as production insurance risk models.

Additional behavioral, financial, policy, and historical claim information would be necessary for a more comprehensive production solution.

## 🛠️ Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Linear Algebra
- Jupyter Notebook

## 📁 Repository Structure

```text
insurance-ml-linear-algebra/
│
├── README.md
│
├── data/
│   └── insurance_us.csv
│
└── notebook/
    └── insurance_ml_linear_algebra.ipynb
