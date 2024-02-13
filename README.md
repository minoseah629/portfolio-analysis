# Portfolio Analysis
## Introduction
This project is a data analytics project for a 401k portfolio.
## Data Source 
The data in example.csv has been sanitized.  
<img width="1270" alt="image" src="https://github.com/minoseah629/portfolio-analysis/assets/1980068/f4e441e4-9ffd-4c1e-b800-29cc66cb9c3c">
## Tools
Apache Spark via Pyspark and pandas, Python, jupyter notebook,matplotlib and delta tables
## Methodology
1. The jupyter notebook uses pyspark to read the example dataset.
2. pyspark has SQL capability to perform some data cleaning.
   + Few columns had $ which could not be processes so $ were removed.
   + Few columns had - and ( ) to indicate a negative amount or quality
   + Dates in dataset were assumed date on initial import of csv
3. Use SQL:
   + identify securities invested
   + identify total amount allocated
   + identify personal contributions (category - Employee pre-tax contributions)
   + identify employer contributions (category - Employer matching 401k contributions (fully vested))
   + identify portfolio fees
4. identify allocated contributions per category
   + use pandas to generate visualization of contribution percentages
   + calculated total contribution per category
5. calculate total quantity (shares) and total amount per security
6. Visualize security progress
7. Use API to gather current market price via Twelve Data API

## Limitations
1. As a github data analytics project, some analytics cannot be shared due to personal nature of data
   + Stuff to share
     1. Tracking personal portfolio strategy changes
     2. Tracking dividend income and fees
         *   percentage of dividend to total security shares held
         *   yearly fees can be calculated
