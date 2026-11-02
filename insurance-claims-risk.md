---
title: "Insurance Operations and Risk Analysis"
---

[Back to home](./)

# Insurance Operations and Risk Analysis

Analyzed 40,000 synthetic records across policies, claims,
agents and support requests to investigate operational
performance, financial exposure and data quality.

**Tools:** Python, Pandas, Matplotlib, Seaborn,
scikit-learn and Jupyter Notebook.

**Project type:** Independent portfolio project using
synthetic data, not client or employer records.

## Business Question

How can insurance operational data help identify policies
requiring renewal attention, high-value claims and support
backlogs?

The analysis also explored whether the available claim
attributes could predict approval outcomes.

## Data and Approach

The dataset contains four related tables, each with
10,000 records, covering six Canadian provinces and
the period 2021–2025.

I checked for duplicates, missing values and valid
relationships between tables before calculating operational
metrics. The analysis covered:

- Claims volume, value, status and resolution time.
- Policy status, premiums and upcoming expirations.
- Support request volumes, resolution rates and priorities.
- Cross-table reconciliation and data quality.
- Claim approval classification using logistic regression.

## Key Findings

| Area | Finding |
| --- | --- |
| Policy renewals | 490 policies were approaching expiry within the analysis's 90-day window, representing approximately $2.05 million in premiums. |
| Claims exposure | 3,288 claims exceeded $50,000 and were flagged for further review. |
| Support backlog | 7,472 requests were unresolved, including 1,933 marked critical. |
| Resolution performance | Critical requests averaged 15.9 days to resolve, compared with 14.5 days for high-priority requests. |
| Data quality | No duplicate records were found, and all tested relationships between tables were valid. |

These findings describe the synthetic dataset. The premium
figure represents potential exposure associated with
upcoming expirations, rather than confirmed revenue loss.

## Operational Reporting

I created a six-panel dashboard covering regional claims
volume, claim types, policy status, support resolution
rates and trends over time.

![Insurance operational reporting dashboard](https://raw.githubusercontent.com/sandrai05/insurance-operational-reporting/main/operational_dashboard.png)

The dashboard brings the main operational measures together
so readers can compare performance and identify areas
requiring further investigation.

## Claims Classification

I tested whether claim type, region, claim amount and
resolution time could predict approval outcomes.

The modelling sample included 5,956 claims with a decided
status. A logistic regression model initially predicted
the majority class for every case. Applying balanced class
weights improved identification of denied claims, but
overall test accuracy was only 51.8%.

The result showed limited predictive value in the tested
features. Because the data are synthetic, this finding
does not explain how real insurers make approval decisions.

## Recommendations

The analysis suggested several areas for operational review:

- Prioritize renewal outreach using upcoming expiry dates
  and associated premiums.
- Route high-value claims for appropriate review.
- Investigate the unresolved critical-request backlog.
- Review triage practices where critical requests take
  longer to resolve than high-priority requests.

These are proposed actions based on the analysis,
not implemented changes or measured business outcomes.

## Full Project

The repository contains the complete notebook, synthetic
datasets, additional charts and executive summary.

[View the full project on GitHub](https://github.com/sandrai05/insurance-operational-reporting)

[Back to home](./)
