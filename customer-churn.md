---
title: Customer Churn Analysis with DAX and Power BI
---

[← Back to homepage](./)

# Customer Churn Analysis with DAX and Power BI

Analyzed 56,344 telecom customer records to explore how
churn varied across customer groups, contract types,
payment methods and service subscriptions.

The project involved preparing data with Power Query,
building a data model and creating calculated columns
and over 15 DAX measures. A Power BI dashboard brings
these calculations together for interactive exploration.

**Focus:** Data transformation, data modelling,
DAX calculations and customer segmentation.

## Business Questions

The analysis explored:

- What proportion of customers had churned?
- How did churn vary across contract and payment types?
- Which customer groups had higher churn rates?
- How did service subscriptions relate to churn?
- How could these patterns inform further retention analysis?

## Dataset

The dataset contains 56,344 telecom customer records,
including customer demographics, contract details,
monthly charges, service subscriptions and churn status.

Canadian city assignments used in the geographic
visualization were simulated. That view demonstrates
geographic filtering rather than actual regional
differences in telecom churn.

## Data Preparation with Power Query

Used Power Query to clean and transform the source data
before loading it into Power BI.

This stage prepared the fields needed for customer
segmentation, calculations and reporting.

## Data Modelling and Calculated Columns

Organized the data model to support comparisons across
customer characteristics and service subscriptions.

Created calculated columns to make the source fields
more useful for analysis:

- **Age Group:** Grouped customers into age bands.
- **Monthly Charge Group:** Grouped monthly charges
  into ranges for comparison.
- **Subscription flags:** Created fields such as
  `IsSubscribed` to support filtering and calculations.
- **Sort columns:** Created numeric sort orders for age
  and charge groups so categories appeared in a logical
  sequence across visuals.

These additions allowed the report to compare customer
segments without relying on individual ages or charge
amounts in every visual.

## DAX Measures

Created over 15 explicit measures to calculate customer
counts, churn rates and segment-level comparisons.

Unlike calculated columns, these measures respond to
the report's filter context, allowing the same calculation
to update as users select different customer groups.

### Customer Counts and Overall Churn

Measures for total customers, active customers and
churned customers provide the basis for the report.

Churn measures include:

- Churn Rate
- Churn Yes %
- Churn No %

### Contract and Demographic Comparisons

Created measures including:

- **MTM Churn Rate:** Churn among customers with
  month-to-month contracts.
- **Senior Churn Rate:** Churn within the customer
  segment defined as seniors.

These measures support comparisons between specific
segments and the overall customer population.

### Charges, Payment Methods and Services

Additional measures include:

- **Avg Monthly Charges (Churned)**
- **Churn Count by Payment Method**
- **Churned with Tech Support**

Together, these calculations support investigation
of how charges, payment arrangements and service
subscriptions relate to churn.

## Findings and Interpretation

### Overall Churn

The calculated churn rate was **26.54%**.

This provides a baseline for comparing customer segments.
A segment's churn count should be considered alongside
its customer population and churn rate.

### Contract Type

The analysis highlighted month-to-month contracts
as an area for closer retention review.

Contract comparisons help identify where further
investigation or targeted outreach may be useful.

### Payment Method

Customers using electronic checks showed higher churn
rates than customers using automated payment methods.

This is an observed association. Additional analysis
would be needed to determine whether payment method,
customer characteristics or other factors explain
the difference.

### Service Subscriptions

The analysis compared churn across standalone and
bundled service subscriptions.

These comparisons provide a starting point for
investigating whether particular service combinations
are associated with stronger customer retention.

## Dashboard Preview

The dashboard presents the model and DAX measures through
customer summaries, segment comparisons and filters.

![Customer churn dashboard](https://github.com/user-attachments/assets/469baa4b-36be-4d99-bbac-ab6dfb595be1)

### Customer Summary

KPI cards display total customers, active customers
and churned customers.

![Customer summary cards](https://github.com/user-attachments/assets/4a9a8ae3-7af2-4ddb-80ff-f4b6cf0f1465)

### Customer Segmentation

Visuals compare churn across demographic groups,
contract types and payment methods.

![Customer segmentation](https://github.com/user-attachments/assets/39957102-9428-4432-bbae-0e5dca1cec16)

![Additional customer comparisons](https://github.com/user-attachments/assets/a5688f57-5715-414d-b8ff-9262a87a892a)

![Churn comparisons across customer groups](https://github.com/user-attachments/assets/8042dd24-1185-4a67-89b0-3332ac900883)

### Service Comparisons

Service-level visuals allow users to compare churn
across subscription combinations.

![Service subscription comparisons](https://github.com/user-attachments/assets/6670d4a3-7040-406e-9369-827ea4551e3e)

### Interactive Filters

Filters allow users to explore monthly charge groups
and location. Location values are simulated.

![Dashboard filters](https://github.com/user-attachments/assets/889d77a9-7629-437f-90ae-ad9dfd7ec23b)

## How the Analysis Could Be Used

The report could support:

- Selecting customer segments for further retention research.
- Reviewing churn patterns across contract structures.
- Comparing payment methods and service subscriptions.
- Developing hypotheses for retention campaigns or testing.

The project identifies patterns and potential areas
for action. It does not demonstrate that a retention
intervention reduced churn.

## My Contributions

- Prepared and transformed data using Power Query.
- Developed the Power BI data model.
- Created customer segments and calculated columns.
- Built sort columns for consistent category ordering.
- Wrote over 15 DAX measures.
- Designed the dashboard and interactive filters.
- Interpreted findings in relation to retention questions.

## Tools

**Power Query:** Data preparation and transformation.  
**DAX:** Calculated columns, measures and segmentation logic.  
**Power BI:** Data modelling and interactive reporting.

---

[← Back to homepage](./) |
[Connect on LinkedIn](https://www.linkedin.com/in/sandraigboanugo/)
