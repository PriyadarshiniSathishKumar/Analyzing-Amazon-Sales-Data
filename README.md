# Analyzing-Amazon-Sales-Data
This Python code analyzes a CSV file named "Amazon Sales data.csv", assumed to contain information about Amazon sales transactions. Here's a breakdown of the steps:

# Import Libraries:

pandas: Used for data manipulation and analysis.
numpy: Used for numerical operations.
matplotlib.pyplot: Used for creating basic plots.
seaborn: A library built on top of matplotlib for creating more visually appealing statistical graphics.

# Data Loading and Cleaning:

Reads the CSV data using pd.read_csv.
Handles potential encoding issues with encoding='latin-1'.
Prints the first few rows of data using data.head().
Shows column names using data.columns.
Gets information about the data (data types, missing values) using data.info().

# Data Preprocessing:

Converts the 'Order Date' and 'Ship Date' columns to datetime format using pd.to_datetime for time-based analysis.
Converts categorical columns like 'Region', 'Country', 'Item Type', 'Sales Channel', and 'Order Priority' to string data types using astype(str) for consistency.

# Descriptive Statistics:

Creates a summary of descriptive statistics for numerical columns (Units Sold, Unit Price, Unit Cost, Total Revenue, Total Cost, Total Profit) using .describe().

# Missing Values:

Checks for missing values in the data using df.isnull().sum().
Sets the maximum number of rows to display in the output using pd.set_option('display.max_rows', None). This ensures all data is shown if there are many rows.

# Top 20 Countries by Sales:

Counts the frequency of occurrences in the 'Country' column using .value_counts().
Creates a pie chart using matplotlib.pyplot to visualize the top 20 countries with the highest sales volume.

# Box Plots for Key Metrics:

Creates box plots using seaborn.boxplot to explore the distribution of Total Profit, Total Cost, Total Revenue, Unit Cost, and Unit Price.
Box plots reveal potential outliers, central tendency (median), and spread of the data.

# Outlier Detection:

Defines a function detect_outliers that identifies outliers based on a threshold of 2 or 3 standard deviations from the mean.
Applies the function to each of the key metrics (Total Profit, Total Cost, Total Revenue) to find and print outlier data points.

# Total Revenue by Month:

Creates a bar chart using plt.bar to visualize the total revenue for each month (assuming 'Order Month' is a column indicating the month of the order).
Sets chart title and axis labels for clarity.

# Total Profit by Year:

Groups data by 'Order Year' and calculates the average Total Profit for each year using df.groupby('Order Year')['Total Profit'].mean().
Creates a line graph using .plot() to visualize the trend of total profit over time.

# Revenue and Profit by Item Type:

Groups data by 'Item Type' and calculates the total revenue and total profit for each category using .groupby('Item Type')['Total Revenue'].sum() and .groupby('Item Type')['Total Profit'].sum().
Sorts the results in descending order to identify the item types with the highest revenue and profit.

# Correlation Matrix:

Calculates the correlation coefficients between 'Total Revenue', 'Total Cost', and 'Total Profit' using .corr().
Correlation indicates the strength and direction of the linear relationship between these variables.

This code provides a comprehensive analysis of the Amazon sales data, allowing for insights into sales performance, profit margins, and product category trends.

# Colab Link
https://colab.research.google.com/drive/1TVYHtzTfbitywGwRr2L6cZgjKigSykxs?usp=sharing

![image](https://github.com/user-attachments/assets/34ba65c6-4383-4c46-b524-9b54d006bf28)

![image](https://github.com/user-attachments/assets/04cd4e32-9c12-46d0-8773-db0602456d62)

![image](https://github.com/user-attachments/assets/b4e59bb6-0699-42d3-9966-6d6429b4cd5d)

![image](https://github.com/user-attachments/assets/77c889a2-c4f1-466c-aed4-ec879c3903b0)

![image](https://github.com/user-attachments/assets/5dfcf234-7673-4fc6-bbdb-0b0e8ea99d92)













