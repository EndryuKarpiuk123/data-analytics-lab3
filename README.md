# Practical Work No. 3 - Data Cleaning and Transformation

This repository contains my solution for Practical Work No. 3. The goal of the work is to gain practical skills in detecting and handling missing values, duplicates and outliers; converting data types; working with string and datetime values; creating new features; encoding categories; applying normalisation and standardisation; and building a reproducible data-cleaning pipeline.

## Repository contents

| File | Description |
|------|-------------|
| `karpiuk_lb3.ipynb` | Practical part (Steps 1-10): missing values, duplicates, outliers (IQR), type conversion, string cleaning, feature engineering, one-hot encoding, normalisation / standardisation, and saving the cleaned dataset. |
| `karpiuk_tasks3.ipynb` | Individual tasks 1-7 and the additional ★ task (`clean_dataset()` function), plus answers to the self-check questions. |
| `README.md` | This file. |

## Dataset

The notebooks use `sales.csv` - a coffee shop transactions dataset:

| Column | Description |
|--------|-------------|
| `date` | Transaction date |
| `datetime` | Transaction date and time |
| `cash_type` | Payment type (`card` / `cash`) |
| `card` | Anonymised card identifier (empty for cash payments) |
| `money` | Transaction amount |
| `coffee_name` | Name of the drink |

If `sales.csv` is not found on Google Drive, the notebooks automatically generate a synthetic sample with the same structure (300 rows), so every cell can be run without extra preparation.

## How to run

1. Open [Google Colab](https://colab.research.google.com) and sign in with your Google account.
2. Choose **File → Upload notebook** and select one of the `.ipynb` files (or open it directly from GitHub).
3. Upload `sales.csv` to the root of your Google Drive (`MyDrive`), or skip this step to use the generated sample.
4. Run the cells in order with **Shift + Enter**. When prompted by `drive.mount('/content/drive')`, grant access to your Drive.

> Note: the notebooks save their output files (`cleaned_sales.csv`, `sales_cleaned_task2.csv`, `cleaned_test_dataset.csv`) to the root of Google Drive.

## Requirements

- Python 3 (pre-installed in Google Colab)
- `pandas`
- `numpy`

## What was covered

- Missing values: `isnull().sum()`, `dropna()`, `fillna()` with mean, median and mode
- Duplicates: `duplicated()`, `drop_duplicates()`
- Outliers: the interquartile range (IQR) method
- Type conversion: `pd.to_datetime()` and the `.dt` accessor
- String cleaning with the `.str` accessor: `strip()`, `lower()`, `replace()` (including regular expressions)
- Feature engineering: year, month, day, day of week, hour; `np.where()`
- One-hot encoding with `pd.get_dummies()`
- Min-max normalisation and standardisation (and how to verify them)
- A reusable `clean_dataset()` function that combines all cleaning steps (★ task)

## Author

Karpiuk
