# Apache Spark vs PySpark vs Databricks Spark

## 1. Apache Spark

Apache Spark is the core engine — an open-source, distributed computing system.

- Written in **Scala** (JVM-based)
- Executes jobs in parallel across a cluster
- Supports multi-language APIs: **Scala**, **Java**, **Python**, **R**
- Used for **big data processing**, **ETL**, **ML**, **graph processing**, and **streaming**

When someone says “Apache Spark”, they mean the **underlying technology** that everything else builds on.

## 2. PySpark

**PySpark** is the official **Python API** for Apache Spark.

Lets you use Python to:

- Load data (e.g., CSV, Delta, Parquet)
- Write transformations and queries
- Train ML models (with Spark MLlib or Pandas APIs on Spark)

Internally, it translates Python code to JVM bytecode using **Py4J** or **Spark Connect**.
You write Python code, but it’s **executed by the Spark engine**, often running in the JVM on a cluster.


## 3. Databricks Spark (aka Databricks Runtime)

**Databricks Spark = Apache Spark + Databricks Runtime Enhancements**

This is what runs inside Databricks notebooks.

Based on open-source Apache Spark, it includes:

- Optimizations for **Delta Lake**
- Enhanced **Spark SQL** performance
- **MLflow** integration
- **Auto-scaling**, **serverless** options
- Better support for **pandas**, **Arrow**, and **GPU** workloads

## In Simple Terms

| Term                 | What It Is                              | Language    | Where It Runs                    |
| -------------------- | --------------------------------------- | ----------- | -------------------------------- |
| **Apache Spark**     | Core distributed compute engine         | Scala (JVM) | Open-source / Cloud / Databricks |
| **PySpark**          | Python API for Spark                    | Python      | Runs on Spark via JVM or Connect |
| **Databricks Spark** | Apache Spark + Databricks optimizations | Multi-lang  | On Databricks clusters (managed) |

## How This Affects You in Databricks
- When you're using a notebook in Databricks:
    - You’re writing PySpark (Python code using the `spark` object)
    - That code is executed by Apache Spark
    - It’s all managed by the Databricks platform, which gives you enhanced features like:
        - Delta Lake
        - SQL Warehouses
        - Auto-scaling clusters