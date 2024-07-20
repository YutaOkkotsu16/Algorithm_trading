# Algorithm_trading
# Algo_1.py - Trading Strategy

## Overview
This Python script implements a simple trading strategy by fetching stock data from the IEX Cloud API, processing the data, and generating recommended trades based on a given portfolio size.

## Features
- Fetches stock data from the IEX Cloud API.
- Processes and organizes stock data into a Pandas DataFrame.
- Calculates the number of shares to buy based on the user's portfolio size.
- Exports the recommended trades to an Excel file with formatted styles for readability.

## Requirements
- Python 3.x
- Libraries: `numpy`, `pandas`, `requests`, `xlsxwriter`, `math`
- IEX Cloud API Token
- CSV file containing stock tickers (`sp_500_stocks.csv`)

## Setup
1. **Install Dependencies**:
    ```sh
    pip install numpy pandas requests xlsxwriter
    ```
2. **API Token**:
    - Ensure you have an IEX Cloud API token.
    - Store the token in a file named `secrets.py` with the following content:
      ```python
      IEX_CLOUD_API_TOKEN = 'your_api_token_here'
      ```
3. **Stock Data**:
    - Ensure you have a CSV file named `sp_500_stocks.csv` containing the stock tickers.

## Usage
1. **Run the Script**:
    ```sh
    python Algo_1.py
    ```
2. **Enter Portfolio Size**:
    - When prompted, enter the value of your portfolio.
3. **Output**:
    - The script will generate an Excel file named `recommended_trades.xlsx` containing the recommended trades.

## Script Details
1. **Importing Stock Data**:
    - Reads stock data from `sp_500_stocks.csv`.
2. **Acquiring API Token**:
    - Imports the API token from `secrets.py`.
3. **Fetching Stock Data**:
    - Retrieves stock data for each symbol from the IEX Cloud API.
4. **Creating Pandas DataFrame**:
    - Constructs a DataFrame to store stock information.
5. **Batch API Calls**:
    - Makes batch API calls to get data for multiple stocks.
6. **Calculating Position Size**:
    - Calculates the number of shares to buy based on the portfolio size.
7. **Exporting Data to Excel**:
    - Writes the recommended trades to an Excel file.
8. **Formatting Excel File**:
    - Formats the Excel file with specific styles for better readability.

- This will generate an Excel file with the recommended trades based on a $100,000 portfolio.

## Notes
- Ensure the `sp_500_stocks.csv` file and `secrets.py` file are in the same directory as the script.
- The script uses the IEX Cloud sandbox environment for API calls. For production use, replace the sandbox URL with the live URL.

## License
This project is licensed under the MIT License.
