# Big Data Analytics Lab

## Optimize Business Processes Using Big Data Analytics

### Student
Muhire Rutayisire

### Overview
This lab demonstrates how big data analytics can be applied to a retail transactions dataset using PySpark. The lab covers descriptive, diagnostic, and advanced analytics, along with feature engineering, customer segmentation, anomaly detection, and Parquet output for downstream data use. The objective is to show how data can support business decision-making and process improvement. :contentReference[oaicite:0]{index=0}

### Tools and Technologies
- Python 3
- PySpark
- Spark DataFrame API
- Window Functions
- Parquet

### Dataset
The dataset contains simulated retail transactions with fields such as customer name, region, category, unit price, quantity, timestamp, and payment method. A revenue column was created by multiplying unit price by quantity. :contentReference[oaicite:1]{index=1}

## Lab Tasks Completed

### 1. Data Preparation
A Spark session was created and the dataset was loaded into a PySpark DataFrame using a defined schema. The timestamp column was converted into timestamp format, and a new revenue column was added for analysis.

### 2. Descriptive Analytics
Descriptive analytics were used to summarize the dataset. Statistics such as count, mean, minimum, maximum, and standard deviation were generated for unit price, quantity, and revenue. Revenue totals were also calculated by category and by region to identify the strongest business areas.

### 3. Diagnostic Analytics
Diagnostic analytics were performed to better understand business trends. Monthly revenue totals were calculated to show revenue changes over time. A pivot table was also created to compare category performance across different regions.

### 4. Advanced Analytics with Window Functions
Window functions were used to perform more detailed analysis. A running total of customer revenue was calculated to track how customer spending changed over time. Transactions were also ranked by revenue within each region to highlight top-performing sales.

### 5. Feature Engineering and RFM Scoring
Additional analytical features were created from the timestamp column, including hour, day of week, month, and weekend flag. RFM analysis was then performed:
- **Recency** measured how recently a customer made a purchase
- **Frequency** measured how often the customer purchased
- **Monetary** measured total customer spending

These values were scored using `ntile()` to support customer segmentation.

### 6. Customer Segmentation
Customers were grouped into segments based on their RFM scores. The main segments used in this lab were:
- Champions
- At Risk
- Potential Loyalist

This helps identify valuable customers as well as customers who may need attention.

### 7. Anomaly Detection
Z-scores were calculated on transaction revenue to detect unusual transactions. Transactions with absolute z-scores greater than 2 were flagged as anomalies. This can help businesses identify unusually high-value purchases or possible outliers in transaction behavior. :contentReference[oaicite:2]{index=2}

### 8. Parquet Output
The engineered dataset was written to Parquet format in the `output/transactions_parquet` folder. This output can be used for future analysis or downstream data engineering tasks. :contentReference[oaicite:3]{index=3}

## Results Summary
The lab successfully showed how PySpark can be used to analyze retail transaction data from multiple perspectives. The workflow moved from basic summaries to more advanced business insights such as customer ranking, segmentation, and anomaly detection. The final dataset was also saved in Parquet format, which supports efficient storage and future processing.

## Conclusion
This lab provided practical experience with big data analytics using PySpark. It showed how data can be transformed into useful business insights through descriptive, diagnostic, predictive-style feature engineering, segmentation, and anomaly detection techniques. It also demonstrated how processed analytics data can be stored in Parquet format for scalable use in real-world data workflows.# big-data-lab
