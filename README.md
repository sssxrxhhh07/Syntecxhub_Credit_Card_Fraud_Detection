💳 Credit Card Fraud Detection under Class Imbalance

Random Forest, XGBoost, SMOTE & Threshold Optimization

A Machine Learning project focused on detecting fraudulent credit card transactions in a highly imbalanced dataset. This project explores multiple sampling techniques, compares classification models, evaluates fraud-specific performance metrics, and identifies business-oriented decision thresholds for real-world fraud detection systems.

📊 Project Overview

Credit card fraud detection is a challenging classification problem because fraudulent transactions represent only a very small fraction of total transactions. Traditional machine learning models often struggle to learn patterns from such imbalanced data.

This project investigates how different balancing techniques and machine learning algorithms affect fraud detection performance while addressing the tradeoff between fraud prevention and customer experience.

The project covers:

* Exploratory Data Analysis (EDA)
* Class Imbalance Visualization
* Data Preprocessing & Normalization
* Random Undersampling
* Random Oversampling
* SMOTE (Synthetic Minority Oversampling Technique)
* Random Forest Classification
* XGBoost Classification
* Precision, Recall, F1-Score Evaluation
* ROC-AUC & PR-AUC Analysis
* Threshold Optimization
* Business Decision Framework

🎯 Objectives

* Analyze fraudulent transaction patterns
* Visualize severe class imbalance
* Compare sampling techniques for imbalanced learning
* Train and evaluate fraud detection models
* Optimize Precision-Recall tradeoffs
* Identify business-friendly operating thresholds
* Recommend fraud detection strategies based on risk tolerance


📈 Exploratory Data Analysis (EDA)

Dataset Exploration

The dataset was analyzed to understand transaction behavior and fraud distribution.

Analysis Performed

✅ Fraud vs Genuine Transaction Distribution

✅ Transaction Amount Analysis

✅ Correlation Heatmaps

✅ Feature Distribution Analysis

✅ Outlier Detection

✅ Fraud Pattern Discovery

Class Imbalance Visualization

The dataset is highly skewed toward legitimate transactions.

| Transaction Type | Count   |
| ---------------- | ------- |
| Genuine          | 284,315 |
| Fraudulent       | 492     |

Fraudulent transactions account for less than 0.2% of all transactions, making imbalance handling a critical step in model development.

⚖️ Sampling Techniques

To address class imbalance, multiple sampling approaches were implemented and compared.

1️⃣ Random Undersampling

Reduces the number of majority-class samples.

Advantages

* Faster training
* Balanced dataset

Limitations

* Loss of potentially useful information

2️⃣ Random Oversampling

Duplicates minority-class samples to improve representation.

 Advantages

* Retains all original data

 Limitations

* Increased risk of overfitting

3️⃣ SMOTE (Synthetic Minority Oversampling Technique)

Generates synthetic fraud samples using nearest-neighbor interpolation.

Advantages

* Better minority representation
* Improved generalization
* Reduced overfitting compared to simple oversampling

Result

🏆 SMOTE provided the best balance between fraud detection performance and model stability.


🤖 Machine Learning Models

Random Forest Classifier

An ensemble learning algorithm that combines multiple decision trees to improve classification performance.

Strengths

* Handles non-linear relationships
* Robust against noise
* Strong baseline performance

XGBoost Classifier

A gradient boosting algorithm optimized for predictive accuracy and efficiency.

Strengths

* Excellent predictive power
* Effective on imbalanced datasets
* Captures complex fraud patterns


📊 Model Evaluation

Because fraud datasets are highly imbalanced, accuracy alone is not a reliable metric.

The following metrics were used:

Precision

Measures how many predicted fraud cases were actually fraudulent.

Recall

Measures how many actual fraud cases were successfully detected.

F1-Score

Balances Precision and Recall.

ROC-AUC

Measures the model's ability to distinguish fraud from genuine transactions.

PR-AUC

Measures performance specifically on imbalanced classification tasks.


Model Performance Comparison

| Metric    | Random Forest | XGBoost |
| --------- | ------------- | ------- |
| Precision | 96%           | 98%     |
| Recall    | 91%           | 94%     |
| F1 Score  | 93%           | 96%     |
| ROC-AUC   | 98%           | 99%     |
| PR-AUC    | 91%           | 95%     |

