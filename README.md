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
```

Learning Roadmap
Phase	Topic	Notebooks
```
Phase 0	Spark Orientation	Notebook 0
Phase 1	PySpark DataFrame Basics	Notebooks 1-3
Phase 2	Transformations, Actions, and Lazy Evaluation	Notebook 4
Phase 3	Columns, Aggregations, and Windows	Notebooks 5-7
Phase 4	Joins and Relational Thinking	Notebooks 8-9
Phase 5	Reading and Writing Data	Notebooks 10-11
Phase 6	Delta Lake and Tables	Notebook 12
Phase 7	ETL and Data Quality	Notebooks 13-14
Phase 8	Performance Fundamentals	Notebooks 15-17
Phase 9	Practical Analytics Projects	Notebooks 18-20
```

# Featured Projects
## Retail Sales Analytics Mini-Project

Builds a small lakehouse-style analytics workflow using synthetic retail transaction data.

Outputs include:
```
Raw transactions
Clean transactions
Store summary
Category summary
Customer summary
High-value transaction report
```
## Practices Spark on a healthcare-flavored orthopedic outcomes dataset.

Skills demonstrated:
```
Patient, procedure, and follow-up joins
Filtering patients with follow-up
Average outcome by implant type
Complication rates by age bucket
Window functions for latest follow-up
Patient-level modeling table preparation
```
## Simulates a public sector inspection analytics modernization scenario.

Skills demonstrated:
```
Shipment, inspection, and port joins
Data quality checks for missing inspection records
Anti joins for unmatched records
Violation aggregation
Window functions for top inspection categories
Executive dashboard-ready SQL views
```

This repository demonstrates practical ability with:
```
PySpark DataFrame API
Spark SQL
SparkSession basics
DataFrame schemas
Transformations and actions
Lazy evaluation
Column expressions
Built-in Spark functions
Aggregations
Window functions
Joins
Anti joins and semi joins
Data quality checks
ETL design
Delta Lake basics
Reading and writing files
Creating managed tables
Creating SQL views
Partitioning concepts
Caching and persistence
Query plan inspection with explain()
Translating raw data into business-ready outputs
Portfolio Notes
```

This repository demonstrates my ability to:
```
Learn and document technical concepts clearly
Build end-to-end analytics workflows in Spark
Transform raw data into trusted analytical outputs
Design reusable data quality checks
Create summary tables for reporting and dashboards
Use Spark SQL and PySpark together
Think carefully about table grain before joining data
Explain performance concepts such as partitions, shuffles, caching, and query plans
Connect technical implementation to business outcomes
```

# How to Use This Repository
## Option 1: Run Notebooks in Databricks Free Edition
```
Sign up for Databricks Free Edition.
Clone or download this repository.
Open your Databricks workspace.
Import a notebook from the notebooks/ folder.
Run the notebook cells from top to bottom.
Modify the exercises to test your understanding.
```

## Option 2: Use the Repo as a Learning Guide
You can also read the notebooks directly on GitHub and use them as a study guide.

Each notebook is designed to include:
```
Plain-English explanations
Commented PySpark code
Small synthetic datasets
Practice exercises
Mini-project reflection sections
Common mistakes
Key takeaways
```
# Recommended Study Order

Start from the beginning and move sequentially:

00 → 01 → 02 → 03 → 04 → 05 → 06 → 07 → 08 → 09

Then move into data engineering patterns:

10 → 11 → 12 → 13 → 14

Then performance fundamentals:

15 → 16 → 17

Then practical projects:

18 → 19 → 20

For each notebook:
```
Read the markdown explanations.
Run each code cell.
Inspect the output.
Change small pieces of the code.
Re-run the cell.
Complete the exercises.
Write your own notes in markdown.
Commit your updated notebook to GitHub.
```

The best way to learn Spark is not just to read the code, but to change it and observe what happens.

# Notes on Synthetic Data

The datasets in these notebooks are synthetic and simplified.

They are designed for learning Spark concepts, not for making real business, healthcare, or public sector decisions.

# Future Improvements

Planned additions may include:
```
- Intermediate Spark performance examples
- More Delta Lake examples
- Structured Streaming intro notebooks
- ML feature engineering in Spark
- MLflow basics
- Databricks Workflows examples
- Unity Catalog concepts
- Dashboard screenshots
- Architecture diagrams
- More public sector, healthcare, and retail analytics projects
- Repo Status
```
## This repository is a work in progress.

## Current focus:
```
Spark fundamentals
PySpark DataFrame practice
Databricks notebook workflows
Practical analytics mini-projects
```
## Future focus:
```
Intermediate Spark performance
ML feature preparation
MLflow
Lakehouse architecture patterns
Databricks Solution Architect-style demos
```

# License

This repository uses the MIT License. See LICENSE for details.

# Acknowledgments

This project is built around Apache Spark, PySpark, Delta Lake, and Databricks notebook workflows.

Databricks Free Edition makes it possible to practice these skills in a browser-based environment without setting up local Spark infrastructure.
