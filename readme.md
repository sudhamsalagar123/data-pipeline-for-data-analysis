🧼 Customer Sales Data Preprocessing Pipeline
This project demonstrates a complete data preprocessing workflow for a customer sales dataset, from data cleaning to feature engineering and transformation — preparing it for machine learning models.

📂 Project Overview
Goal:
To clean and preprocess customer data for machine learning, enabling predictive modeling — specifically to predict high-value customers based on behavior and demographics.

✅ Steps Performed
1. Load the Dataset
Reads the dataset from customer_sales_dataset.csv

Displays shape, sample rows, summary statistics, and missing value counts

2. Data Cleaning
Date Parsing: Converts purchase_date to datetime

Missing Values:

Numerical columns: Filled with mean

Categorical columns: Filled with most frequent (mode)

email and address: Filled with placeholders

Ensures a clean dataset with no missing values

3. Exploratory Data Analysis (Basic)
Outputs distributions of:

Gender

Product categories

Saves a histogram plot of purchase amounts as purchase_distribution.png

4. Feature Engineering
Extracted Features:

purchase_month: Month from purchase_date

loyalty_score: Combines recency and satisfaction score; clipped between 1–5

high_value_customer: Flag for customers with above-average income and purchase amount

5. Feature Preprocessing for Machine Learning
Drops non-informative fields (customer_id, email, etc.)

Splits data into train and test sets

Defines:

Numerical pipeline: Imputation + standard scaling

Categorical pipeline: Imputation + one-hot encoding

Applies transformations using ColumnTransformer

Outputs the shape of the final preprocessed datasets

6. Save Cleaned Data
Saves the cleaned dataset to cleaned_customer_data.csv

🧪 Output
✅ cleaned_customer_data.csv: Cleaned and enriched data

✅ purchase_distribution.png: Histogram plot of purchase amounts

✅ X_train_processed & X_test_processed: Final processed feature arrays ready for modeling

🚀 Next Steps
You can now use the preprocessed data to:

Train classification models (e.g., Logistic Regression, Random Forest)

Evaluate model performance using y_test

Tune hyperparameters or perform cross-validation

🛠️ Libraries Used
pandas, numpy

matplotlib, seaborn

scikit-learn (for imputation, scaling, encoding, splitting, and pipelines)

📁 File Structure
bash
Copy
Edit
.
├── customer_sales_dataset.csv           # Original dataset
├── cleaned_customer_data.csv            # Cleaned and enriched dataset
├── purchase_distribution.png            # Distribution plot
├── your_preprocessing_script.py         # (The script you wrote)
└── README.md                            # Project documentation
