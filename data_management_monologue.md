# The Evolution of Data Management Systems

Hello, fellow data engineers and architects. Today, we'll explore the evolution of data management systems and how each technological advancement shaped our current data lakehouse architecture. I hope this introduction helps you understand the emergence of data lakehouses.

Let's begin with the 1970s and 1980s. During this era, computing resources were scarce and expensive. We relied on single-core processors like the IBM System/370, limited RAM, and magnetic disks with small capacities. Network connectivity was basic, and data was primarily structured and transaction-focused.
Business focus was primarily on essential data. Hence, data was stored using normalization, which reduces the data footprint to non-redundant values.

This era was also crucial for gaining consumer trust in centralized processing using computers, replacing manual, distributed processes. RDBMS normalization, along with ACID transactions, significantly boosted DBMS adoption during that time. This data was highly structured, and these RDBMS systems were known as transactional or OLTP systems.

As businesses grew, more data accumulated across time, regions, and business partners. This led to the need to analyze vast amounts of structured data for actionable insights. Thus, the business intelligence suite of products was born, capable of reading large amounts of structured data. The performance of these BI tools came at the trade-off of storage. These new BI tools worked better with slightly redundant data stored in dimensional models like star and snowflake schemas. These large storages were called data warehouses or OLAP systems.

Deviation from 3rd normal form and redundant data leads to various anomalies related to data integrity and quality. To handle these anomalies, we separated transaction systems from warehouses, ensuring data quality and integrity were managed by transactional systems, while warehouses were ONLY fed from the OLTP systems. This segregation is known as OLTP-OLAP. Remember this guardrail that OLAP systems were fed only from enterprise OLTP systems, as I will refer to it later in the context of data lakes.

With technological advancements, RAM became cheaper, CPUs became faster, and storage became larger and cheaper. This facilitated massive growth of OLTP-OLAP systems.

The 2000s brought the internet era, leading to unprecedented challenges. Organizations started mining previously discarded data for competitive advantages. These new data types included system logs, social media feeds, and sensor data. A lot of this data was unstructured and was arriving asynchronously in micro batches. Companies were able to deploy relatively cheaper, often redundant hardware to mine this data for intelligence using techniques like MapReduce and Hadoop. Key technological advances at that time included multi-core processors, gigabyte-scale RAM, distributed file systems, and gigabit networks.

With the arrival of even faster persistent storage (SSD) and cloud compute, MapReduce gave way to distributed and lazy evaluation frameworks like Spark.

As technology became economical enough to store large amounts of data and process it faster, a fundamental, age-old assumption was challenged:

Do we really need to structure and model the data before we run business transactions and generate insights?

Schema-on-read started providing sufficient and faster value in many functional domains, especially in the booming startup economy with e-commerce, e-delivery, e-taxi, and subscription-based businesses. The primary focus was to acquire customers faster and allow them the freedom to start and stop subscriptions with any competitor at any time. Hence, defining an enterprise schema before writing data became an impediment to speed to market.

This shifted the paradigm of how we store and process data, how we create business solutions, and how we adapt and evolve business solutions in a competitive environment.

This means organizations have to:
a) store the data as it arrives, without wasting time modeling it into a rigid structure (schema-on-write),
b) figure out the fit-for-purpose structure as business needs arise (schema-on-read), and
c) augment it with more data, often external, to generate actionable insights.

In the modern era, from the 2010s to the present, we see cloud-scale processing with specialized AI chips, terabyte-scale RAM, object storage, SSDs, high-speed cloud interconnects, and real-time, streaming, and AI-generated data.

The data lake emerged to address the need for flexible storage of raw data, support for varied data formats, reduced time-to-insight, and cost-effective storage solutions.

However, it introduced a new problem, or rather resurfaced an old one. As data lakes were not restricted to being fed only from enterprise OLTP systems, data arriving in the lake became inconsistent, of mixed quality, and highly redundant. Businesses found it difficult to trust and act on insights generated from such systems, as data was not properly governed and insights were not traceable to the golden sources. People started calling data lakes data swamps.

There was a need to find the middle path between enterprise warehouses and data lakes.

It was not feasible to put unstructured data in traditional RDBMS and still use relational algebra (SQL) on top of it. Oracle tried it, but it made the system clunky, costly, and slow. There is merit in keeping structured transactional systems separate from late-arriving unstructured data.

Another solution, which seems to be working, is to build a strong metadata layer on the existing data lake to aid schema design, quality, and governance. Such an architecture is called a data lakehouse.

The data lakehouse architecture provides several key benefits: ACID transactions on cloud storage, schema enforcement and evolution, time travel and versioning, and optimized file formats. It also provides robust metadata management, data quality controls, access control and security, and lineage tracking. Additionally, it delivers performance capabilities, such as query optimization, data skipping, caching mechanisms, and concurrent access support.

As this meta data is stored within same ecosystem as data, various AI tools could be used to enhance the meta data and interact with data withing natual language through LLMs.

Apache Iceberg tables, Databricks Delta tables, and Apache Hudi are emerging components of this architecture.

Data lakehouse vendors are working to address some the moving targets in this space like scaling metadata operations, optimizing real-time processing, improving query performance at extreme scale, optimizing costs, and portability across various lakehouse providers. While enterprise using lakehouse need to evolve data governance policies, build better understanding of data privacy, be aware of cross-border regulations, have up to date security requirements, and have a dynamic view of the data quality.

The data lakehouse is an offspring of the traditional database reliability and data lake scalability.

Remember, while technologies evolve, our fundamental goals remain constant: improving data availablity, ensuring data reliability, optimizing performance, maintaining governance, and enabling valuable insights.