Pandas Practice

Practice notebooks to learn Pandas for data analysis. I solve practice questions on a synthetic orders dataset (200 rows). The data is made up. It is not real customer data.

The questions are listed in QUESTIONS.md. I will keep adding more.

Skills practiced
Loading data with read_csv
Looking at data: head(), tail(), columns
Selecting columns (Series and DataFrame)
Selecting rows and columns with loc and iloc
Boolean masks with &, |, ~, isin()
Finding missing and wrong values with isna() and notna()
Files
File	What it has
Select Columns.ipynb	Selecting columns
loc_iloc.ipynb	loc and iloc practice
Mask.ipynb	Filtering rows with masks
Data cleaning.ipynb	Finding missing and wrong values
orders_practice.csv	Synthetic orders dataset
QUESTIONS.md	Practice questions
Dataset columns

Order ID, Customer Name, Gender, Age, City, Order Date, Product, Qty, Unit Price, Total Amount, Payment Mode, Rating

The data has some missing values (Age, City, Rating) and a few wrong ages, so it is good for cleaning practice.

How to run
pip install pandas notebook
python -m notebook

Open any notebook and run the cells from top to bottom. Keep orders_practice.csv in the same folder.

What's next
Cleaning with fillna(), dropna(), drop_duplicates()
Analysis with groupby()
Using these skills on a real orders dataset
