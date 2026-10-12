# Customer Shopping Behavior Analysis

## Project Overview

This project focuses on analyzing customer shopping behavior using Python, Pandas, and PostgreSQL. The main objective is to clean and preprocess customer shopping data, perform feature engineering, and store the processed data in a PostgreSQL database for further analysis.

The project demonstrates practical skills in data preprocessing, data transformation, database connectivity, and database management using pgAdmin 4.

## Objectives

- Explore and understand customer shopping data.
- Identify and handle missing values.
- Clean column names and standardize data.
- Perform feature engineering by creating customer age groups.
- Convert purchase frequency categories into numerical day values.
- Examine the relationship between discount usage and promotional codes.
- Store processed data in PostgreSQL.
- Manage and inspect database tables using pgAdmin 4.

## Dataset

**Dataset Name:** Shopping Behaviour Dataset

**Source:** Kaggle

[View and download the dataset on Kaggle](https://www.kaggle.com/datasets/saadaliyaseen/shopping-behaviour-dataset)

The dataset contains customer shopping information that can be used to explore purchasing patterns, product categories, purchase amounts, review ratings, and shopping frequency.

*Note: Please check the dataset's license and usage terms before redistributing the original dataset in this repository.*

## Technologies Used

- **Python** – Data processing and analysis
- **Pandas** – Data cleaning and transformation
- **Jupyter Notebook** – Writing and executing Python code
- **PostgreSQL** – Storing processed data
- **pgAdmin 4** – Graphical database management
- **SQLAlchemy** – Connecting Python to PostgreSQL
- **Psycopg2** – PostgreSQL database adapter

## Project Workflow

### 1. Data Loading and Exploration
- Loaded the shopping behavior dataset into a Pandas DataFrame.
- Inspected the first few rows and dataset structure.
- Reviewed summary statistics and checked for missing values.

### 2. Data Cleaning
- Handled missing values in the `Review Rating` column using category-wise median values.
- Converted column names to lowercase.
- Replaced spaces in column names with underscores.
- Renamed the purchase amount column for easier use.

### 3. Feature Engineering
- Created an `age_group` column by grouping customers into age categories.
- Converted purchase frequency categories into numerical day values.
- Compared the `discount_applied` and `promo_code_used` columns.
- Removed the `promo_code_used` column after examining the relationship between the two fields.

### 4. Database Integration
- Connected Python to PostgreSQL using SQLAlchemy and Psycopg2.
- Stored the processed DataFrame in a PostgreSQL table named `customer`.
- Used pgAdmin 4 to access and manage the database and inspect the stored table.

## Repository Structure

```text
customer-shopping-behavior-analysis/
│
├── project.ipynb
└── README.md
      ├── customer_shopping_behavior.csv
      ├── Customer_behavior_dashboard.xlsx
```

*Update the filenames and extensions above to match the files you actually upload. Include the dashboard only if you want to share it, and do not upload credentials or other sensitive information.*

## How to Run the Project

### Prerequisites
- Python 3.x
- Jupyter Notebook
- PostgreSQL
- pgAdmin 4

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/customer-shopping-behavior-analysis.git
cd customer-shopping-behavior-analysis
```

### Step 2: Install Required Libraries

```bash
pip install pandas sqlalchemy psycopg2-binary jupyter
```

### Step 3: Prepare the Dataset

Place the CSV dataset in the project directory and ensure its filename matches the one used in the notebook.

### Step 4: Configure PostgreSQL

- Start your PostgreSQL server.
- Create the database `customer_behavior`.
- Configure the connection securely using environment variables.
- Open the notebook and update the connection code to read those variables instead of containing hardcoded credentials.

### Step 5: Run the Notebook

```bash
jupyter notebook
```

Open `project.ipynb` and run the cells in order.

## Database Details

- **Database:** `customer_behavior`
- **Table:** `customer`
- **Database Tool:** pgAdmin 4
- **Python Connectivity:** SQLAlchemy and Psycopg2

The notebook writes the processed customer data into PostgreSQL. Ensure the database exists and the connection settings are correct before running the database section.

## Key Learnings

- Data cleaning and preprocessing using Pandas
- Handling missing values with group-based median imputation
- Feature engineering and categorical data transformation
- Connecting Python applications to PostgreSQL
- Managing databases using pgAdmin 4
- Organizing a data analytics project for GitHub

## Author

**Abhinav Pradhan**

GitHub: [GitHub Profile](https://github.com/abhinavpradhan-dotcom)
