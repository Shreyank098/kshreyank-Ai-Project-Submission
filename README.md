📧 Email Sentiment Analysis & Flight Risk Prediction

This project analyzes internal email data to label sentiments, identify patterns, assess employee communication trends, and predict potential flight risks using natural language processing (NLP) and machine learning.

📌 Features
✅ Python scripts implementing:

1. Sentiment Labeling (Positive, Negative, Neutral)
2. EDA & Data Visualizations
3. Monthly Sentiment Scoring
4. Employee Sentiment Ranking
5. Flight Risk Identification (based on rolling negative sentiment count)
6. Linear Regression Model for message length prediction
7. Automatically saves plots to /visualization

🎯 Aim
To evaluate employee sentiment over time using email content, identify high-risk individuals through communication tone, and develop analytical insights for HR decision-making.

📄 Dataset
The dataset consists of Enron-style email metadata with the following columns:

Subject – Email subject line | body – Email content (used for sentiment) | date – Date of the email | from – Sender's email address (used to identify employee)

⚙️ How It Works
1. Load and Clean Data - Parse and rename columns - Remove null values

2. Sentiment Labeling
Uses TextBlob to classify messages into Positive, Neutral, or Negative.

3. Visualizations
Sentiment distribution bar chart - Employee ranking by negative/positive sentiment - Monthly sentiment score trend

4. Feature Engineering
Extract message length and word count - Generate TF-IDF matrix for regression

5. Predictive Modeling
Ridge Regression predicts message length from TF-IDF features - Model evaluation: RMSE and R² Score

6. Flight Risk Identification
Calculates 30-day rolling sum of negative emails - Employees with ≥4 negative emails in 30 days are flagged

📊 Results

Regression RMSE: ~118.1
R² Score: ~0.75

High-Risk Employees (≥4 negative emails in a 30-day window) are listed in console output
