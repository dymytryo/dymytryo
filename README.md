### Hi there 👋

Portfolio: [https://dymytryo.github.io/](https://dymytryo.github.io/)
  
<h2>👨‍💻 My Projects:</h2>

<h3>Snowflake to Starburst and Iceberg Acquisition Integration</h3>

- Objective: support BILL's acquisition of Divvy by moving acquired data workflows from Snowflake to BILL's Starburst/Trino and Apache Iceberg lakehouse under Sarbanes-Oxley (SOX) controls, with object-level parity validation and a coordinated Tableau cutover;
- Impact: addressed a ~$450/day (~$165K/year) Snowflake run rate, validated ~950 objects, reached ~80% migration progress at the documented checkpoint, and remediated ~3x Iceberg storage amplification;
- Link: [Snowflake integration case study](https://dymytryo.github.io/case-studies/snowflake-starburst-migration.html), [data_warehouse/snowflake](https://github.com/dymytryo/data_warehouse/tree/main/snowflake)
- Company Domain: Data Platform (acquisition integration)
- Tools: `Snowflake`, `Starburst`/`Trino`, `Apache Iceberg`, `dbt`, `Airflow`, `Fivetran`, `Tableau`
- Languages: `SQL`, `Python`

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

<h3>North Star Metric for Merchant Retention Rate</h3>

- Objective: measure 3-month cohort retention of merchants and transaction volume for a virtual card program, separating activity retention from enrollment retention;
- Link: [merchant retention case study](https://dymytryo.github.io/case-studies/merchant-retention.html), [merchant_retention notebook](https://github.com/dymytryo/notebooks/tree/main/merchant_retention)
- Company Domain: Product & Strategy  
- Tools: `DuckDB`, `dbt`-style marts, `Jupyter Notebook` (originally `Athena` + `QuickSight`)
- Languages: `SQL`, `Python`

<h3>Month-End Close ETL</h3>

- Objective: automate the day-1 morning of monthly financial close: a business-day-aware Airflow DAG orchestrating config-driven AWS Glue jobs for monthly report tables, processor virtual-card revenue normalization, and NetSuite journal-entry CSV generation with KMS-encrypted S3 outbound;
- Link: [month-end-close-etl project](https://github.com/dymytryo/finance-analytics/tree/main/projects/month-end-close-etl)
- Company Domain: Finance & Accounting  
- Tools: `AWS Glue`, `Airflow`, `Athena`/`Starburst`, `NetSuite`, `S3` + `KMS`
- Languages: `Python`, `SQL`

<h3>Forecasting Daily Settled TPV with an LSTM</h3>

- Objective: forecast next-day settled TPV for the virtual card program with an LSTM, benchmarked against persistence, seasonal naive, and a linear model on identical inputs, with a 10-seed stability study, feature ablation, and refit-cadence experiment;
- Link: [TPV LSTM case study](https://dymytryo.github.io/case-studies/tpv-lstm-forecasting.html), [tpv_lstm_forecasting notebook](https://github.com/dymytryo/notebooks/tree/main/tpv_lstm_forecasting)
- Company Domain: Treasury & Settlement Operations  
- Tools: `Keras 3` (`JAX` backend), `pandas`, `scikit-learn`, `Jupyter Notebook`
- Languages: `Python`

<h3>Customer Lifetime Value for a Virtual Card Program</h3>

- Objective: price the check-to-virtual-card conversion program: survival curves for time on the rail, CLV by four methods, per-channel conversion spend ceilings, and an RFM regression for next-month revenue;
- Link: [virtual card CLV case study](https://dymytryo.github.io/case-studies/virtual-card-clv.html), [virtual_card_clv notebook](https://github.com/dymytryo/notebooks/tree/main/virtual_card_clv)
- Company Domain: Product & Strategy  
- Tools: `pandas`, `scikit-learn`, `statsmodels`, `seaborn`, `Jupyter Notebook`
- Languages: `Python`


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
<h3> Dockerized Analytics Engineering Runtime </h3>

Repository: [docker](https://github.com/dymytryo/docker)

Local `Airflow` + `dbt` runtime in `Docker`: an orchestration image and a slim dbt CI image, a `Postgres` warehouse target, and a five-task dbt release pipeline (deps, seed, run, test, artifact validation) built on a small DAG factory. Includes a step-by-step [DAG factory walkthrough](https://github.com/dymytryo/docker/blob/main/docs/dag-factory.md): shared scheduling policy, defaults, and override patterns.

---
<h2>👨‍💻 Coding Examples:</h2>

- [Jupyter Notebooks](https://github.com/dymytryo/notebooks) -> notebooks that include tutorials
- [Python snippets](https://github.com/dymytryo/python_snippets) -> useful functions for working with data
- [SQL snippets](https://github.com/dymytryo/sql_snippets) -> generic yet useful SQL tips and tricks
