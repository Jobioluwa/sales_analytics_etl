# Sales Analytics ETL Project

## Overview

This project demonstrates an ETL (Extract, Transform, Load) pipeline for sales data analysis. The pipeline extracts data from CSV files, transforms it by merging sales data with weather information, and loads it into a SQL database for analysis.

## Project Description

An end-to-end data pipeline that combines sales transaction data with weather conditions to analyze the impact of temperature on sales performance. The project showcases data engineering fundamentals including data extraction, transformation, merging datasets, and SQL database operations.

## Technologies Used

- **Python 3.13.7**
- **Pandas** - Data manipulation and analysis
- **SQLite/SQL** - Database storage and querying
- **Jupyter Notebook** - Interactive development environment

## Features

- ✅ CSV data extraction and loading
- ✅ Data cleaning and preprocessing
- ✅ Merging multiple datasets (sales + weather data)
- ✅ Handling data type mismatches (e.g., date column case sensitivity)
- ✅ SQL database integration
- ✅ SQL queries for data analysis
- ✅ Temperature-based sales analysis (Cold, Warm, Hot categories)

## Project Structure

```
sales_analytics_etl/
│
├── notebooks/
│ └── sales_analytics_etl.ipynb # Main analysis notebook
│
├── data/
│ ├── sales_data.csv # Sales transaction data
│ └── weather_data.csv # Weather information
│
├── database/
│ └── sales.db # SQLite database
│
└── README.md # Project documentation
```

## Dataset Information

### Sales Data

- Store_Id
- Store_Name
- Product_Category
- Date
- Unit_Sales
- Dollar_Sales
- Store_Zip
- Promotion_Flag
- Revenue_Per_Unit

### Weather Data

- date
- temp (temperature in Fahrenheit)

## Key Learnings

### 1. Data Merging Challenges

- Resolved column name case sensitivity issues (Date vs date)
- Used `left_on` and `right_on` parameters for merging datasets with different column names
- Removed duplicate columns after merge

### 2. SQL Integration

- Loaded pandas DataFrames into SQL database
- Performed SQL queries directly from Jupyter notebooks using `pd.read_sql()`
- Created temperature-based filters for data analysis


## How to Run

1. **Clone the repository**

```bash
git clone https://github.com/Jobioluwa/sales_analytics_etl.git
cd sales_analytics_etl
```

1. **Launch Jupyter Notebook**

```bash
jupyter notebook
```

1. **Open the notebook**
Navigate to `sales_analytics_etl.ipynb` and run all cells
1. **Query the database**
Use the SQL queries provided in the notebook to analyze the data

## Challenges Overcome

1. **KeyError during merge**: Resolved by identifying column name case differences between DataFrames
1. **Duplicate columns**: Fixed by using proper merge parameters or dropping redundant columns
1. **MergeError**: Solved by ensuring data transformations execute in correct order
1. **Git setup**: Installed Git for version control and GitHub integration

## Future Enhancements

- [ ] Add more weather features (humidity, precipitation)
- [ ] Implement automated data pipeline
- [ ] Create data visualizations (matplotlib/seaborn)
- [ ] Add statistical analysis of temperature impact on sales
- [ ] Deploy as a web dashboard

## Author

**Jobioluwa**

- GitHub: [@Jobioluwa](https://github.com/Jobioluwa)
- Email: tyegunjobi@gmail.com

## License

This project is open source and available for educational purposes.

## Acknowledgments

- Thanks to the Python and pandas community for excellent documentation
- Inspired by real-world ETL pipeline challenges

-----

**Last Updated**: October 2025
