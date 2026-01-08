☕ Café Sales Data Analysis & Business Intelligence Dashboard

📌 Project Overview

This project transforms raw, "dirty" sales records from a local café into actionable business intelligence. Using Power BI and Power Query, I cleaned inconsistent data, engineered new time-series features, and built an interactive dashboard to uncover sales trends, product performance, and customer behavior patterns.

The goal was to move beyond simple reporting to provide strategic recommendations for inventory, staffing, and payment infrastructure.

📂 Files in this Repository:

Cafe_Sales_Insights.pbix - The complete Power BI project file (Data Cleaning + Dashboard).

README.md - Project documentation.

🛑 The Business Problem

The café struggled with messy transaction data that made it impossible to track performance accurately.

Data Quality Issues: Missing sales figures, inconsistent item names (e.g., "salad" vs "Salad"), and ambiguous date formats prevented analysis.

Operational Blind Spots: The management didn't know their peak sales hours, which items were actually driving revenue, or how customers preferred to pay.

Objective:
Clean the data to 100% validity and visualize key metrics to optimize staffing schedules, inventory planning, and operational investments.

🛠️ The Solution: Data Cleaning & Transformation

All data transformation was performed using Power Query to ensure reproducibility.

1. Data Cleaning Strategy (Deductive Imputation)

Instead of dropping rows with missing values (which would lose 10%+ of the data), I used a deductive imputation strategy:

Formula: Total Spent = Quantity × Price Per Unit

Execution: I calculated missing values for any column by leveraging the other two known variables, rescuing hundreds of transaction records.

2. Standardization & Quality Assurance

Text Cleaning: Applied Trim, Clean, and Proper Case to standardize categorical columns like Item and Location.

Date Handling: Converted inconsistent date formats and filtered out invalid time-stamps.

Validation: Achieved 100% Column Quality (0 errors, 0 empty values) before loading data into the model.

3. Feature Engineering

Time Intelligence: Created Transaction Month and Day of Week columns from the raw date field.

Sorting Logic: Created hidden numerical sort columns (Month Number, Day Number) to ensure chronological sorting in visualizations.

📊 Dashboard & Key Insights

The analysis revealed distinct patterns in customer behavior and sales volatility.

1. Sales Trends (Seasonality & Operations)

Monthly Volatility: Sales are highly seasonal. The annual trough is in May, while peaks occur in January and November, indicating a strong late-year "seasonal rush."

Daily Operations:

Peak Revenue Day: Thursday (Highest total sales volume).

Premium Customer Day: Tuesday (Highest Average Transaction Value - ATV of $9.35).

Action: Staffing should be maximized on Thursdays, while Tuesdays should be targeted for upselling premium items.

2. Product Performance

Top Revenue Driver: Salad is the #1 revenue-generating item.

Concentration: The top 3 items account for a disproportionate share of total revenue.

Action: Operational focus (inventory & quality control) must prioritize the Salad station to protect the primary revenue stream.

3. Customer Behavior (Payment & Location)

Digital Dominance: Digital Wallets are the preferred payment method (34.76%), overtaking Cash and Credit Cards.

Location Balance: Sales are evenly split between In-Store and Takeaway.

Action: Immediate investment in digital payment infrastructure is required to prevent transaction failures during peak times.

📝 Technical Challenges & Learnings

Market Basket Analysis (MBA) Limitation: I attempted to perform MBA to find product bundles. However, technical auditing revealed the dataset structure used single-item transactions (unique Transaction IDs for every item). This finding allowed me to pivot the analysis to Average Transaction Value (ATV) instead, providing a more relevant metric for this specific data structure.

Redundancy Management: I identified that Total Revenue and Transaction Volume were highly correlated. To provide deeper insight, I focused on ATV to segment high-value vs. high-volume days.

🔗 Data Source

Dataset: Cafe Sales - Dirty Data for Cleaning Training (Kaggle)

👤 Author

[Abdullah Tariq]

[[LinkedIn Profile Link](https://www.linkedin.com/in/syed-abdullah-tariq-ahmed-9a4a382ba/)]

