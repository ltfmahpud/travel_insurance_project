# Predicting Travel Insurance Claims with Classification Models  

## Context  
When someone plans a trip, especially abroad, they will face various risks that could occur. These risks include illness during the trip, ticket cancellations, or even a broken rental car. To protect themselves from these risks, many travelers choose to buy travel insurance. The insurance provides various types of coverage depending on their needs.

However, out of the many insurance policies sold, only a small number are claimed by the insured. When a claim is made, the insurance company needs to ensure that there is enough liquidity available to fulfill its obligations. However, if the liquidity set aside for claims is too large and unused, the insurance company will face a problem, as the liquidity remains idle and does not generate maximum profit.

To address this issue, the insurance company must predict the claims that are likely to occur. With accurate predictions, **the company can allocate enough liquidity for the expected claims, while the remaining liquidity can be invested in other products**. This way, the company not only fulfills its obligations to the claims but also maximizes profit through more efficient liquidity allocation. 

---

## Data Source and Dataset Info  
The dataset was taken from Kaggle* and it belongs to a travel insurance company. The dataset consist of 11 columns and 44327 rows. The rows indicates the number of insured and the columns are as follows:  
- **Agency**: Agency tenure with the company (number of years or months).
- **Agency Type**: Type of travel insurance agency (e.g., Online, Broker, Direct).
- **Distribution Channel**: Channel through which the insurance was sold (e.g., Online, In-person, Phone).
- **Product Name**: Type of travel insurance product (e.g., Comprehensive, Medical, Trip Cancellation).
- **Gender**: Gender of the insured (Male, Female).
- **Duration**: Duration of the travel (in days or months).
- **Destination**: Travel destination (e.g., Europe, USA, Asia).
- **Net Sales**: Sales amount from the insurance policy (e.g., in USD or EUR).
- **Commission (in value)**: Commission earned from the sale of the insurance policy (e.g., in USD or EUR).
- **Age**: Age of the insured (numeric value).
- **Claim**: Whether a claim was made (1: Yes, 0: No).

---

## Project Goal  
The purpose is to create machine learning model which can predict insured who are likely to claim.  

---

## Analytic Approach  

### Exploratory Data Analysis (EDA)  

### Data Cleaning and Modifying  
- Remove unused features
- Duplicate
- Handling missing value
- Remove Outlier
- Feature Modifying

### Modelling Process and Optimalization  
    - Encoding and Scaling
    - Handling Imbalance Classification   
    - Data Splitting
    - Compare performance from some candidate algorithms
    - Hyperparameter Tuning  

### Explain AI
    - Confusion Matrix
    - Feature Coefficient 

---

## Metrics for Evaluation  
- **Primary Metric:** Recall.
Our goal is to calculate the number of predictions that make a claim, whether or not the claim is valid. This aims to avoid situations where we predict no claim, but in reality, there is a claim. If liquidity cannot cover the claim submission, the company's reputation in the eyes of customers will be severely damaged.
- **Second-hand Metric:** Accuracy and ROC-AUC.
Other metric will be used for us to understand more about the model.  

---

## Tools and Technologies Used  

### Programming Language  
- Python  

### Standard Libraries  
- `numpy`, `pandas`: For data manipulation and analysis.  
- `matplotlib`, `seaborn`: For data visualization.  

### Machine Learning and Preprocessing  
- `scikit-learn`:  
  - `train_test_split`, `StratifiedKFold`, `GridSearchCV`, `RandomizedSearchCV`, `cross_val_score`: Model training and validation.  
  - `ColumnTransformer`, `Pipeline`: Data preprocessing.  
  - `OneHotEncoder`, `StandardScaler`: Encoding and scaling.  
  - Evaluation metrics: `accuracy_score`, `recall_score`, `roc_auc_score`.  
- `imbalanced-learn`: Handling imbalanced data using `SMOTE` and other techniques.    

### Classifiers Used  
- `LogisticRegression`  
- `KNeighborsClassifier`  
- `DecisionTreeClassifier`  
- `RandomForestClassifier`     
- `XGBClassifier`  

### Utilities  
- `pickle`: Saving and loading the trained model.  
- `os`: System-level file handling.  
- `warnings`: For managing warning messages.  

---
