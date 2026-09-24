# IPL Matches Data Analysis using Pandas[cite: 7]

## Overview
This repository contains a Jupyter Notebook demonstrating foundational Exploratory Data Analysis (EDA) and data cleaning techniques using the Python `pandas` library[cite: 7]. The analysis is performed on a historical dataset of IPL cricket matches (`matches.csv`), covering seasons from 2007/08 through 2024[cite: 7].

## Dataset
*   **File:** `matches.csv`[cite: 7]
*   **Initial Dimensions:** 1,095 rows and 20 columns[cite: 7]
*   **Key Features:** Includes comprehensive match details such as `season`, `city`, `date`, `team1`, `team2`, `toss_winner`, `toss_decision`, `winner`, `target_runs`, and `umpires`[cite: 7].

## Prerequisites
To execute the notebook, ensure you have the following installed in your environment:
*   Python 3.x[cite: 7]
*   Pandas (`pip install pandas`)[cite: 7]
*   Jupyter Notebook / JupyterLab

## Key Operations Covered

### 1. Data Loading and Inspection
*   **Data Ingestion:** Loaded the raw CSV dataset into a Pandas DataFrame using `pd.read_csv()`[cite: 7].
*   **Initial Exploration:** Inspected the top and bottom rows using `df.head()` and `df.tail(10)`[cite: 7].
*   **Structural Overview:** Evaluated the dataset's footprint using `df.shape`, `len(df)`, and `df.columns`[cite: 7].
*   **Schema Information:** Reviewed column data types and non-null counts via `df.info()`[cite: 7].

### 2. Data Cleaning Pipeline
*   **Duplicate Handling:** Assessed the dataset for duplicated records using `df.duplicated().sum()`[cite: 7].
*   **Missing Value Identification:** Quantified null values across all columns utilizing `df.isnull().sum()`[cite: 7].
*   **Feature Pruning:** Removed the sparsely populated `method` column using `df.drop(columns="method", inplace=True)`[cite: 7].
*   **Null Value Resolution:** Dropped remaining rows containing missing values via `df.dropna(inplace=True)`, resulting in a clean dataset of 1,028 rows and 19 columns[cite: 7].

### 3. Data Analysis and Manipulation
*   **Column Indexing:** Extracted specific single columns (`df['method']`) and multiple column subsets (`df[['toss_decision', 'winner', 'city']]`)[cite: 7].
*   **Statistical Summary:** Generated standard descriptive statistics (mean, min, max, standard deviation, quartiles) for numerical features using `df.describe()`[cite: 7].
*   **Row Indexing:** Extracted specific row records using integer-location based indexing via `df.iloc[0]`[cite: 7].

## Usage Instructions
1. Clone this repository to your local machine.
2. Ensure the `matches.csv` data file is located in the same directory as the Jupyter Notebook[cite: 7].
3. Open the notebook in your Jupyter environment.
4. Run the cells sequentially to execute the data transformation and analysis pipeline.
