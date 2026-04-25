# COVID-19 Data Analysis

## Aim
The aim of this experiment is to analyze COVID-19 data using Python and extract meaningful insights regarding the spread and impact of the virus across different countries and regions. The analysis includes data cleaning, transformation, aggregation, and visualization. Special focus is given to identifying trends over time, the most affected countries, and a detailed analysis of India at both country and state levels.

---

## Theory
COVID-19 data analysis is an application of data science techniques to understand patterns, trends, and relationships in pandemic-related datasets. The dataset used contains information such as confirmed cases, deaths, and recoveries across multiple countries and dates.

### 1. Data Collection and Loading
The dataset is loaded using the pandas library. If the dataset is not already present in the working directory, it is uploaded manually using Google Colab utilities.

### 2. Data Cleaning
Data cleaning ensures that the dataset is consistent and usable:
- Unnecessary columns like `SNo` and `Last Update` are removed.
- Data types are converted to appropriate formats:
  - `ObservationDate` is converted to datetime format.
  - `Confirmed`, `Deaths`, and `Recovered` are converted to integer types.

### 3. Feature Engineering
A new column called **Active Cases** is created using the formula:This represents the number of currently infected individuals.

### 4. Data Exploration
Basic exploration includes:
- Viewing the first few rows of the dataset.
- Checking data types and non-null values.
- Finding the latest available date in the dataset.

### 5. Data Aggregation
Grouping operations are performed to summarize the data:
- Country-wise aggregation of confirmed, deaths, recovered, and active cases.
- Date-wise aggregation to observe global trends.
- State-wise aggregation for India.

### 6. Visualization
Visualization is performed using Plotly:
- Choropleth maps display global distribution of confirmed and recovered cases.
- Color intensity helps compare severity across countries.

### 7. Country-Level Analysis
- Identification of total affected countries.
- Listing unique countries.
- Ranking countries based on confirmed cases.
- Extracting data for specific countries like India, US, and China.

### 8. India-Specific Analysis
- Filtering data for India.
- Identifying number of states/union territories.
- Handling missing state values.
- Determining the state with the highest confirmed cases.

---

## Commands Used

### Libraries Imported
- `pandas` → For data manipulation and analysis
- `numpy` → For numerical operations
- `os` → For file handling
- `google.colab.files` → For uploading files in Colab
- `plotly.express` → For data visualization

### File Handling Commands
- `os.path.exists()` → Check if file exists
- `files.upload()` → Upload dataset
- `os.rename()` → Move file to desired directory

### Data Loading and Viewing
- `pd.read_csv()` → Load CSV file
- `data.head()` → View first few rows
- `data.info()` → Get dataset summary

### Data Cleaning
- `data.drop()` → Remove columns
- `astype()` → Convert data types

### Feature Engineering
- Arithmetic operations to create new columns

### Data Selection and Filtering
- `data.iloc[]` → Select rows by index
- Conditional filtering using boolean expressions

### Aggregation and Grouping
- `groupby()` → Group data
- `sum()` → Aggregate values
- `reset_index()` → Reset index after grouping
- `value_counts()` → Count unique values
- `nunique()` → Count number of unique entries
- `unique()` → List unique values

### Sorting
- `sort_values()` → Sort data

### Handling Missing Values
- `fillna()` → Replace missing values

### Date Operations
- `max()` → Find latest date

### Visualization
- `px.choropleth()` → Create world map visualizations

---

## Conclusion
This experiment successfully demonstrates how to analyze real-world COVID-19 data using Python. The process involved data cleaning, transformation, and visualization to uncover meaningful insights.

Key conclusions:
- The pandemic affected a large number of countries globally with varying intensity.
- Certain countries had significantly higher confirmed and recovered cases.
- Visualization techniques such as choropleth maps help in understanding geographical distribution effectively.
- India-specific analysis revealed variations in case distribution across states.

Overall, this experiment highlights the importance of data analysis in understanding global health crises and supports informed decision-making through data-driven insights.
