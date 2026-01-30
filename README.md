# 🚗 Automotive Sales Analytics

Exploratory data analysis of 100,000 automotive sales transactions, uncovering customer behavior patterns, geographic trends, and product performance insights.

Show Image
Show Image
Show Image

📊 Project Overview
Objective: Analyze automotive sales data to identify key drivers of revenue, customer segmentation opportunities, and geographic market performance.
Dataset: 100,000 sales transactions with 20 features including:

Customer demographics & location
Order details (quantity, price, date)
Product categories (Classic Cars, Motorcycles, Planes, etc.)
Sales performance metrics


🔍 Key Findings
Sales Performance

Average Transaction Value: $3,553
Price Range: $199 - $193,348
Average Order Size: 35 items

Customer Behavior

Days Since Last Order: Recalculated from order date for accurate customer recency analysis
Geographic Distribution: Sales concentrated in specific regions (analysis included)

Data Quality

100% Complete: No missing values after cleaning
Data Cleaning: Removed 5 irrelevant columns (phone, address details)
Feature Engineering: Created DAYS_SINCE_LASTORDER metric for recency analysis


🛠️ Technical Approach
Data Cleaning
python# Removed non-analytical columns
dropped_cols = ['PHONE', 'ADDRESSLINE1', 'POSTALCODE', 
                'CONTACTLASTNAME', 'CONTACTFIRSTNAME']

# Datetime transformation
data['ORDERDATE'] = pd.to_datetime(data['ORDERDATE'])

# Recency calculation
new_date = datetime(2020, 6, 1) - data['ORDERDATE']
data['DAYS_SINCE_LASTORDER'] = new_date.dt.days
Exploratory Analysis

Numerical Features: 8 features (Sales, Quantity, Price, MSRP, etc.)
Categorical Features: 8 features (Product line, Customer, Country, etc.)
Statistical Summary: Descriptive statistics for all numerical variables

Visualization

Distribution plots for key metrics
Geographic sales analysis
Product category performance
Customer segmentation insights


📂 Project Structure
automotive-sales-analytics/
├── autocar_final.py       # Complete analysis script
├── data.csv               # Raw sales data (100K records)
└── README.md              # Project documentation

🚀 Quick Start
Requirements
bashpip install pandas numpy matplotlib seaborn
Run Analysis
bashpython autocar_final.py
Expected Output

Data cleaning summary
Statistical analysis tables
Visualizations (distributions, trends)
Business insights report


📈 Business Insights
Revenue Optimization

High-value transactions ($10K+) represent significant revenue opportunity
Average transaction value suggests premium product mix

Customer Segmentation

Recency analysis enables targeted re-engagement campaigns
Geographic concentration indicates market penetration opportunities

Product Strategy

Price range analysis ($26-$252 per item) shows diverse product portfolio
MSRP vs actual price analysis reveals pricing strategy effectiveness


🔬 Methodology

Data Loading: Import 100K sales records
Quality Assessment: Check dimensions, data types, missing values
Data Cleaning: Remove irrelevant columns, handle duplicates
Feature Engineering: Create recency metric for customer analysis
Statistical Analysis: Descriptive statistics for numerical features
Visualization: Generate plots for key metrics and trends
Insight Generation: Translate findings into business recommendations


🎯 Key Metrics
MetricValueInsightAvg Sales$3,553Strong transaction valueAvg Quantity35 itemsBulk ordering behaviorAvg Price$101/itemPremium product positioningData Quality100% completeHigh-quality dataset

🛠️ Tech Stack
Core Libraries:

pandas - Data manipulation and analysis
numpy - Numerical computations
matplotlib - Static visualizations
seaborn - Statistical data visualization

Analysis Techniques:

Descriptive statistics
Data cleaning & transformation
Feature engineering
Exploratory data visualization


📚 Lessons Learned
Data Quality

Duplicate entries required recalculation of time-based metrics
Proper datetime handling critical for temporal analysis

Feature Engineering

Created DAYS_SINCE_LASTORDER to replace inconsistent original metric
Improved data accuracy for customer recency analysis

Segmentation

246 unique recency values enable granular customer lifecycle analysis
Geographic and product category dimensions reveal market opportunities


👤 Author
Ahmet Baran Bozkurt
Data Science Student | Analytics Enthusiast

📄 License
This project is for educational and portfolio purposes.

Last Updated: January 2026
Status: Exploratory Analysis Complete
