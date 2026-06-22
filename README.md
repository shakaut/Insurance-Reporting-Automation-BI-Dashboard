# Insurance Reporting Automation & BI Dashboard

## Overview

This project automates the extraction, processing, and visualization of insurance operational data. It fetches data from PostgreSQL databases, 
generates weekly reports for multiple insurance document types, stores them in structured files, and provides an interactive Business Intelligence dashboard built with Streamlit.

<img width="1280" height="720" alt="New Project" src="https://github.com/user-attachments/assets/30964adc-0c34-4c86-bc70-b88c75595332" />

---------
## Features

- Automated execution of SQL queries and PL/pgSQL functions
- Weekly data extraction from PostgreSQL databases
- Support for 7 different report types
- Company-wise and week-wise reporting
- Separate tracking for Issued and Created records
- Automatic CSV generation and weekly appending
- Interactive Streamlit dashboard
- Historical trend analysis and KPI monitoring

## Architecture

```text
PostgreSQL Database
        │
        ▼
Python ETL Scripts
(psycopg2 + pandas)
        │
        ▼
Weekly CSV Repository
        │
        ▼
Streamlit BI Dashboard
        │
        ▼
Company-wise Analytics
```

## Reports Automated

### Life Insurance

- Policies
- Claims
- Original Receipts

### Non-Life Insurance

- Policies
- Cover Notes
- Money Receipts
- Addendum/Endorsements

Each report maintains:

- Issued Count
- Created Count
- Weekly Historical Data
- Company-wise Metrics

## Workflow

1. Execute SQL functions automatically.
2. Fetch data from PostgreSQL using Python.
3. Transform data using Pandas.
4. Append new weekly columns to existing CSV files.
5. Store historical datasets.
6. Visualize data through Streamlit dashboards.

## Tech Stack

| Technology | Purpose |
|-------------|---------|
| Python | Automation |
| PostgreSQL | Database |
| PL/pgSQL | Dynamic reporting functions |
| Pandas | Data processing |
| psycopg2 | Database connectivity |
| Streamlit | BI Dashboard |
| CSV Files | Historical data storage |

## Dashboard Features

- Company-wise analysis
- Week-wise trend visualization
- Issued vs Created comparison
- Interactive charts
- Historical performance tracking
- KPI monitoring

## Project Structure

```text
project/
│
├── scripts/
│   ├── life_policy.py
│   ├── life_claim.py
│   ├── life_or.py
│   ├── nonlife_policy.py
│   ├── nonlife_created.py
│   └── ...
│
├── data/
│   ├── life_policy_issued.csv
│   ├── life_policy_created.csv
│   ├── nonlife_policy_issued.csv
│   ├── nonlife_policy_created.csv
│   └── ...
│
├── dashboard/
│   └── app.py
│
└── README.md
```

## Key Achievements

- Automated 7 reporting pipelines.
- Eliminated manual report preparation.
- Created a reusable weekly ETL workflow.
- Built an interactive BI dashboard for operational monitoring.
- Enabled company-wise and week-wise analytics.

## Future Enhancements

- Scheduled execution using Windows Task Scheduler or Cron
- Export reports to Excel and PDF
- Email notifications
- Database-backed historical storage
- Advanced KPI dashboards
- Role-based authentication

## Author

**Shakhauat**

Python • PostgreSQL • Data Engineering • Streamlit • Business Intelligence