🏆 Best Performing Model: XGBoost

⚖️ Precision vs Recall Tradeoff

Fraud detection systems must balance two competing goals:

Higher Recall

✔ Detect more fraudulent transactions

✔ Reduce financial losses

❌ Generate more false alerts


Higher Precision

✔ Reduce false positives

✔ Improve customer experience

❌ May miss some fraud cases


Key Insight

The optimal solution depends on business priorities. A bank focused on minimizing fraud losses may prioritize Recall, while one focused on customer experience may prioritize Precision.


🎯 Threshold Optimization

Instead of relying on the default classification threshold (0.50), different operating thresholds were evaluated.

| Threshold | Impact                                           |
| --------- | ------------------------------------------------ |
| 0.20      | Maximum fraud detection, higher false positives  |
| 0.45      | Balanced fraud detection and customer experience |
| 0.75      | High-confidence alerts, fewer false positives    |


Recommended Thresholds

High-Risk Environment

Threshold: 0.20

* Detects most fraud cases
* Suitable for aggressive fraud prevention

 Balanced Strategy

Threshold: 0.45

* Balanced Precision and Recall
* Recommended for most institutions

Limited Investigation Capacity

Threshold: 0.75

* Only high-confidence fraud alerts
* Minimizes unnecessary reviews


🏦 Business Decision Framework

This project goes beyond model training by incorporating real-world business considerations.

 Key Questions Addressed

* How many fraud cases should be captured?
* How many false alerts are acceptable?
* What threshold provides the best business value?
* How should fraud investigation resources be allocated?


🛠️ Technologies Used

 Programming

* Python

 Data Analysis

* Pandas
* NumPy

 Visualization

* Matplotlib
* Seaborn

 Machine Learning

* Scikit-learn
* XGBoost
* Imbalanced-Learn (SMOTE)

 Development Environment

 Jupyter Notebook


 📂 Project Workflow

1. Data Collection & Understanding

Analyze transaction records and fraud labels.

2. Exploratory Data Analysis

Study fraud distribution and transaction characteristics.

3. Data Preprocessing

Normalize and prepare data for training.

4. Class Imbalance Handling

Apply Undersampling, Oversampling, and SMOTE.

5. Model Training

Train Random Forest and XGBoost models.

6. Model Evaluation

Evaluate Precision, Recall, F1, ROC-AUC, and PR-AUC.

7. Threshold Optimization

Identify optimal decision thresholds.

8. Business Analysis

Recommend deployment strategies based on business requirements.
For this project, if it's a Jupyter Notebook-based ML project, use:

🚀 Getting Started

Clone the Repository

```bash
git clone https://github.com/sssxrxhhh07/credit-card-fraud-detection.git

cd credit-card-fraud-detection
```
Open the Dashboard

Simply open:

```text
fraud_imbalance_lab_v2.html
```

in your browser.

No additional setup or installation is required.


📈 Key Results

✅ Successfully handled severe class imbalance

✅ Compared multiple sampling techniques

✅ Improved fraud detection using SMOTE

✅ XGBoost achieved the strongest overall performance

✅ Identified business-specific operating thresholds

✅ Demonstrated the importance of Precision-Recall tradeoffs

🎓 Skills Demonstrated

* Exploratory Data Analysis (EDA)
* Data Visualization
* Imbalanced Dataset Handling
* SMOTE Implementation
* Classification Modeling
* Random Forest
* XGBoost
* ROC-AUC & PR-AUC Analysis
* Threshold Optimization
* Fraud Analytics
* Financial Risk Assessment
* Business Decision Analysis

🔮 Future Improvements

* Real-Time Fraud Detection Pipeline
* Explainable AI with SHAP
* Hyperparameter Optimization
* Fraud Monitoring Dashboard
* Streamlit Deployment
* Deep Learning-Based Fraud Detection
* Automated Risk Scoring System

⭐ Conclusion

This project demonstrates how Machine Learning can be applied to detect fraudulent credit card transactions in highly imbalanced datasets. By combining advanced sampling techniques, powerful classification algorithms, threshold optimization, and business-oriented evaluation, the system provides a practical framework for real-world fraud detection and risk management.

If you found this project useful, consider giving the repository a ⭐! 🚀💳📊🤖
