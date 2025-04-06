
# 🏏 IPL Data Analysis with PySpark & SQL

This project performs an end-to-end Exploratory Data Analysis (EDA) and builds a robust Spark-based ETL pipeline using **PySpark** and **SQL** to analyze IPL (Indian Premier League) cricket data. The goal is to extract meaningful insights from structured match and ball-by-ball datasets by applying Spark transformations, aggregations, window functions, and SQL queries at scale.

Built entirely on **Apache** **Spark** with **Databricks** Community Edition, this project reads data directly from Amazon S3, processes it using PySpark DataFrames, and visualizes key findings using Matplotlib and Seaborn.

---

##  Problem Statement

The goal of this project is to analyze large-scale IPL cricket data to extract actionable insights related to:

- Player performance
- Team strategies
- Match outcomes
- Toss and venue advantages
- Season-wise trends

Using the power of distributed computing via PySpark, this project processes and transforms raw cricket data to derive useful statistics and visualize them clearly.

---

##  Technologies & Tools Used

- **Language**: Python, SQL (Spark SQL)
- **Big Data Framework**: Apache Spark (PySpark)
- **Platform**: Databricks (Community Edition)
- **Storage**: Amazon S3 (Public IPL dataset)
- **Libraries**: Pandas, Matplotlib, Seaborn

---

Sure! Here's a clean and professional version of the section you shared:

---

## 📁 Datasets Used

All datasets were sourced from a public Amazon S3 bucket: `s3://ipl-data-analysis-project/`  
Each file was loaded into **Apache Spark** DataFrames using predefined schemas for optimized performance and structured querying.

- **Ball_By_Ball.csv** – Detailed ball-by-ball event data including runs scored, wickets taken, batsmen, and bowlers.  
- **Match.csv** – Match-level details such as toss results, winners, venue information, and season.  
- **Player.csv** – Player metadata including player names, IDs, and roles.  
- **Player_match.csv** – Mapping of players to matches indicating which player participated in which game.  
- **Team.csv** – Team-level metadata including team names, abbreviations, and IDs.

---

##  Data Processing & Transformation

- Loaded S3 CSV data using Spark
- Casted data types (e.g., run values to Integer)
- Created temporary views for SQL queries
- Joined `matches` and `deliveries` on `match_id` for combined insights

---

##  Key Insights Extracted

-✅ Top-scoring batsmen per season
-✅ Most economical bowlers in powerplay overs
-✅ Impact of toss decision on match outcome (win/loss)
-✅ Average runs scored by players in winning matches
-✅ Venue-wise average and highest total scores
-✅ Most common dismissal types
-✅ Team-wise performance after winning the toss

---

##  Visualizations

The project uses **Matplotlib** and **Seaborn** to build insightful visualizations that highlight key IPL trends and comparisons. These include:

-  **Top 10 Most Economical Bowlers** in Powerplay (Average Runs per Ball)  
-  **Impact of Toss Winner** on Match Outcome (Win/Loss Analysis)  
-  **Top 10 Batsmen by Average Runs** in Matches Their Team Won  
-  **Venue-wise Analysis** of Average and Highest Team Scores  
-  **Most Frequent Dismissal Types** (e.g., bowled, caught, etc.)  
-  **Team-wise Performance** After Winning the Toss

---

##  Folder Structure

```bash
.
├── IPL_Data_Analysis_PySpark.ipynb   # Main analysis notebook
├── README.md                         # Project documentation
├── assets/                           # (Optional) Visuals or output charts
```
