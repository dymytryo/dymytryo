### Hi there 👋

Portfolio: [https://dymytryo.github.io/](https://dymytryo.github.io/)
  
<h2>👨‍💻 My Projects:</h2>

<h3>Data Platform Observability</h3>

- Objective: take an analytics warehouse of 4K+ dbt models with multiple IoT ingestions from no observability to full coverage, cutting data downtime by 45% — freshness SLAs from dbt sources, control-count reconciliation, metadata coverage, and transition-based alerting, graded daily into four live scorecards (tests, alerts, tables, users/stewards);
- Link: [data observability case study](https://dymytryo.github.io/case-studies/data-observability.html), [observability repo](https://github.com/dymytryo/observability)
- Company Domain: Data Platform
- Tools: `dbt`, `Snowflake`, `DuckDB`, `PagerDuty`/`Slack` alert routing
- Languages: `SQL`, `Python`, `YAML`

<h3>Google Sheets Ingestion & Change Capture</h3>

- Objective: self-serve ingestion of Google Sheets for analytics — typed reads of any sheet plus insert/update/delete change capture via snapshot diffing;
- Link: [gsheets_ingestion notebook](https://github.com/dymytryo/notebooks/tree/main/gsheets_ingestion)
- Company Domain: Operations
- Tools: `Google Sheets API`, `pandas`, `Parquet`, `dbt` hand-off
- Languages: `Python`

<h3>North Star Metric for Merchant Retentation Rate</h3>

- Objective: track the changes in cohorts for the transaction volume generated and retained for a given payment product;
- Link: [retention_with_sql](https://github.com/dymytryo/retention_with_sql/blob/51aa94b897ba2d06196ad50989ece30167c657c8/README.md)
- Company Domain: Product & Strategy  
- Tools: `Athena`, `Quicksight`, `dbt`, `PyCharm`
- Languages: `Presto SQL`, `PostgreSQL`


<h3>Propensity to Get a Car Loan</h3>

- Objective: for the marketing outreach campaign predict the propensity of getting a car loan by a member;
- Link: [vehicle loan propensity case study](https://dymytryo.github.io/case-studies/vehicle-loan-propensity.html)
- Company Domain: Marketing  
- Tools: `Tableau`, `MS SQL Server`, `Jupyter Notebook`, `MS PowerPoint`
- Languages: `mySQL`, `Python`

---
<h3> Aiflow Projects </h3>

Repository: [Aiflow](https://github.com/dymytryo/airflow )

1. **Lake-to-DWH Cross-Notification Pipeline**  
   Dynamically generates staging DAGs in the Data Warehouse `Airflow` instance to run dbt models whenever upstream Lake tables are refreshed. Uses Airflow `Dataset` for cross-instance triggers.

2. **Payment Volume Pacing DAG**  
   Runs daily to project end-of-month payment volumes per method based on business-day pacing logic, writes results to `Redshift`, and powers a live `Tableau` dashboard for operational decision-making.

3. **Airflow DagRun Export DAG**  
   Exports recent `DagRun` metadata from the `Airflow` metastore into `Redshift` tables, enabling easy historical query and SLA monitoring beyond the limitations of Airflow’s native metastore.

4. **DBT Drop Redshift View or Table DAG**  
   A manual-triggered DAG that drops specified `Redshift` tables or views via runtime config, allowing analytics engineers to manage schema cleanup without needing direct console access.
---
<h2>👨‍💻 Coding Examples:</h2>

- [Jupyter Notebooks](https://github.com/dymytryo/notebooks) -> notebooks that include tutorials
- [Python snippets](https://github.com/dymytryo/python_snippets) -> useful functions for working with data
- [SQL snippets](https://github.com/dymytryo/sql_snippets) -> generic yet useful SQL tips and tricks
