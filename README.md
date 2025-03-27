# Connecting to SQL

## 1. Overview  
This program allows users to query a **SQL Server** database for historical **security price** data. Users can input a `securityid` and a date range to retrieve data from the `security_price` table. The program establishes a secure connection to the database, executes the query, and outputs the results using **pandas**.

## 2. Features
- Dynamic SQL query generation based on user input.
- Option to choose between multiple servers.
- Validates user input to prevent invalid date ranges.
- Displays results in a readable pandas DataFrame format.
- Secure connection to the database using Windows Authentication.

## 3. Requirements/Dependencies
- Python 3.10.9
- pandas – for handling data in DataFrame format.
- pyodbc – for connecting to the SQL Server database.

### Install dependencies using:

```bash
pip install pandas pyodbc
```
## 4. Usage Instructions

### 1. Clone the repository:
```bash
git clone https://github.com/your-username/sql-query-tool.git
```
### 2. Navigate to the project folder:
```bash
cd sql-query-tool
```
### 3. Run the script:
```bash
python main.py
```
### 4. Follow the prompts:

1. **Choose a server:**

   - PSQL103-USEA1A
   - PSQL102-USEA1A

2. **Enter the securityid:**

```bash
Enter the security ID: 12345
Enter the date range in YYYY-MM-DD format:
```

3. **Enter the date range in YYYY-MM-DD format:**
```bash
Enter the start date (YYYY-MM-DD): 2025-01-01  
Enter the end date (YYYY-MM-DD): 2025-03-01  
```

## 5. Known Issues & Limitations
- Does not support older Excel file formats (.xls).

- Error handling is basic; files without any sheets or with special characters may cause issues.

- The program does not support Excel files that contain complex formulas or formatting.

## 6. Future Enhancements
- Support for older Excel file formats (.xls).

- Option to choose the destination folder for CSV files.

- Multi-threading to handle large files faster.

- More robust error handling for edge cases (empty sheets, special characters, etc.).

## 7. Testing
- The program was tested using basic Excel sheets composed of multiple worksheets. The tests confirmed that the program can:

- Correctly process Excel files with multiple sheets.

- Convert each sheet to an individual CSV file.

- Save the CSV files in the same folder as the original Excel file. Testing was conducted with sample Excel files containing varying numbers of sheets to ensure the program handles typical use cases.

