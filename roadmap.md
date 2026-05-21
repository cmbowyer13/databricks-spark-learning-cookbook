
---

# Spark Learning Roadmap

This roadmap outlines the learning path for the Databricks Spark Learning Cookbook.

The goal is to move from Spark fundamentals to practical analytics workflows that resemble real data engineering, analytics, and lakehouse projects.

---

## Phase 0: Orientation — What Spark Is and Why It Exists

### Notebook 0: What is Spark?

**Goal:** Understand Spark as a distributed data processing engine.

You will learn:

| Concept | What You Should Understand |
|---|---|
| Spark | A distributed engine for processing data at scale |
| Driver | The process that coordinates the Spark job |
| Executors | Worker processes that run tasks |
| Cluster | The collection of compute resources Spark uses |
| SparkSession | Your main entry point into Spark from PySpark |
| DataFrame | Spark’s main tabular data abstraction |
| Lazy evaluation | Spark waits to execute until an action is called |
| Transformations | Operations that define a new DataFrame |
| Actions | Operations that trigger execution |

**Key lesson:** Spark is not faster pandas. Spark is a distributed computation engine.

---

## Phase 1: PySpark DataFrame Basics

### Notebook 1: Creating DataFrames

**Goal:** Learn how to create Spark DataFrames manually and from simple Python objects.

You will practice:

- Creating a DataFrame from a list of tuples
- Adding column names
- Inferring schemas
- Defining schemas manually
- Viewing data with `show()` and `display()`
- Inspecting structure with `printSchema()`, `columns`, and `dtypes`

**Mini-project:** Create a small retail transaction DataFrame.

---

### Notebook 2: Selecting, Filtering, and Adding Columns

**Goal:** Learn basic DataFrame transformations.

You will practice:

- `select()`
- `filter()`
- `where()`
- `withColumn()`
- `drop()`
- `alias()`
- Basic column expressions

---

### Notebook 3: Spark SQL and Temporary Views

**Goal:** Learn how Spark lets you mix Python DataFrame operations and SQL.

You will practice:

- `createOrReplaceTempView()`
- `spark.sql()`
- SQL filtering
- SQL aggregation
- Comparing SQL syntax with DataFrame syntax

**Mini-project:** Analyze transaction data using both DataFrame syntax and SQL syntax.

---

## Phase 2: Transformations, Actions, and Lazy Evaluation

### Notebook 4: Transformations vs Actions

**Goal:** Understand when Spark actually runs code.

You will learn:

| Type | Examples |
|---|---|
| Transformations | `select`, `filter`, `withColumn`, `groupBy` |
| Actions | `show`, `count`, `collect`, `display`, `write` |

**Mini-project:** Build a chain of transformations and inspect the query plan with `explain()`.

---

## Phase 3: Columns, Aggregations, and Window Functions

### Notebook 5: Working with Columns and Built-In Functions

**Goal:** Learn important PySpark column functions.

You will practice:

- Numeric functions
- String functions
- Date/time functions
- Conditional logic
- Null handling

**Mini-project:** Clean messy customer transaction data.

---

### Notebook 6: Aggregations with `groupBy`

**Goal:** Learn how to summarize data at scale.

You will practice:

- `count()`
- `sum()`
- `avg()`
- `min()`
- `max()`
- `agg()`
- Aliasing output columns
- Grouping by multiple columns

**Mini-project:** Analyze sales by store, product category, and month.

---

### Notebook 7: Window Functions

**Goal:** Learn one of the most powerful Spark concepts for analytics.

You will practice:

- `row_number`
- `rank`
- `dense_rank`
- `partitionBy()`
- `orderBy()`
- Running totals
- `lag`
- `lead`

**Mini-project:** Rank transactions within each store and calculate running revenue over time.

---

## Phase 4: Joins and Relational Thinking

### Notebook 8: Joins in Spark

**Goal:** Learn how Spark combines datasets.

You will practice:

| Join Type | Meaning |
|---|---|
| Inner join | Matching rows only |
| Left join | Keep all rows from left table |
| Right join | Keep all rows from right table |
| Full outer join | Keep all rows from both |
| Anti join | Rows in left with no match in right |
| Semi join | Rows in left with a match, but only left columns |

**Mini-project:** Join transactions to stores, products, and customers.

---

### Notebook 9: Common Join Problems

**Goal:** Learn what can go wrong with joins.

You will practice debugging:

- Duplicate keys
- Null join keys
- Missing matches
- Ambiguous column names
- Many-to-many joins
- Unexpected row counts
- Incorrect grain

