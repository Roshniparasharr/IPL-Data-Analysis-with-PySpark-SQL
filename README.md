
# 🏏 IPL Data Analysis with PySpark & SQL

This project performs an end-to-end exploratory data analysis (EDA) of Indian Premier League (IPL) datasets using **PySpark**, **Spark SQL**, and **Python**. It utilizes big data tools and techniques to uncover meaningful insights from ball-by-ball and match-level data hosted on **Amazon S3**, processed on **Databricks**.

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

Great! Since you're using **five datasets** instead of just two, and they’re all from your custom S3 path (`s3://ipl-data-analysis-project/`), here's the corrected and updated `## 📂 Datasets Used` section for your `README.md`:

---

## 📂 Datasets Used

All datasets were sourced from a public Amazon S3 bucket: `s3://ipl-data-analysis-project/`  
Each dataset is read into Spark using predefined schemas for efficient processing.

| Dataset Name        | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| `Ball_By_Ball.csv`  | Ball-by-ball event-level data including runs, wickets, batsmen, and bowlers |
| `Match.csv`         | Match-level information like toss results, match winners, venues, etc.      |
| `Player.csv`        | Player metadata including names and roles                                   |
| `Player_match.csv`  | Mapping of players to matches (who played in which match)                   |
| `Team.csv`          | Team metadata including team names and abbreviations                        |

These datasets form the backbone of the analysis and were transformed into Spark DataFrames with custom schemas.

---

##  Data Processing & Transformation

- Loaded S3 CSV data using Spark
- Casted data types (e.g., run values to Integer)
- Created temporary views for SQL queries
- Joined `matches` and `deliveries` on `match_id` for combined insights

---

## 📊 Key Insights Extracted

✅ Most Player of the Match awards  
✅ Matches played per season  
✅ Most matches played by team  
✅ Toss decisions & toss-winning impact  
✅ Top run scorers and wicket takers  
✅ Total sixes/fours by player  
✅ Matches won by team per season  
✅ Venue-based win distribution  
✅ Match outcome by toss decision

---

## 📈 Visualizations

The project includes several bar charts and line plots built using **Matplotlib** and **Seaborn**, showcasing trends and comparisons such as:

- Season-wise match count  
- Player performance (runs, wickets, boundaries)  
- Team wins & toss decisions  
- Venue-based win patterns

---

## 📁 Folder Structure

```bash
.
├── IPL_Data_Analysis_PySpark.ipynb   # Main analysis notebook
├── README.md                         # Project documentation
├── assets/                           # (Optional) Visuals or output charts
```
