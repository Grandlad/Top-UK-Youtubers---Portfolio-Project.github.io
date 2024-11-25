# Data Porftolio

Welcome to my portfolio website :)! 

# Table of contents

- [Objective](#objective)
- [Data Source](#data-source)
- [Stages](#Stages)
- [Design](#design)
  - [Mockup](#mockup)
  - [Tools](#tools)
- [Development](#development)
  - [Pseudocode](#pseudocode)
  - [Data Exploration](#data-exploration)
  - [Data Cleaning](#data-cleaning)
  - [Transform the Data](#transform-the-data)
  - [Create the SQL View](#create-the-sql-view)
- [Testing](#testing)
  - [Data Quality Tests](#data-quality-tests)
- [Visualization](#visualization)
  - [Results](#results)
  - [DAX Measures](#dax-measures)
- [Analysis](#analysis)
  - [Findings](#findings)
  - [Validation](#validation)
  - [Discovery](#discovery)
- [Recommendations](#recommendations)
  - [Potential ROI](#potential-roi)
  - [Potential Courses of Actions](#potential-courses-of-actions)
- [Conclusion](#conclusion)
  - [Potential Courses of Actions](#potential-courses-of-actions)
- [Conclusion](#conclusion)

  
# Objective

  Head Marketing to decide who are the top YouTubers in 2024 and verify which ones would be best ones to run their marketing campaings through the next year.

  The solution will be to create a dashboard which will provide insights into YouTubers metrics, such as:
  - Total subscriber count,
  - Total views,
  - Total videos,
  - Engagement metrics.

This data will be helpful for marketing team to make informed decisions about further collaboration with the YouTubers.

# Data Source

Data has been sourced from Kaggle (an Excel extract: https://www.kaggle.com/datasets/bhavyadhingra00020/top-100-social-media-influencers-2024-countrywise?resource=download)

# Stages

- Design,
- Development,
- Testing,
- Analysis.

# Design

Data Visuals that can be helpful to determine client needs:

## Dashboard mockup

1. Table
2. Treemap
3. Scorecards
4. Horizontal bar chart

![Dashboard-Mockup](assets/images/dashboard_mockup.png)

## Tools

| Tool | Purpose |
| --- | ---|
| Excel | Exploring the data |
| SQL Server | Cleaning, testing, analyzing data |
| PowerBI | Visualizing the data via interactive dashboards |
| GitHub | Hosting the project documentation and version control |
| Mokkup AI | Designing the wireframe/mockup of the dashboard |

# Development 

More less approach from start to finish:

1. Get the Data
2. Explore the data in Excel
3. Lead the data into SQL Server
4. Clean the data with SQL
5. Test the data with SQL
6. Visualize the data in Power BI
7. Generate the fidings based on the insights
8. Write the documentation + commentary
9. Publish the data to GitHub pages

## Transform the data 

```sql
/*
# 1. Select the required columns
# 2. Extract the channel name from the 'NOMBRE' column
*/

-- 1.
SELECT
    SUBSTRING(NOMBRE, 1, CHARINDEX('@', NOMBRE) -1) AS channel_name,  -- 2.
    total_subscribers,
    total_views,
    total_videos

FROM
    top_uk_youtubers_2024
```

