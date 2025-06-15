# Netflix-Movies-and-TV-shows
Built an interactive dashboard analyzing Netflix content trends by genre, type, country, and time. Used Power Query for data cleaning, DAX for custom calculations, and multi-page visuals for storytelling insights.

Tool: Power BI | Domain: Media & Entertainment Analytics
Skills: Data Cleaning, Power Query, DAX, Data Modeling, Visualization, Storytelling

Overview
This project involved designing a comprehensive Power BI dashboard to explore and analyze Netflix’s global content library. Using a cleaned dataset of Netflix titles, the dashboard reveals key patterns and insights into how content is distributed across various categories, including type (movies vs. TV Shows), genre, country, director, and release year. The goal was to build a portfolio-ready project that demonstrates the end-to-end BI workflow — from raw data ingestion to interactive storytelling.

 

 Data Preparation
Imported the Netflix title dataset (.csv) into Power BI

Used Power Query to clean and transform the data:

Removed null values and duplicates

Parsed complex fields like duration into minutes or the number of seasons

Extracted first category from multi-genre fields (listed_in)

Created a binary field for "Murder Mystery?" content classification

Created relationships between the Netflix and Category Mapping tables


Modeling & DAXBuilt custom calculated columns using DAX:
Seasons Extracted number of seasons from “1 Season”, “3 Seasons”, etc.

Duration in MinsParsed movie durations from the duration column

Used DAX measures to calculate:

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
