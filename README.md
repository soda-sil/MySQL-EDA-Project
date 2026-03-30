# 🔍 Exploratory Data Analysis in MySQL — Tech Layoffs Dataset

## 📌 Project Overview
This project performs Exploratory Data Analysis (EDA) on a cleaned dataset of tech industry layoffs using MySQL. This project was built on top of the Data Cleaning in MySQL project, using the cleaned layoffs_staging2 table as its starting point.

The goal was to explore the data freely, identify trends, patterns, and outliers, and extract meaningful business insights from the layoffs data.


## 📂 Dataset

- **Source:** Layoffs Dataset from AlexTheAnalyst
- **Rows:** ~2,361 records (after cleaning)
- **Columns:** company, location, industry, total_laid_off, percentage_laid_off, date, stage, country, funds_raised_millions
- **Time Period:** Tech layoffs from 2022–2023


## 🛠️ Tools Used

- **MySQL:** all analysis performed in SQL
- **MySQL Workbench:** query execution and results exploration


## 🔍 Key Questions Explored
1. **What was the largest single-day layoff?**

    - Queried the maximum total_laid_off in the dataset: identified a company that laid off 12,000 people in a single day.
   
1. **Which companies laid off 100% of their workforce?**

   - Filtered for percentage_laid_off = 1 and sorted by total employees and funds raised to understand the scale of these companies.
   
1. **Which companies had the most total layoffs overall?**
   
1. **How many people were laid off per year?**

1. **Which industries and countries were most affected?**
   
    - Grouped by industry and country to identify the hardest-hit sectors and regions.

1. **Rolling Monthly Total of Layoffs**
   
    - Used a CTE with a window function to calculate a cumulative rolling total of layoffs month by month. 

1. **Top 5 Companies with Most Layoffs Per Year**
   
    - Used nested CTEs and DENSE_RANK() to rank companies by layoffs within each year.


## 💡 Key SQL Concepts Demonstrated
- **Functions:** SUM(), MAX(), GROUP BY
- **Window Functions:** DENSE_RANK(), SUM() OVER()
- **CTEs:** Multi-step analysis with WITH clause
- **String Functions:** SUBSTRING() for date parsing
- **Filtering & Sorting:** WHERE, ORDER BY, HAVING

## 📁 Repository Structure
├── README.md

├── data/

│   └── layoffs.csv             # Raw dataset

└── sql/
    └── eda_analysis.sql        # Full EDA script

## 🔗 Related Project
This project uses data cleaned in: Data Cleaning in MySQL (Layoffs Dataset)

## 🚀 How to Reproduce

1. First complete the Data Cleaning project to generate the layoffs_staging2 table

1. Open sql/eda_analysis.sql in MySQL Workbench

1. Run queries individually or all at once to explore the results


## 👤 Author

### Sofia Costa

https://www.linkedin.com/in/sofiassvcosta/

https://github.com/soda-sil
