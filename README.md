                                                  ☕ Coffee Quality & Production Analysis Using SQL
#Project Title:-
Coffee Quality & Production Analysis Using SQL

## 1. Introduction

Coffee is one of the most popular beverages in the world, and maintaining high coffee quality is important for coffee businesses.
This project analyzes coffee quality and production data from different countries using SQL. The goal is to identify the best-performing countries, coffee varieties, and processing methods to support better business decisions.

---

## 2. Objective

The main objectives of this project are:

* Analyze coffee quality scores.
* Identify top-performing countries.
* Evaluate coffee varieties.
* Analyze processing methods.
* Study production volume trends.
* Generate useful business insights using SQL.

---

## 3. Dataset Description

The dataset contains 100 coffee records collected from different coffee-producing countries.

### Columns Included

* ID
* Country
* Variety
* Processing Method
* Bags
* Total Score

### Countries Included

* Brazil
* Ethiopia
* Colombia
* India
* Kenya

---

## 4. Database Design

A relational database was created using MySQL.

### Table Name

`coffee`

### Primary Key

`id`

### Table Structure

```sql
CREATE TABLE coffee(
id INT PRIMARY KEY,
country VARCHAR(50),
variety VARCHAR(50),
processing_method VARCHAR(50),
bags INT,
total_score DECIMAL(5,2)
);

#Overview:-
Coffee is one of the most traded agricultural products in the world.
Understanding coffee quality and production trends helps businesses improve sourcing decisions and identify high-performing coffee-producing regions. 
This project uses SQL to analyze coffee data from multiple countries and extract meaningful insights.

#Problem Statement:-

##Coffee companies need to identify:

Which countries produce the highest-quality coffee?
Which coffee varieties perform best?
Which processing methods lead to better quality scores?
How production volume varies across countries?
Which regions should be prioritized for sourcing?

This project answers these business questions using SQL.

Dataset
Dataset Information
Attribute	Description
Total Records	100
Countries	Brazil, Ethiopia, Colombia, India, Kenya
Data Type	Coffee Quality Dataset
Columns
ID
Country
Variety
Processing Method
Bags
Total Score
Tools and Technologies
MySQL
SQL
GitHub
Excel

#Methods:-
##SQL Concepts Used

* SELECT

* WHERE

* ORDER BY

* GROUP BY

* HAVING

* Aggregate Functions

* CASE Statements

*Subqueries

* Window Functions

* RANK()

*DENSE_RANK()

Key Insights
Country Analysis
Kenya achieved the highest average coffee quality score.
Ethiopia consistently produced premium-quality coffee.
Brazil led in total production volume.
Variety Analysis
SL28 variety received the highest quality scores.
Heirloom variety showed consistent performance.
Processing Method Analysis
Washed processing method generated the highest average score.
Honey and Natural methods performed competitively.
Business Insight
High-quality sourcing opportunities exist in Kenya and Ethiopia.
Production volume and quality are not always directly related.
Dashboard / Model / Output
Top Quality Countries
SELECT country,
AVG(total_score) avg_score
FROM coffee
GROUP BY country
ORDER BY avg_score DESC;
Best Processing Method
SELECT processing_method,
AVG(total_score) avg_score
FROM coffee
GROUP BY processing_method
ORDER BY avg_score DESC;
Country Ranking
SELECT country,
DENSE_RANK() OVER(
ORDER BY AVG(total_score) DESC
) ranking
FROM coffee
GROUP BY country;
Production Analysis
SELECT country,
SUM(bags) total_bags
FROM coffee
GROUP BY country
ORDER BY total_bags DESC;

##Outputs##
├── country_ranking.png
├── production_analysis.png
├── variety_analysis.png
├── processing_method_analysis.png
└── top_quality_samples.png


#Results & Conclusion:-

The analysis revealed that Kenya and Ethiopia are the strongest performers in coffee quality, while Brazil dominates coffee production volume. 
The Washed processing method consistently delivers better quality scores than other methods.
These findings can help coffee businesses improve sourcing strategies and focus on high-quality coffee-producing regions.

#Future Work:-
Create Power BI Dashboard
Develop Interactive Visualizations
Analyze Larger Datasets
Build Predictive Models
Perform Quality Forecasting
Add Regional-Level Analysis


##Author:-

Susheel kumar

B.Tech (Electronics & Communication Engineering)

Aspiring Data Analyst | SQL | Excel | Power BI | Python

