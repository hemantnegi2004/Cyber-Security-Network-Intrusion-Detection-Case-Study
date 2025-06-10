# Cyber-Security-Network-Intrusion-Detection-Case-Study
Machine Learning using Python

## 📌 Project Overview / Summary
**Project Title**:
Cyber Security – Network Intrusion Detection Case Study

----------------
## Objective:
The goal of this project is to build a machine learning model to detect network intrusions and classify them as either:

**Binary classification**: Normal vs. Attack

**Multiclass classification**: Normal vs. various specific attacks (Back, BufferOverflow, FTPWrite, GuessPassword, Neptune, NMap, PortSweep, RootKit, Satan, Smurf).

---------------------
## Dataset Description:
The dataset includes network traffic data captured from multiple files, each representing different types of attacks.

Each record contains 41 features including:

Basic features (duration, protocol_type, service, flag, src_bytes, dst_bytes, etc.)

Content-based features (num_failed_logins, logged_in, etc.)

Traffic features (count, serror_rate, etc.)

A new column ‘attack’ was created to label the type of activity.

-------------------------
## Data Preparation:
✅ All CSV files were combined into a single dataset.
✅ The ‘attack’ column was used to define:

Binary classification target: 0 (Normal) vs. 1 (Attack)

Multiclass classification target: 0 (Normal) vs. specific attack classes.
✅ Categorical features (protocol_type, service, flag) were label encoded and stored in a mapping dictionary for interpretability.
✅ Numerical features were standardized using StandardScaler.
✅ Train-test split was performed using stratified sampling to ensure class balance.

----------------------
## Modeling Approach:
We explored and evaluated multiple machine learning models:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

Each model was trained and evaluated on both binary and multiclass classification tasks.

------------------------
## Key Findings:
✅ All models consistently achieved very high accuracy (~99.97% to 99.99%) on both training and testing sets.
✅ No significant overfitting observed (train and test scores were nearly identical).
✅ Feature importance plots confirmed that the dataset contains strong signals distinguishing between classes.

------------------------
## Conclusions:
The network traffic dataset is highly predictive of attacks, enabling effective detection.

Logistic Regression, Decision Tree, and Random Forest models all performed equally well, indicating model robustness.

Due to interpretability and simplicity, Logistic Regression can be considered as the preferred model, while Random Forest offers an additional perspective on feature importance.
