# EDA_2_Visualization
Creating  Column, Bar and Frequency charts
Exploratory Data Analysis and visualization of a bank marketing campaign dataset using Python (pandas, Matplotlib, Seaborn).
# Bank Marketing Campaign: EDA & Visualization

## Description
This project performs Exploratory Data Analysis (EDA) on a bank's marketing campaign dataset. The goal is to clean the raw data, explore customer characteristics, and understand how factors like age, job, marital status, balance, loan status and call duration relate to whether a customer subscribed to a term deposit (`response`).

The project follows a complete analysis workflow: loading data, understanding it, cleaning it, and then visualizing it with univariate and bivariate analysis.

## Dataset
The dataset contains customer details and campaign information such as:

| Column | Meaning |
|---|---|
| age, salary, balance | Customer's age, annual income, average yearly balance |
| marital, job, education | Marital status and job/education details |
| housing loan, personal loan, default | Loan and credit default status |
| contact, day, month | How and when the customer was contacted |
| duration, campaign | Call length and number of contacts in this campaign |
| pdays, previous, poutcome | History of previous campaigns |
| response | Whether the customer subscribed to the term deposit (yes/no) |

## Data Cleaning Steps
- Skipped junk header rows while loading the file
- Removed rows with missing `age` and fixed the data type
- Dropped the `customerid` column (identifier only) and checked for duplicates
- Split `jobedu` into separate `job` and `education` columns
- Filled missing `month` with the mode and missing `response` with `no`
- Renamed columns for clarity (`housing` → `housing loan`, `loan` → `personal loan`)
- Converted `month` to datetime and extracted `month_name` and `year`
- Standardized `duration`, which had mixed units (seconds and minutes), into minutes

## Visualizations
**Univariate analysis:** histogram, KDE plot, pie chart, count plots, box plots, distribution plot

**Bivariate analysis:** violin plot, box plot, bar plot, count plot with hue, scatter plot, stacked bar chart

## Tech Stack
Python, pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Project Structure
```
bank-marketing-eda/
├── notebooks/
│   └── EDA_and_Visualization.ipynb
├── data/
│   └── bank_data.csv
├── requirements.txt
└── README.md
```

## How to Run
```bash
git clone https://github.com/<your-username>/bank-marketing-eda.git
cd bank-marketing-eda
pip install -r requirements.txt
jupyter notebook notebooks/EDA_and_Visualization.ipynb
```
Place `bank_data.csv` inside the `data/` folder before running.

## Key Insights
_Add 3-4 findings from your own plots here._

## Author
**Sanjeet Kumar**
Post-Graduate Program in Data Science & AI, Digicrome Academy
