# CheatSheet for Snowflake, Databricks, and Oracle Cloud

A comprehensive comparison table between Snowflake, Databricks, and Oracle Cloud Infrastructure (OCI):

| Category Group    | Category                              | Snowflake                          | Databricks                         | Oracle Cloud (OCI)                 |
|-------------------|---------------------------------------|------------------------------------|------------------------------------|------------------------------------|
| Architecture      | Core Platform                         | Snowflake Data Cloud               | Databricks Lakehouse               | Oracle Cloud Infrastructure        |
| Architecture      | Storage Format                        | Micro-partitions                   | Delta Lake                         | Oracle Block Storage / Object Storage |
| Architecture      | Compute                               | Virtual Warehouses                 | Clusters                           | Oracle Compute Instances           |
| Architecture      | Cluster Management                    | Fully Managed                      | Managed Clusters                   | Oracle Kubernetes Engine           |
| Performance       | Processing Engine                     | Snowflake SQL Engine               | Apache Spark + Photon              | Oracle Database SQL Engine         |
| Performance       | Execution Engine                      | Query Optimizer                    | Photon                             | Exadata Smart Scan                 |
| Architecture      | Control Plane                         | Snowflake Control Services         | Databricks Control Plane           | Oracle Cloud Console               |
| Architecture      | Data Plane                            | Snowflake Storage Layer            | Databricks Execution & Storage Layer | Oracle Autonomous Data Warehouse   |
| Architecture      | Storage Layer                         | Proprietary Storage                | Delta Lake                         | Oracle Cloud Object Storage        |
| Architecture      | Metadata Store                        | Metadata Store                     | Unity Catalog + Hive Metastore     | Oracle Data Catalog                |
| Performance       | Data Warehouse                        | Snowflake Data Warehouse           | Databricks SQL Warehouse           | Oracle Autonomous Data Warehouse   |
| Architecture      | Lakehouse                             | Iceberg Tables / External Tables   | Delta Lake                         | Oracle Big Data Service            |
| Performance       | Virtual Warehouse                     | Virtual Warehouse                  | SQL Warehouse                      | Oracle Autonomous Warehouse        |
| Performance       | Serverless Execution                  | Snowpark                           | Serverless Compute                 | Oracle Functions                   |
| Integrations      | Programming Support                   | Snowpark (Python, Java, Scala)     | Notebooks (Python, Scala, SQL, R)  | PL/SQL, Java, Python, SQL          |
| Machine Learning  | Machine Learning                      | Snowpark ML (limited)              | Databricks ML (MLflow, AutoML)     | Oracle Machine Learning            |
| Integrations      | Data Sharing                          | Secure Data Sharing                | Delta Sharing                      | Oracle Data Safe                   |
| Security          | Data Catalog & Governance             | Data Governance                    | Unity Catalog                      | Oracle Data Catalog                |
| Integrations      | ETL/ELT Framework                     | Tasks & Streams                    | Workflows                          | Oracle Data Integrator (ODI)       |
| Security          | Access Control                        | RBAC                               | RBAC                               | Oracle IAM                         |
| Performance       | Cache Mechanisms                      | Query & Result Cache               | Delta Cache                        | Exadata Smart Flash Cache          |
| Performance       | Auto-Scaling                          | Multi-cluster Compute              | Adaptive Query Execution           | Oracle Auto-Scaling                |
| Security          | Network Security                      | Private Link                       | VPC Peering                        | Oracle Cloud VPN                   |
| Security          | Data Masking                          | Dynamic Masking                    | Unity Catalog Masking              | Oracle Data Redaction              |
