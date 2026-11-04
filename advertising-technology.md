---
title: Programmatic Advertising Analysis
---

[← Back to homepage](./)


Analyzed 20,749 synthetic advertising records using BigQuery
and SQL to examine campaign spending, engagement, conversion
performance and viewability.

The project covers dataset generation, data preparation,
KPI calculations and comparative analysis. A six-page
Looker Studio report presents the findings.

**Tools:** BigQuery, SQL, Looker Studio and Python  
**Data:** Synthetic programmatic advertising records for 2023

## Business Questions

The analysis explores questions a media or business
intelligence team might investigate:

- How does campaign spending change throughout the year?
- How do advertising formats compare on cost and performance?
- Which advertiser categories have lower acquisition costs?
- How does viewability vary across devices?
- How can cumulative spending and performance rankings
  support budget reviews?

The dataset is synthetic. Findings describe this simulated
environment and should not be treated as evidence of
real advertising market behavior.

## Dataset

The dataset contains 20,749 records covering January
through December 2023, with four advertising formats,
four device types, twelve advertiser categories and
twenty-one publisher networks.

Fields include:

- Campaign month, advertising format and device type
- Advertiser category, publisher network and bid type
- Spend, impressions, clicks and conversions
- Viewability, video starts and video completions

Python was used to generate the dataset, which was
stored and analyzed in BigQuery.

## Data Preparation and SQL Analysis

SQL was used to prepare the data for reporting, calculate
performance metrics and compare results across campaign
segments.

### Date Preparation

Created a DATE field so monthly results could be sorted
chronologically in Looker Studio.

### Aggregation and KPI Calculations

Grouped campaign records by month, format, advertiser
category and device to examine:

- Total spend, impressions, clicks and conversions
- Cost per thousand impressions (CPM)
- Click-through rate (CTR)
- Cost per click (CPC)
- Cost per conversion
- Conversion rate
- Video completion rate

### Common Table Expressions and Window Functions

Used a common table expression to organize monthly spend
by format and a window calculation to track cumulative
spending across the year.

Used `RANK()` partitioned by advertising format to compare
advertiser categories within each format.

These queries support budget pacing reviews and help
identify segments for further investigation.

## Selected Findings

### Spending Increased Toward Year-End

Annual spending totaled approximately $35.5 million,
with 3.48 billion impressions and 4.86 million clicks.

November spending reached approximately $4.6 million,
compared with $1.6 million in January. This pattern
provides a basis for reviewing monthly budget allocation
and planning for periods of higher spending.

### Video Received the Largest Investment

Video accounted for approximately $15.3 million in spend,
followed by CTV at $10.0 million, native at $5.4 million
and display at $4.9 million.

Spending alone does not establish effectiveness. Comparing
cost, engagement and conversion metrics helps assess
whether investment aligns with campaign objectives.

### Advertising Costs Varied by Format

Reported CPM ranged from approximately $4.54 for display
to $25.83 for CTV.

The difference highlights the importance of evaluating
formats against their intended objectives, rather than
using a single cost metric to judge performance.

### Devices Showed Different Cost and Viewability Profiles

The report showed approximately 68% viewability for desktop
and 60% for mobile, alongside higher desktop CPM.

This comparison illustrates the trade-off between
placement cost and viewability. Further analysis would
be needed to determine whether the additional cost
produced better campaign outcomes.

## Looker Studio Report

The six-page report presents the SQL analysis through
charts, tables and written commentary.

### Overview

Introduces the project and reporting sections.

![Report overview](Adtech_Campaign_Performance_Dashboard_2023_page-1.jpg)

### Spend and Volume Trends

Examines monthly spending, impressions, clicks and
investment by advertising format.

![Spend and volume trends](Adtech_Campaign_Performance_Dashboard_2023_page-2.jpg)

### Format Performance

Compares spending and performance metrics across video,
CTV, native and display.

![Format performance](Adtech_Campaign_Performance_Dashboard_2023_page-3.jpg)

### Advertiser Category Analysis

Compares category spending and conversion-related metrics
to identify areas for further review.

![Advertiser category analysis](Adtech_Campaign_Performance_Dashboard_2023_page-4.jpg)

### Device and Viewability Analysis

Examines differences in viewability and advertising costs
across device types.

![Device and viewability analysis](Adtech_Campaign_Performance_Dashboard_2023_page-5.jpg)

### Cumulative Spend and Category Rankings

Presents the analysis developed using common table
expressions and window functions.

![Cumulative spend and category rankings](Adtech_Campaign_Performance_Dashboard_2023_page-6.jpg)

## Project Files

- [SQL queries](./queries.sql)
- [Synthetic dataset](./adtech_campaign_performance_2023.csv)
- [Full report PDF](./Adtech_Campaign_Performance_Dashboard_2023.pdf)

## My Contributions

- Generated the synthetic dataset using Python
- Stored and prepared the data in BigQuery
- Wrote SQL queries for aggregation and KPI calculations
- Used CTEs and window functions for cumulative analysis
  and category rankings
- Built the six-page Looker Studio report
- Wrote commentary connecting the results to business questions

## Skills Demonstrated

SQL querying, cloud-based data analysis, data preparation,
KPI development, comparative analysis, visualization
and business reporting.

---

**Sandra Igboanugo**  
[Connect on LinkedIn](https://www.linkedin.com/in/sandraigboanugo/)
