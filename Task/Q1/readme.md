# Task 1 – Customer Data Preprocessing (Q1)

## 📌 Question / Task Description

**Task to do**

1. Install Python (Anaconda from www.anaconda.com)  
2. Create a data frame for customer information with the following columns:
   - **Customer ID**: A unique identifier for each customer  
   - **Age**: Age of the customer (numerical)  
   - **Gender**: Gender of the customer (categorical: 'Male' or 'Female')  
   - **Income**: Annual income of the customer (numerical)  
   - **City**: City of residence (categorical: 'Urban' or 'Rural')  
   - **Subscription Status**: Whether the customer has subscribed to a service (categorical: 'Subscribed' or 'Not Subscribed')  

3. Check for missing values; if yes then handle it using:
   - `isna()`  
   - `fillna()`  
   - `dropna()`  

4. Encode the categorical data (Gender, City, Subscription Status) using:
   - **Label Encoding** or  
   - **One-Hot Encoding**

5. Perform feature scaling on **Age** and **Income** using:
   - **MinMaxScaler**

---

# Task 2 – Data Loading & Visualization (Q1.2)

## 📌 Question / Task Description

**Task to do**

1. Load a sample dataset using pandas (e.g., Iris dataset or a custom CSV).

   ```python
   import pandas as pd
   df = pd.read_csv('file_path.csv')

---

## What this notebook does

The notebook `Answer_Q1.ipynb` performs all the required steps:

1. **Create the DataFrame**
   - Manually creates a small sample dataset with the required columns.
   - Introduces some `None` values to simulate missing data.

2. **Check Missing Values**
   - Uses `df.isna()` to show which cells are missing.
   - Uses `df.isna().sum()` to count missing values in each column.

3. **Handle Missing Values**
   - For numerical columns (**Age**, **Income**), fills missing values using the **mean** of the column with `fillna()`.
   - For categorical columns (**Gender**, **SubscriptionStatus**), fills missing values using the **mode** (most frequent value) with `fillna()`.
   - Explains in Markdown why we use mean/median/mode instead of random values.

4. **Encode Categorical Data**
   - Uses **Label Encoding** for:
     - `Gender` → `Gender_Encoded`
     - `SubscriptionStatus` → `Subscription_Encoded`
   - Uses **One-Hot Encoding** for:
     - `City` → `City_Urban`, `City_Rural` using `pd.get_dummies()`
   - Markdown explains what Label Encoding and One-Hot Encoding are and why they are needed for machine learning.

5. **Feature Scaling**
   - Uses **MinMaxScaler** from `sklearn.preprocessing` to scale:
     - `Age` and `Income`
   - Creates new columns:
     - `Age_Scaled`, `Income_Scaled`
   - Markdown explains why feature scaling is important and shows the MinMax formula.

---

## Files

- `task/Answer_Q1.ipynb`  
  Jupyter Notebook containing:
  - Code
  - Outputs (tables)
  - Beginner-friendly Markdown explanations for each step.

(Optionally, you can also add:)
- `task/data/customer_data.csv` – exported version of the final DataFrame  
- `task/requirements.txt` – list of Python dependencies (`pandas`, `scikit-learn`)

---

## How to Run

1. Install **Anaconda** from the official website.  
2. Open **Anaconda Prompt** and start JupyterLab:

   ```bash
   jupyter lab
