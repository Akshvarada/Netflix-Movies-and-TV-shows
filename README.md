# Netflix-Movies-and-TV-shows
Built an interactive dashboard analyzing Netflix content trends by genre, type, country, and time. Used Power Query for data cleaning, DAX for custom calculations, and multi-page visuals for storytelling insights.

Allianz Disability Claims Analysis: Improving Profitability with Predictive Modeling and Customer Segmentation
This capstone project was developed to help Allianz Benelux SA address a critical business challenge: the growing mismatch between premiums collected and payouts for long-duration disability claims. Using a real-world dataset of 5,370 historical claims, our objective was to identify the underlying drivers of prolonged claims, forecast future risk, and segment policyholders into actionable customer groups to support more effective pricing and claim management strategies.

🔍 Business Problem
Allianz observed that a subset of disability claims was lasting significantly longer than anticipated, causing their loss ratio to increase and impacting profitability. The goal was to:

Predict claim duration using customer and policy features

Identify high-risk segments of claimants

Recommend prescriptive actions to mitigate financial exposure

🧹 Data Cleaning & Feature Engineering
The original dataset contained a mix of categorical and numeric data, including:

Demographics: Sex, Birth Year, District

Claim details: Claim Year, Claim Duration, Annuity

21 fields capturing disability severity over time (Pct_dis1 to Pct_dis21)

Key engineered features included:

Claim Severity: average of all 21 disability percentages

Age at Claim: Claim Year - Birth Year

Total Payouts: Annuity * Claim Duration

Customer Type: Single-claim vs. multiple-claim customer

This transformation enabled structured analysis and modeling while preserving business relevance.

📈 Exploratory Analysis
Customers aged 31–60 showed the highest volume of claims and financial exposure.

Only 8% of customers had multiple claims, but they accounted for over 20% of total payouts.

Claim Severity had a near-perfect correlation (r = 0.99) with claim duration, revealing it as a dominant predictor.

Age showed a moderate negative correlation (r = -0.29) — younger claimants tended to have longer disability durations.

🤖 Predictive Modeling
Two supervised learning models were developed using the caret package:

Linear Regression

R²: 0.9877

RMSE: 0.69

Findings:

Claim Severity: +21 months for every unit increase

Age at Claim: Negative effect on duration

Sex: Statistically insignificant

Use Case: Easily interpretable, suitable for audit and policy justification.

Random Forest Regression

R²: 0.9688

RMSE: 2.21

Findings:

Reinforced the importance of severity and age

Slightly less accurate but more robust to outliers

Use Case: Suitable for automation and real-time risk flagging

🔎 Customer Segmentation with K-Means Clustering
To develop a risk-based pricing strategy, I applied unsupervised learning to segment customers into clusters using:

Claim Severity

Claim Duration

Age at Claim

Sex (numeric encoding)

Number of claims filed

📌 Optimal clusters: 3 (determined via Elbow Method)

Cluster 1: Female, moderate severity (0.15), short duration (~3.5 years), low financial risk

Cluster 2: Younger, 82% male, high severity (0.75), longest duration (~16.2 years) — high-risk group

Cluster 3: Older males, low severity (0.13), shortest duration (~3.2 years), least risky

These segments enabled Allianz to align pricing with actual claim risk, avoiding undercharging high-risk customers and overcharging low-risk ones.

🧠 Prescriptive Analytics Tool
To operationalize the findings, I developed a lightweight, rule-based classification tool that predicts whether a new claim is high or low risk.
It uses four inputs:

Claim Duration

Age

Sex

Claim Severity

🚩 A claim is flagged as High-Risk if:

Duration > 10 years (75th percentile)

Claim Severity ≥ 0.7

Profile matches high-risk cluster (younger, male, severe)

✅ This tool is easily integrable into Allianz’s workflow for real-time triage, allowing early interventions and better reserve planning.

📊 Key Visuals Used
Figure 1: Correlation heatmap of predictors

Figure 2: Histogram of Claim Duration by Age Group

Figure 3: Random Forest feature importance plot

Figure 4: Elbow Method to determine optimal clusters

Figure 5–7: Payout trends, segment profiles, and age-based claim risks

✅ Impact & Business Value
This project created a full-cycle analytics solution, from data cleaning to predictive and prescriptive modeling. Allianz can now:

Predict long-duration claims accurately

Segment customers by risk and tailor premiums

Flag high-risk claims proactively for early action

Tools Used: R, ggplot2, caret, randomForest, factoextra, clustering, EDA
Total Titles

Count by type (Movies vs TV Shows)

Average number of seasons

Applied Top N filters, context-aware calculations, and aggregation logic across pages


 Dashboard Structure
The report is organized into multiple pages, each focused on a unique analytical lens:

Page 1: Content Overview
KPIs for total titles, total movies, and total shows

Donut chart comparing movie vs show percentages

Bar chart of the top 10 most frequent genres

Page 2: Movie Insights
Clustered bar chart of the top 10 movie directors

Release year trend line for movie count

Bar chart of the most common movie ratings (e.g., PG, R)

KPI card for the longest movie duration

World map visual showing the top countries producing movies

Page 3: TV Show Insights
Clustered bar chart of top countries by show count

KPI for the average number of seasons

Bar chart of the most frequent show genres

Release trend of shows over time

Page 4: Murder Mystery Titles
Filtered analysis of murder mystery-themed titles

KPI: total murder mystery content

Table showing titles, type, rating, and release year

Map of countries producing such content


 Impact & Outcome
This project highlights the ability to:

Transform semi-structured data into insightful, decision-ready visuals

Apply data storytelling principles to guide exploration

Communicate complex patterns (genre trends, content by country/type) clearly

It demonstrates strong proficiency in Power BI, DAX, and storytelling, making it a powerful addition to a data or business analytics portfolio.
