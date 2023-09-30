# dataengineering_miniproject_1
dataengineering_miniproject_1 for learning how deploy data into database using psqul ,python,pandas

# PostgreSQL Database Creation and Data Import

This Python script allows you to create a PostgreSQL database, define a table schema, and insert data from a CSV file into the table. It is designed to automate the database setup process for managing movie-related data.

## Prerequisites

Before running the script, ensure that you have the following prerequisites installed:

- Python (3.x recommended)
- PostgreSQL database server
- Psycopg2 library (for Python PostgreSQL connections)
- Pandas library (for data manipulation)

You can install Psycopg2 and Pandas using pip:

```bash
pip install psycopg2 pandas
```

## Usage

1. Clone this repository or download the script to your local machine.

2. Open the script `create_database.py` and update the following variables with your PostgreSQL database connection details:

   - `host`: PostgreSQL host (e.g., "localhost").
   - `dbname`: Name of the default PostgreSQL database (e.g., "postgres").
   - `user`: PostgreSQL username.
   - `password`: PostgreSQL password.
   
   ```python
   host = "localhost"
   dbname = "postgres"
   user = "postgres"
   password = "password"
   ```

3. Ensure that you have a CSV file containing movie data (e.g., `netflix_titles.csv`) in the specified location. Update the file path accordingly:

   ```python
   movielist = pd.read_csv("path/to/netflix_titles.csv")
   ```

4. Customize the table creation and data insertion logic in the script to match your specific data schema and requirements. For example, you can modify the `CREATE TABLE` statement and `INSERT INTO` query.

5. Run the script:

   ```bash
   python create_database.py
   ```

6. The script will create a new database, define a table schema, and insert data from the CSV file into the table.

## Script Overview

- `create_database()`: Function to establish a connection to PostgreSQL, create the "movie1" database, and return a cursor and connection object for further operations.

- `tab_insert`: SQL query template for inserting data into the "movielist" table.

- `for` loop: Iterates through the cleaned movie data from the CSV file and inserts records into the database.


## Acknowledgments

- [Psycopg2](https://pypi.org/project/psycopg2/)
- [Pandas](https://pandas.pydata.org/)
```

