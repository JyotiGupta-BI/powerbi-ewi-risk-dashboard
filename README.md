📊 Project Overview
This Power BI dashboard analyzes a lending institution's customer risk profile using Early Warning Indicators (EWI). It consolidates customer-level data—spanning DPD, utilization, product type, income proof staleness, and region—to highlight operational and credit risks proactively.

📁 Dataset: Simulated customer-level lending data(150 records)
🛠 Tools Used: Power BI, DAX, Conditional Formatting, Bookmarks, Custom Tooltips
Data Fields: Customer ID, Region, Product, Balance, DPD, Utilization Ratio, Document Status, Risk Bucket

🎯 Key Metrics & KPIs
Metric	                     Value	              Description
Total Customers	              150	            Total number of borrowers
Total Loan Amount	           ₹150M	          Total loan disbursed
Outstanding Balance	         ₹110M	          Active exposure
Average DPD	                  30.9	          Indicates repayment behavior
High Risk %	                  12%	            Customers with both high DPD & high balances
High Utilization Accounts	    48	            Utilization ratio > 1.0
EAR (Exposure at Risk)	      ₹28M	          Exposure from high-risk accounts
EAR %	                        25%	            % of total exposure at risk

📈 Key Visual Insights
1. Risk Segmentation by DPD
   
🔸 Most customers are current or low-risk.
🔸 However, 39 customers (~26%) fall in the "High Risk" DPD category.

2. Region-wise High-Risk Accounts
   
🔸 North and South regions contribute the most to high-risk accounts.
🔸 South is a concern due to high DPD and high balance customers.

4. High Risk by Product & Region
   
🔸 Credit Card and Personal Loan segments show elevated high-risk clustering in North and West.
🔸 Home Loan (North) has the highest concentration of risk (marked red using diverging colors).

4. Average DPD Trend (2019–2023)
    
🔸 Peak DPD observed in 2021 (42), suggesting post-pandemic stress.
🔸 Steady improvement by 2023.

5. High Utilization % by Product
🔸 Auto Loan and Home Loan show the highest number of accounts with utilization ratio > 1.0.

6. Customer Score Distribution
🔸 Stacked bar of EWI Score Buckets by Region shows East and West have higher share of “High” risk customers.

7. Stale Documents (EWI-2)
🔸 19% of accounts have not updated income documentation recently—a non-monetary but regulatory risk.

8. Risk Performance by Region (Summary Matrix)
   
Region	    Avg DPD	     % High Risk	   Utilization %	    Total Customers
East	       30	           9.3%	           41.9%	               43
South	       30	           15.6%	         34.4%	               40
West	       33	           8.6%	           31.4%	               35
North	       32	           15.0%	         20.0%	               32

🧠 Insight: Though North has fewer customers, it shows high risk concentration and stale documentation concerns.

🧩 Advanced Customizations
🔘 Clear Filters Bookmark – resets all slicers with one click

🟨 Tooltip Page – dynamically shows key region-level insights like % stale docs, Avg DPD, Avg Loan Amt

📊 Conditional Formatting:

🔸 Diverging color scale in matrix (Green → Yellow → Red)
🔸 Risk bucket coloring in bar chart (low → high DPD)

📌 Calculated KPIs:

🔸 EAR = SUM(Balance) of high-risk accounts
🔸 EAR % = EAR / Total Exposure
🔸 High Risk % = SUM(EWI_1) / COUNT(Customer_ID)

📌 Additional Insights (Not Directly Shown)

🔸 1. EAR vs Customer Distribution Imbalance
While North has just 21% of total customers, it contributes to ~29% of EAR, indicating disproportionate risk exposure from a few high-ticket loans (especially in Home Loans).

🔸 2. DPD Trends Show Recovery After 2021
The spike in Average DPD in 2021 aligns with possible post-COVID repayment challenges. Since then, DPD has dropped by over 30%, suggesting improved collection efficiency or better underwriting.

🔸 3. Product-Level Risk Clustering
Credit Card segment shows high DPD across all regions → may need revised limits or stricter utilization controls.

Auto Loans have high utilization yet lower default levels — suggesting strategic retention value but careful monitoring.

🔸 4. Utilization Alert in East
The East region has highest utilization (41.9%), yet shows lowest high-risk % — suggesting possible early-stage stress.

May serve as a leading indicator needing proactive check-ins before DPD spikes.

🔸 5. Stale Documents – A Governance Risk
81% of customers have updated income docs — good compliance. But the remaining 19% pose an audit flag, especially if they overlap with high-risk or high-utilization segments.

