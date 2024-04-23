# IPL Data Analysis

This Jupyter Notebook provides a detailed analysis of the Indian Premier League (IPL) cricket tournament using Apache Spark on the Databricks platform.

## Features

### Data Ingestion
- The notebook reads multiple CSV files containing IPL match, player, and team data.
- Utilizes Spark DataFrames with defined schemas for data ingestion.
- Data is loaded from an S3 bucket into Spark DataFrames using `spark.read.schema()` and `format("csv")` methods.[1]

### Data Transformation
- Creates a new "high_impact" column in the "ball_by_ball_df" DataFrame to flag significant events.
- Adds new columns like "month", "day", "win_margin_category", and "toss_match_winner" for further analysis in the "match_df" DataFrame.[1]
- Temporary views are created for "ball_by_ball", "match", "player", "player_match", and "team" DataFrames for SQL-based querying.[1]

### Data Analysis
- Identifies top scoring batsmen per season through SQL queries joining relevant tables.
- Analyzes the impact of the toss on match outcomes using SQL queries on the "match" table.[1]

## Platform
The analysis was executed on the Databricks platform using Apache Spark, providing scalability and efficiency for large-scale datasets.
