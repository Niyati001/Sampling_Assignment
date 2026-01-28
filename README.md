# Sampling_Assignment
Predictive Analysis assignment 1 on sampling by Dr. Anjula Mehto

Sampling Assignment – Credit Card Fraud Detection

Problem Statement:
This assignment focuses on understanding how different sampling techniques affect the performance of machine learning models. Since the given dataset is imbalanced, sampling is required to improve learning and accuracy.

Dataset:
The dataset used is Creditcard_data.csv.
Target column: Class
0 → Normal transaction
1 → Fraud transaction

Initially, the dataset had very few fraud cases, making it highly imbalanced.
Data Balancing:
To handle the imbalance, SMOTE was applied.
This technique oversamples the minority class and helps in creating a balanced dataset with equal class distribution.

Sampling Techniques:
After balancing the data, five samples were created using the sample size formula discussed in class.
The following sampling techniques were applied:
Sampling1 – Simple Random Sampling
Sampling2 – Systematic Sampling
Sampling3 – Stratified Sampling
Sampling4 – Cluster Sampling
Sampling5 – Convenience Sampling

Machine Learning Models:
Five machine learning models were used:
M1 – Logistic Regression
M2 – Decision Tree
M3 – KNN
M4 – Naive Bayes
M5 – Random Forest
Data was split into 80% training and 20% testing.

Results:
Model	S1	S2	S3	S4	S5
M1	50.10	52.24	63.18	69.23	70.12
M2	59.25	65.27	68.72	28.36	30.25
M3	90.45	72.41	32.17	42.58	41.85
M4	78.25	56.24	47.23	33.44	40.12
M5	81.25	12.85	57.36	32.25	52.74

Analysis:
The results show that different sampling techniques work better for different models.
Sampling1 performs best for M3
Sampling5 gives better accuracy for M1
Model performance changes significantly with sampling method
A comparison graph is included in the notebook for better understanding.

Conclusion
This assignment shows that sampling techniques have a strong impact on model accuracy. There is no single best sampling method for all models, and choosing the right technique is important for better results.

Tools Used:
Python
Google Colab
Pandas, NumPy
Matplotlib
Scikit-learn
