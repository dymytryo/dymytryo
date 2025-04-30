### Hi there 👋
  
<h2>👨‍💻 My Projects:</h2>

<h3>Ops Workflow Automation & Reporting</h3>

- Objective: automate tasks using API calls for the Ops and generate reporting for the stakeholders;
- Link: [workflow_atomation](https://github.com/dymytryo/workflow_automation/blob/cddcfad27ab375e406d30f75822ef4296301e548/README.md)
- Company Domain: Operations
- Tools: `Google Sheets API`, `AWS`: `SageMaker`, `Athena`, `S3`, `Quicksight`, `Cloudwatch` 
- Languages: `Python`, `Presto SQL`</b>

<h3>North Star Metric for Merchant Retentation Rate</h3>

- Objective: track the changes in cohorts for the transaction volume generated and retained for a given payment product;
- Link: [retention_with_sql](https://github.com/dymytryo/retention_with_sql/blob/51aa94b897ba2d06196ad50989ece30167c657c8/README.md)
- Company Domain: Product & Strategy  
- Tools: `Athena`, `Quicksight`, `dbt`, `PyCharm`
- Languages: `Presto SQL`, `PostgreSQL`


<h3>Propensity to Get a Car Loan</h3>

- Objective: for the marketing outreach campaign predict the propensity of getting a car loan by a member;
- Link: [car_loan_propensity](https://github.com/dymytryo/car_loan_propensity/blob/c99d9025d97a8b575075d2a4fcd3573fd7784db0/README.md)
- Company Domain: Marketing  
- Tools: `Tableau`, `MS SQL Server`, `Jupyter Notebook`, `MS PowerPoint`
- Languages: `mySQL`, `Python`

<h3> Aiflow Projects </h3>

Repository: [Aiflow](https://github.com/dymytryo/airflow )

1. **Lake-to-DWH Cross-Notification Pipeline**  
   Dynamically generates staging DAGs in the Data Warehouse Airflow instance to run dbt models whenever upstream Lake tables are refreshed. Uses Airflow `Dataset` for cross-instance triggers.

2. **Payment Volume Pacing DAG**  
   Runs daily to project end-of-month payment volumes per method based on business-day pacing logic, writes results to Redshift, and powers a live Tableau dashboard for operational decision-making.

3. **Airflow DagRun Export DAG**  
   Exports recent `DagRun` metadata from the Airflow metastore into Redshift tables, enabling easy historical query and SLA monitoring beyond the limitations of Airflow’s native metastore.

4. **DBT Drop Redshift View or Table DAG**  
   A manual-triggered DAG that drops specified Redshift tables or views via runtime config, allowing analytics engineers to manage schema cleanup without needing direct console access.

<h2>👨‍💻 Coding Examples:</h2>

- [Jupyter Notebooks](https://github.com/dymytryo/notebooks) -> notebooks that include tutorials
- [Python snippets](https://github.com/dymytryo/python_snippets) -> useful functions for working with data
- [SQL snippets](https://github.com/dymytryo/sql_snippets) -> generic yet useful SQL tips and tricks
