# customer-segmentation-and-retail-analysis
🧠 Customer Segmentation Analysis using Python + Power BI
This project performs Customer Segmentation Analysis using a retail transaction dataset from an online store. The goal is to understand customer purchasing behavior using RFM analysis and visualize insights through Power BI dashboards.

📂 Dataset Information
Source: online_retail_10_11.csv

Rows: ~500K+

Fields:

InvoiceNo – Unique ID of the transaction

StockCode – Product code

Description – Product description

Quantity – Number of products purchased

InvoiceDate – Date of purchase

UnitPrice – Price per item

CustomerID – Unique customer ID

Country – Customer’s country

🧪 Exploratory Data Analysis (Python)
✔️ Steps Performed:
Imported required libraries:

python
Copy
Edit
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
Loaded the dataset:

Handled encoding issues using utf-8-sig.

python
Copy
Edit
df = pd.read_csv("online_retail_10_11.csv", encoding="utf-8-sig", on_bad_lines='skip')
Cleaned the data:

Removed null values (especially CustomerID)

Removed negative or zero Quantity and UnitPrice

Removed cancelled orders (InvoiceNo starts with 'C')

Feature Engineering:

Calculated TotalPrice = Quantity * UnitPrice

Converted InvoiceDate to datetime

Extracted Month from InvoiceDate

RFM Segmentation:

Recency: Days since last purchase

Frequency: Number of transactions

Monetary: Total amount spent

Used quantile-based scoring to assign segments (0 to 3)

📊 Power BI Dashboard

Key Metrics:
Total Customers: 4,338

Total Revenue: ₹9M

Average Order Value: ₹480.87

Average Recency: 92.54 days

Key Visuals:
📌 Customer Distribution by Segment

💸 Revenue by Segment

📅 Monthly Sales by Segment

👑 Top 10 Customers by Revenue

📈 Average RFM Matrix

💰 Monthly Unit Price Comparison

🎯 Business Insights
Segment 3 contributes the most revenue and holds ~70% of customers.

Top 10 customers generate disproportionately high revenue.

Seasonal trends show a sales spike around month 11 (likely holiday season).

Segmenting customers helps target high-value customers with loyalty programs.

🛠 Tools Used
Tool	Purpose
Python (pandas, numpy)	Data wrangling and EDA
Power BI	Dashboard and visualization
Jupyter Notebook	Prototyping and analysis
GitHub	Version control and sharing

✅ Conclusion
This project demonstrates a complete end-to-end customer analytics pipeline, from raw data cleaning and RFM segmentation in Python to professional dashboarding in Power BI. It offers real business value by helping companies better understand customer segments and behavior.
![Screenshot 2025-06-01 124550](https://github.com/user-attachments/assets/150d6b81-774e-4c71-9f68-cbfeb25d0b2a)

