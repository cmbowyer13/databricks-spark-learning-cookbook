# Databricks Spark Learning Cookbook 

A hands-on PySpark and Databricks learning path covering Spark fundamentals, DataFrames, Spark SQL, Delta Lake, ETL patterns, data quality, performance basics, and practical analytics mini-projects.

This repository is designed as both a personal learning lab and a public portfolio project. The notebooks are written to be beginner-friendly, heavily commented, and runnable in **Databricks Free Edition**.

---

## Why I Built This

I created this repository to strengthen my Spark, PySpark, and Databricks skills through practical notebooks that move from fundamentals to applied analytics projects.

The goal is to build real fluency with Spark by practicing:

- Core PySpark DataFrame operations
- Spark SQL
- Joins and relational thinking
- Aggregations and window functions
- Reading and writing data
- Delta Lake tables
- Data quality checks
- ETL pipeline design
- Performance fundamentals
- Explain plan interpretation
- Practical analytics workflows

This repo is also meant to serve as a portfolio showing how I approach data engineering, analytics, and lakehouse-style problem solving.

---

## Designed for Databricks Free Edition

These notebooks are intended to run in **Databricks Free Edition**.

Databricks Free Edition is a no-cost Databricks environment for students, educators, hobbyists, and learners who want to experiment with data and AI tools. It provides a serverless, quota-limited workspace for learning, prototyping, building notebooks, and working with AI and machine learning tools. Databricks describes Free Edition as designed for learning, training, and other non-commercial purposes.  
See: [Databricks Free Edition](https://www.databricks.com/learn/free-edition) and [Databricks Free Edition documentation](https://docs.databricks.com/aws/en/getting-started/free-edition).

Most examples in this repo use:

- `spark.createDataFrame()`
- `spark.range()`
- small synthetic datasets
- Databricks `display()`
- Spark SQL temporary views
- Delta table writes using `.saveAsTable()`
- beginner-friendly notebook workflows

No external data downloads are required for the beginner notebooks.

---

## How to Sign Up for Databricks Free Edition

To run these notebooks in Databricks Free Edition:

1. Go to the official Databricks Free Edition page:  
   [https://www.databricks.com/learn/free-edition](https://www.databricks.com/learn/free-edition)

2. Click **Sign up for Free Edition**.

3. Create an account using a personal email address.

4. Complete the email verification process.

5. After logging in, open your Databricks workspace.

6. Create a new notebook or import one of the notebooks from this repository.

7. Attach the notebook to the default serverless compute environment if prompted.

8. Run the cells from top to bottom.

Databricks also provides a signup page here:  
[https://signup.databricks.com/](https://signup.databricks.com/)

Free Edition is different from the paid trial. The Databricks trial is aimed at business evaluation and can include usage credits, while Free Edition is intended for personal learning and skill development.

---

## Repository Structure

```text
databricks-spark-learning-cookbook/
│
├── README.md
├── roadmap.md
├── environment.md
├── LICENSE
├── .gitignore
│
├── notebooks/
│   ├── phase-00-orientation/
│   │   └── 00-what-is-spark.ipynb
│   │
│   ├── phase-01-dataframe-basics/
│   │   ├── 01-creating-dataframes.ipynb
│   │   ├── 02-select-filter-withcolumn.ipynb
│   │   └── 03-spark-sql-temp-views.ipynb
│   │
│   ├── phase-02-transformations-actions/
│   │   └── 04-transformations-vs-actions.ipynb
│   │
│   ├── phase-03-aggregations/
│   │   ├── 05-columns-built-in-functions.ipynb
│   │   ├── 06-groupby-aggregations.ipynb
│   │   └── 07-window-functions.ipynb
│   │
│   ├── phase-04-joins/
│   │   ├── 08-joins-in-spark.ipynb
│   │   └── 09-common-join-problems.ipynb
│   │
│   ├── phase-05-reading-writing/
│   │   ├── 10-reading-files.ipynb
│   │   └── 11-writing-data.ipynb
│   │
│   ├── phase-06-delta-lake/
│   │   └── 12-intro-to-delta-tables.ipynb
│   │
│   ├── phase-07-etl-quality/
│   │   ├── 13-simple-etl-pipeline.ipynb
│   │   └── 14-data-quality-checks.ipynb
│   │
│   ├── phase-08-performance/
│   │   ├── 15-partitions-and-parallelism.ipynb
│   │   ├── 16-caching-and-persistence.ipynb
│   │   └── 17-understanding-explain-plans.ipynb
│   │
│   └── phase-09-practical-projects/
│       ├── 18-retail-sales-analytics.ipynb
│       ├── 19-healthcare-outcomes-analytics.ipynb
│       └── 20-public-sector-inspection-analytics.ipynb
│
├── datasets/
│   ├── README.md
│   └── sample-data-notes.md
│
├── sql/
│   ├── dashboard-views/
│   └── validation-queries/
│
├── images/
│   ├── architecture-diagrams/
│   └── notebook-screenshots/
│
└── docs/
    ├── concepts/
    ├── glossary.md
    └── spark-cheatsheet.md
