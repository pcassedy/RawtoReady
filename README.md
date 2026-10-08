# RawtoReady

**Live demo:** https://rawtoready-sprint5.streamlit.app/
**Paper:** [RawtoReady: A Web-Based Automated Tool for Data Cleaning and Preparation](https://doi.org/10.46254/GC03.20250536), 3rd GCC International Conference on IEOM, Tabuk, Saudi Arabia, February 2026 (1st Place, Undergraduate Research Competition)

## Background

RawtoReady is an interactive web application that simplifies data cleaning for students, researchers, and analysts. Users upload a CSV dataset, apply the cleaning operations they need, and download a cleaned dataset that is ready for analysis, with no coding required.

## Features

**Cleaning tools**
- Fill or drop missing values
- Remove duplicate rows
- Standardize column names
- Normalize text
- Fix date formats
- Validate email addresses
- Fuzzy standardization of similar text values
- Numeric anomaly (outlier) detection using a z-score method

**Reporting and history**
- Cleaning Summary Report with statistics before and after cleaning
- Cleaning History: track past runs, rename files, or delete records
- Download the cleaned dataset as a CSV

**Accounts (optional)**
- User registration and login with SHA-256 password hashing
- Guests can use the app without an account, but only logged-in users get saved cleaning history

## How to use it

1. Upload your CSV file.
2. Preview the raw dataset.
3. Choose cleaning options from the sidebar. Tooltips explain which suit your data.
4. Click **Run Cleaning**.
5. Review the results under **Raw Data Preview**, **Cleaned Data Preview**, and **Anomalies Detected**.
6. Read the Summary Report to see what changed.
7. Download the cleaned CSV.

**Creating an account (optional):** click "Create Account" on the login page, register, then log in. Your cleaning history is saved and can be viewed, edited, or deleted anytime.

## Run it locally

```bash
git clone https://github.com/pcassedy/RawtoReady.git
cd RawtoReady
pip install -r requirements.txt
streamlit run app.py
```

Open the local URL shown in your terminal. The user database (`users.db`) is created automatically on first run.

## Tech stack

- **Frontend:** Streamlit
- **Backend:** Python (Pandas, NumPy, regex, difflib)
- **Database:** SQLite
- **Security:** SHA-256 password hashing

## Project structure

```
RawtoReady/
├── .streamlit/config.toml   # theme
├── app.py                   # the application
├── logo.png
├── logonobg.png
├── requirements.txt
└── README.md
```

## Team

RawtoReady was developed as a Software Development course project by 3rd-year Data Science students at Mapua University:

- Gio Miguel R. Bihasa
- Pam Cassedy T. Dumangeng
- Kim Caryl H. Esperanza
- Louella Josephine A. Ng

The original team repository, built in sprints, is at https://github.com/kmcryle/RawtoReady.