**Important habit:** Always compare row counts before and after joins.

---

## Phase 5: Reading and Writing Data

### Notebook 10: Reading Files into Spark

**Goal:** Learn how Spark reads data from files.

You will practice:

- Reading CSV
- Reading JSON
- Reading Parquet
- Using read options
- Controlling schemas

**Mini-project:** Upload a small CSV to Databricks Free Edition and read it into Spark.

---

### Notebook 11: Writing Data

**Goal:** Learn how Spark writes outputs.

You will practice:

- Writing CSV
- Writing Parquet
- Write modes
- Partitioned writes
- Saving as tables

**Mini-project:** Clean a transaction dataset and write the output to a table or file.

---

## Phase 6: Delta Lake and Tables

### Notebook 12: Intro to Delta Tables

**Goal:** Understand why Databricks emphasizes Delta Lake.

You will practice:

- Saving DataFrames as Delta
- Creating managed tables
- Reading tables with `spark.table()`
- Reading tables with SQL
- Intro to updates, deletes, and time travel

**Mini-project:** Create a cleaned transaction Delta table and query it with SQL.

---

## Phase 7: Data Cleaning and ETL Patterns

### Notebook 13: Building a Simple ETL Pipeline

**Goal:** Learn the basic Extract, Transform, Load workflow.

You will practice:

| ETL Stage | Practice |
|---|---|
| Extract | Read raw data |
| Transform | Clean, filter, derive columns |
| Load | Save clean table |
| Validate | Check row counts and nulls |
| Document | Add comments and notebook markdown |

**Mini-project:** Raw transaction data → cleaned transactions table → summary analytics table.

---

### Notebook 14: Data Quality Checks

**Goal:** Learn basic validation patterns before trusting outputs.

You will practice:

- Row count checks
- Null checks
- Duplicate checks
- Range checks
- Category checks
- Join checks

**Mini-project:** Create a simple data quality report using Spark aggregations.

---

## Phase 8: Performance Fundamentals

### Notebook 15: Partitions and Parallelism

**Goal:** Understand how Spark splits work.

You will practice:

- Inspecting partition counts
- `repartition()`
- `coalesce()`
- Understanding shuffles
- `rdd.getNumPartitions()`

**Mini-project:** Compare partition counts before and after transformations.

---

### Notebook 16: Caching and Persistence

**Goal:** Learn when to cache DataFrames.

You will practice:

- `cache()`
- `persist()`
- `unpersist()`
- Repeated actions
- Understanding when caching helps or hurts

**Mini-project:** Run multiple aggregations on the same cleaned DataFrame and compare cached vs. uncached logic conceptually.

---

### Notebook 17: Understanding `explain()` Plans

**Goal:** Learn how to inspect Spark’s execution plan.

You will practice:

- Logical plans
- Physical plans
- Predicate pushdown
- Projection pruning
- Shuffle indicators
- Join plan inspection

**Mini-project:** Use `explain()` on filters, joins, and aggregations.

---

## Phase 9: Practical Analytics Projects

### Notebook 18: Retail Sales Analytics Mini-Project

**Goal:** Combine fundamentals into one realistic retail workflow.

You will build:

| Layer | Output |
|---|---|
| Raw transactions | Original ingested data |
| Clean transactions | Standardized table |
| Store summary | Sales by store |
| Category summary | Sales by category |
| Customer summary | Spend by customer |
| High-value transaction report | Filtered output |

---

### Notebook 19: Healthcare Outcomes Mini-Project

**Goal:** Practice Spark on a healthcare-flavored dataset.

You will practice:

- Filtering patients with follow-up
- Average outcome by implant type
- Complication rate by age bucket
- Patient table + procedure table joins
- Latest follow-up per patient using window functions

---

### Notebook 20: Public Sector / DHS-Style Inspection Analytics Mini-Project

**Goal:** Practice Spark with a Databricks Solution Architect-style scenario.

You will practice:

- Shipments + inspections + ports joins
- Violations by port
- Top inspection categories
- Missing inspection records
- SQL views for executive dashboard tables

---

## Future Roadmap

Potential future phases:

| Phase | Topic |
|---|---|
| Phase 10 | Intermediate Spark Performance |
| Phase 11 | Structured Streaming Basics |
| Phase 12 | ML Feature Preparation in Spark |
| Phase 13 | MLflow Basics |
| Phase 14 | Databricks Workflows |
| Phase 15 | Unity Catalog Concepts |
| Phase 16 | Solution Architect Demo Projects |
