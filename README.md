# 📩 Message Intelligence System
### AI-Powered Spam Message Detection using Machine Learning

> Detecting spam messages with **K-Nearest Neighbors (KNN)**, **Support Vector Machine (SVM)**, and **Naive Bayes** while demonstrating the probability concepts behind intelligent message classification.

---

## 📌 Project Overview

Spam messages are one of the biggest challenges in digital communication. They waste user time, spread phishing attacks, and reduce communication efficiency.

This project develops a **Message Intelligence System** that automatically classifies messages as **Spam** or **Legitimate (Ham)** using supervised machine learning algorithms.

The project not only focuses on model building but also demonstrates:

- 📊 Exploratory Data Analysis (EDA)
- 🧹 Data Cleaning & Preprocessing
- 📈 Feature Engineering
- 🤖 Machine Learning Classification
- 📐 Probability Concepts
- 📊 Model Evaluation & Comparison

---

# 🎯 Objectives

- Detect spam messages automatically.
- Compare multiple classification algorithms.
- Understand the probability concepts behind Naive Bayes.
- Evaluate model performance using multiple metrics.
- Build a complete end-to-end Machine Learning workflow.

---

# 🗂 Dataset Features

The dataset contains various numerical features extracted from messages.

| Feature | Description |
|----------|-------------|
| message_length | Total number of characters in the message |
| num_digits | Number of numeric characters |
| num_special_chars | Number of special characters |
| num_urls | Number of URLs present |
| spam_keyword_score | Spam-related keyword score |
| legit_keyword_score | Legitimate keyword score |
| sender_account_age_days | Sender account age |
| sender_activity_score | Sender activity level |
| messages_sent_last_24h | Number of messages sent in last 24 hours |
| hour_of_day | Message sending hour |
| day_of_week | Day when message was sent |
| spam_label | Target Variable |

---

# 🧹 Data Preprocessing

The following preprocessing steps were performed:

✅ Duplicate Removal

- Dataset checked for duplicate records.
- No duplicate records were found.

---

## 📊 Exploratory Data Analysis (EDA)

The project includes:

### 🔹 Univariate Analysis

- Distribution of each feature
- Class distribution
- Skewness analysis

Observation:

- Spam class is moderately imbalanced.
- Several numerical features show positive skewness.

---

### 🔹 Bivariate Analysis

Relationship between individual features and spam label was analyzed.

Important observations:

- Spam messages contain more URLs.
- Spam messages contain more special characters.
- Spam messages have higher spam keyword scores.
- Sender accounts are generally newer.
- Messages are sent more frequently within 24 hours.

---

### 🔹 Multivariate Analysis

Correlation heatmap was generated.

Strong Positive Features:

- Number of Special Characters
- Messages Sent Last 24 Hours
- Spam Keyword Score
- Number of URLs

Strong Negative Features:

- Legit Keyword Score
- Sender Account Age

---

# ✂️ Feature Selection

Features removed:

- message_id
- message_length
- sender_activity_score
- hour_of_day
- day_of_week

Reason:

- Weak correlation with target
- Low predictive importance
- Identifier column provides no learning information

---

# 🔧 Missing Value Handling

Missing values were identified and handled appropriately before model training.

---

# ⚖ Feature Scaling

Numerical features were standardized before training distance-based models such as:

- KNN
- SVM

This ensures fair distance calculations.

---

# 🤖 Machine Learning Models

Three supervised learning algorithms were implemented.

## 1️⃣ K-Nearest Neighbors (KNN)

### Working Principle

- Finds K nearest neighbors
- Uses Euclidean Distance
- Predicts majority class

Hyperparameter tuning performed using:

- GridSearchCV
- Stratified 5-Fold Cross Validation

Best K selected automatically.

---

## 2️⃣ Support Vector Machine (SVM)

Two kernels were evaluated:

- Linear Kernel
- RBF Kernel

SVM separates classes by maximizing the margin between them.

Cross-validation was performed to verify model consistency.

---

## 3️⃣ Naive Bayes

Naive Bayes is a probabilistic classifier based on **Bayes' Theorem**.

Assumption:

> All input features are conditionally independent given the class label.

Additional probability concepts demonstrated:

- Conditional Probability
- Bayes' Theorem
- Posterior Probability

---

# 📐 Probability Concepts Implemented

This notebook also explains:

- Conditional Probability
- Bayes' Theorem
- Prior Probability
- Likelihood
- Posterior Probability

These concepts explain how Naive Bayes predicts whether a message is spam.

---

# 📊 Model Evaluation Metrics

Models were evaluated using:

- Precision
- Recall
- F1 Score
- Confusion Matrix
- Stratified K-Fold Cross Validation

---

# 📈 Results

| Model | Precision | Recall | F1 Score | Cross Validation |
|--------|-----------|--------|----------|------------------|
| KNN | 1.00 | 1.00 | 1.00 | 1.00 |
| SVM (Linear) | 1.00 | 1.00 | 1.00 | 1.00 |
| SVM (RBF) | 1.00 | 1.00 | 1.00 | 1.00 |
| Naive Bayes | 1.00 | 1.00 | 1.00 | 1.00 |

---

# 📊 Confusion Matrix

For every model:

- True Positives = 197
- True Negatives = 843
- False Positives = 0
- False Negatives = 0

This indicates perfect classification on the evaluation dataset.

---

# 🏆 Key Findings

- Excellent separation between spam and legitimate messages.
- Spam keyword score is a highly informative feature.
- URLs strongly indicate spam messages.
- Older sender accounts are more likely to be legitimate.
- All three classifiers achieved identical performance on this dataset.

---

# 💻 Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# 📚 Machine Learning Concepts Covered

- Data Cleaning
- Exploratory Data Analysis
- Feature Selection
- Feature Scaling
- Train-Test Split
- KNN
- Support Vector Machine
- Naive Bayes
- Conditional Probability
- Bayes' Theorem
- Hyperparameter Tuning
- GridSearchCV
- Stratified K-Fold Cross Validation
- Precision
- Recall
- F1 Score
- Confusion Matrix

---
