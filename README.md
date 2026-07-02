# Loading and Exploring the Dataset

Loading raw data into the working environment is the first step before performing data analysis, preprocessing, or machine learning model development. The dataset is loaded using the Pandas library and converted into a DataFrame for efficient manipulation.

## Data Loading Functions (Pandas)

The following Pandas functions are commonly used to load different file formats:

- **CSV:** `read_csv()` – Loads data from CSV files.
- **Excel:** `read_excel()` – Loads data from Excel spreadsheets.
- **JSON:** `read_json()` – Loads JSON formatted data.
- **Text:** `read_table()` or `read_csv()` with a custom separator.

**Result:**  
The dataset is converted into a two-dimensional **Pandas DataFrame**, making it easier to analyze and manipulate.

## Data Exploration Functions

The following functions help in understanding the dataset:

### `head()`
Displays the first few rows of the dataset to verify that the data has been loaded correctly.

### `shape`
Returns the total number of rows and columns in the dataset.

### `info()`
Displays:
- Column names
- Data types
- Number of non-null values
- Memory usage

### `describe()`
Generates descriptive statistics including:
- Mean
- Standard Deviation
- Minimum Value
- Maximum Value
- Quartiles (25%, 50%, 75%)

## Workflow Impact

Proper data loading and exploration:

- Prevents file path and format errors.
- Helps understand the dataset structure.
- Identifies missing values and incorrect data types.
- Prepares the dataset for visualization, preprocessing, and machine learning model development.
