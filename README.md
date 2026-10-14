# Housing Market Downturn Prediction

This README covers:
- Project overview and team
- Folder structure and rationale for not tracking data
- Step-by‑step data filekeeping and download instructions

## Project Overview
This project develops machine learning models for early detection of housing market downturns using the **HouseTS dataset** (ZIP‑code‑level spatiotemporal data from 2012–2023, covering 30 U.S. metropolitan areas). The goal is to predict whether a ZIP code will experience a price drop of more than 10% within the next six months.

We implement and compare:
- Logistic Regression
- Random Forest

Key features include price trends, volatility, sale‑to‑list gaps, inventory turnover, and lagged indicators. The repository contains data cleaning, feature engineering, exploratory analysis (PCA/K‑means), and model training/evaluation notebooks.

## Repository Structure

housing-market-downturn-prediction/
├── data/
│ ├── raw/ # Place HouseTS.csv here (not tracked by git)
│ ├── processed/ # Cleaned and engineered datasets (not tracked)
│ └── result/ # Prediction outputs (CSV files)
├── notebooks/
│ ├── 01_data_cleaning.ipynb
│ ├── 02_feature_engineering.ipynb
│ ├── 03_PCA_KMeans.ipynb
│ ├── 04_LogisticRegression.ipynb
│ └── 05_RandomForest.ipynbs
├── .gitignore # Excludes data/raw, data/processed, etc
├── requirements.txt # Python dependencies
└── README.md

**Important:** All data files ('.csv') are **excluded from version control** via `.gitignore`. You must obtain the dataset separately (see below).

## Data Filekeeping & Obtaining the Data
The raw dataset (**HouseTS.csv**) is **not** stored in this repository to avoid large file size and license restrictions. To run the notebooks:

1. Download the dataset from Kaggle:  
   [HouseTS Dataset – shengkunwang/housets-dataset](https://www.kaggle.com/datasets/shengkunwang/housets-dataset)
2. Place the downloaded 'HouseTS.csv' file inside the 'data/raw/' folder.
3. The cleaning and feature engineering notebooks will read from 'data/raw/' and write processed files to 'data/processed/' (which is also ignored by git).

All intermediate and final results (predictions, cleaned data) are stored in 'data/processed/' and 'data/result/' which are **not** pushed to GitHub to keep the repository lightweight.

If you clone this repository, you must manually create the 'data/raw/' folder and add the CSV file.


