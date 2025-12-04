Customer Churn Prediction Using Artificial Neural Network (ANN)
Project Overview
Customer churn refers to the phenomenon where customers stop doing business with a company. Predicting churn helps businesses proactively identify at-risk customers and improve retention strategies. In this project, we analyze customer churn in the telecom industry and build a deep learning model (ANN) to predict which customers are likely to churn.
The model is evaluated using metrics such as accuracy, precision, recall, and F1-score.
Dataset
The dataset used contains customer information from a telecom company, including demographics, account information, and service usage.
Columns include: gender, SeniorCitizen, Partner, Dependents, tenure, PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies, Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges, Churn.
Source: customer_churn.csv (CSV file)
Key Steps
1. Data Preprocessing
Dropped customerID column as it is not useful for prediction.
Converted TotalCharges from string to numeric, handling missing/blank values.
Converted categorical Yes/No columns to binary 1/0.
Replaced values like No internet service and No phone service with No.
Converted categorical features to one-hot encoding for machine learning compatibility.
Scaled numeric columns (tenure, MonthlyCharges, TotalCharges) using MinMaxScaler.
2. Exploratory Data Analysis (EDA)
Visualized customer churn trends based on tenure and monthly charges.
Checked unique values of categorical columns to ensure data consistency.
3. Model Building (Artificial Neural Network)
Built a Sequential ANN model with:
Input layer: 26 features
Hidden layers: 2 layers with 26 and 15 neurons respectively, ReLU activation
Output layer: 1 neuron with Sigmoid activation (binary classification)
Compiled with Adam optimizer and binary cross-entropy loss.
Trained for 100 epochs on 80% of the dataset.
4. Model Evaluation
Evaluated using accuracy and metrics such as precision, recall, and F1-score.
Split dataset: 80% training, 20% testing.
Achieved high predictive performance in identifying customers likely to churn.
Technologies & Libraries
Programming Language: Python
Libraries: Pandas, NumPy, Matplotlib, Scikit-learn, TensorFlow/Keras
Data Visualization: Histograms and bar plots for churn distribution
