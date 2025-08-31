Predictive Maintenance in Manufacturing (Regression with Overfitting Resolution)
📌 Problem Statement

This project focuses on predicting days to equipment failure using sensor data collected from heavy machinery. The dataset includes:

Temperature (°C)

Vibration (mm/s)

Pressure (psi)

Runtime (hours)

Target: Days to failure (continuous value)

The initial Linear Regression model suffered from overfitting, meaning it performed well on training data but poorly on unseen test data. The objective was to resolve overfitting using ensemble learning techniques and evaluate the performance.

⚡ Tasks & Solutions
a) Understanding Overfitting & Bias-Variance Tradeoff

Overfitting: The model memorized noise in the training data instead of learning general patterns.

Bias-Variance Tradeoff:

High bias → underfitting (oversimplifies patterns).

High variance → overfitting (too sensitive to noise).

Goal: balance both to achieve good generalization.

b) Model Development (Gradient Boosting)

We chose Gradient Boosting Regressor because:

Handles non-linear relationships.

Reduces overfitting by building trees sequentially with error correction.

Typically outperforms linear models on complex industrial datasets.

Steps in Python (scikit-learn):

Import required libraries.

Load dataset and preprocess (features & target).

Train-test split (80/20).

Fit a Gradient Boosting Regressor.

Predict on the test set.

c) Model Evaluation

We evaluated using:

RMSE (Root Mean Squared Error) – lower is better.

R² (Coefficient of Determination) – closer to 1 means better fit.

5-Fold Cross-Validation – ensures generalization across subsets.




d) Feature Engineering & Improvements

Normalized temperature values.

Real-world application: predictive alerts for maintenance scheduling and downtime reduction.

📊 Results

Gradient Boosting outperformed Linear Regression.

Overfitting reduced via ensemble learning.

Generalization improved with cross-validation.

🛠️ Tech Stack

Python 3

pandas, numpy (data handling)

scikit-learn (machine learning)

matplotlib, seaborn (visualization)

🚀 How to Run

Clone this repo:


Install dependencies:

pip install -r requirements.txt


Run the notebook/script:


📌 Expected Output

RMSE < 50 on test set

R² close to 1

