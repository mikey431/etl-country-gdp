# etl-country-gdp
ETL pipeline in Python to extract, transform, and load country GDP data from Wikipedia into CSV and SQLite.

# ETL Project – Country GDP Data

This project implements an **ETL (Extract, Transform, Load) pipeline** for country GDP data using Python, Pandas, and SQLite.  
The data is extracted from an archived version of the Wikipedia page:  
[List of countries by GDP (nominal)](https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29)

---

## Features
- **Extract**: Retrieve raw GDP data from an HTML table.
- **Transform**: Clean and convert GDP values from *USD millions* to *USD billions*, rounded to two decimal places.
- **Load**: Save the processed data to both a `.csv` file and a **SQLite** database.
- **Query**: Run SQL queries on the database (example: countries with GDP ≥ 100 billion USD).
- **Logging**: Log progress of the ETL process into `etl_project_log.txt`.

---

## Project Structure
- `etl_project.py` – main ETL pipeline script  
- `Countries_by_GDP.csv` – CSV file containing the transformed data  
- `World_Economies.db` – SQLite database created during execution  
- `etl_project_log.txt` – log file capturing ETL process steps  
- `README.md` – project documentation  

---

## How to Run

### 1. Clone the repository
```bash
git clone https://github.com/user/gdp_etl_project.git
cd gdp_etl_project
```
### 2.Create and activate a virtual environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```
### 3.Install dependencies
```bash
pip install -r requirements.txt
```
### 4.Run the ETL script
```bash
python etl_project.py

