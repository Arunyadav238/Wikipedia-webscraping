U.S. Largest Companies by Revenue Scraper (from Wikipedia)
This Python script scrapes data about the largest companies in the United States by revenue from a Wikipedia table and saves it as a CSV file.

Requirements:

Python 3.x
requests library (pip install requests)
beautifulsoup4 library (pip install beautifulsoup4)
pandas library (pip install pandas)
Instructions:

Install Libraries: Ensure you have the required libraries (requests, beautifulsoup4, and pandas) installed using pip install commands mentioned above.

Run the Script: Save the script as a Python file (e.g., companies_scraper.py) and execute it from the command line using python companies_scraper.py.

Output: The script will create a CSV file named "Companies.csv" in the same directory as the script, containing information about the largest U.S. companies, including the columns extracted from the Wikipedia table.

How it Works:

Imports: The script starts by importing necessary libraries:

requests for sending HTTP requests to websites.
beautifulsoup4 (imported as BeautifulSoup) for parsing HTML content.
pandas for creating and manipulating dataframes (used to store and save the scraped data).
Target URL: The script defines the URL of the Wikipedia page containing the list of largest U.S. companies by revenue.

Fetching and Parsing HTML:

It sends a GET request to the target URL using requests.get.
The response content (HTML) is parsed into a BeautifulSoup object for easier navigation.
Extracting Table Data:

The script assumes the data is presented in a table on the Wikipedia page. It finds the relevant table element and extracts:
Table headers (<th> tags): These are used as column names for the DataFrame.
Table data (<td> tags): These represent the actual company information for each row.
Creating and Populating DataFrame:

A pandas DataFrame is created with columns corresponding to the extracted table headers.
The script iterates through table rows (excluding the header row) and for each row:
Extracts data from each cell (<td>).
Appends the extracted data as a new row to the DataFrame.
Saving Data:

The final DataFrame containing company data is saved as a CSV file named "Companies.csv".
