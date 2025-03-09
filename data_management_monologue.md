# The Complete Evolution of Data Management Systems

Hello, fellow data engineers and architects. Today, we'll explore the complete evolution of data management systems, examining how each technological advancement shaped our current data lakehouse architecture.

Let's begin with our core components from the 1970s and 1980s. In this era, our initial constraints were significant. We were working with single-core processors like the IBM System/370, which required manual optimization. RAM was limited to kilobytes or early megabytes, forcing us to focus on efficient memory usage. Storage consisted of magnetic disks with capacities around 70MB, demanding careful data organization. Network connectivity was basic, provided through RS-232 and early Ethernet. And finally, data was primarily structured, transaction-focused information.

These limitations shaped our early architectural decisions. Every byte was precious, leading to normalized database designs to minimize redundancy. We focused on ACID compliance to ensure transaction reliability. And we dedicated significant effort to careful capacity planning and resource optimization.

When data management systems arrived, data storage and processing were costly. The focus was only on the data that mattered the most, hence a lot of focus was on storing the data online once using normalizations. It was also the time to win the trust of the customers that online interactions were safe. Hence, a lot of focus was on solid transaction management respecting ACID principles. RDBMS normalization along with ACID transactions gave the required boost to DBMS of that time. All this data was highly structured, and these RDBMS are called transactional systems.

As businesses grew, more data was accumulated across time, regions, and business partners. This led to the need to analyze this vast amount of structured data to harvest actionable business insights. Thus, the business intelligence suite of products was born, which could read large amounts of structured data. The performance of these BI tools came at the trade-off of storage. This was achieved using star and snowflake schemas, which worked best for the BI tools by storing redundant data. These large storages were called warehouses.

Anomalies related to reduced normalizations were handled by separating the transaction system from the warehouses, ensuring that data quality and data integrity were managed by the transactional systems, while warehouses only handled the data arriving from the OLTP systems. This segregation is known as OLTP-OLAP.

As technology advanced, RAM became cheaper, and OLTP systems grew massively. Persistent storage also became cheaper, allowing OLAP systems to grow rapidly. However, persistent storage was still slow. Solution providers deployed multiple techniques to address the cost versus speed issue, such as network storage, new file formats, caching, and cost-based optimization of query plans.

All this while, data that was not core to the business was often discarded. Examples include website traffic, system logs, sensor data, audio data, transcripts, video data, and user demographics. Much of this data remained unstructured in files and was often discarded.

As processing became cheaper, RAM became faster and cheaper, and persistent storage became faster and cheaper, people started to look at the often discarded unstructured data for additional insights. This marked the arrival of the big data stack. Companies were able to deploy relatively cheaper, often redundant hardware to mine this data for intelligence using techniques like MapReduce.

With the arrival of even faster persistent storage (SSD) and cloud compute, MapReduce gave way to lazy evaluation (Spark). When technology became economical enough to store large data and process it faster, a fundamental age-old assumption was challenged: Do we really need to structure/model the data to run the transactional business and generate insights?

Schema-on-read started providing enough and faster value in many functional domains, especially booming e-commerce, e-delivery, e-taxi, and subscription-based businesses. The whole focus was to acquire customers faster and allow the freedom for customers to start and stop subscriptions with any competitors of their choice at any time.

This shifted the paradigm of how we store and process data, how we create business solutions, and how we adapt and evolve business solutions in a competitive environment. This means we have to store the data even before we can fully understand it. We have to generate insights before our competition. We have to adapt as the market moves. This means organizations have to adopt storing data as it arrives, without wasting time modeling it into a rigid structure (schema-on-write), figuring out the fit-for-purpose structure as business needs arise (schema-on-read), and augmenting it with more data, often external, to generate actionable insights.

As unstructured data and schema-on-read became prevalent, traditional approaches of transactional databases (ODS) and warehouses started showing their technical limitations. The concept of data lakes provided answers to this, where organizations could store vast amounts of unstructured data and process it at an economical pace without worrying about the underlying infrastructure complexities.

However, as data lakes were not strict about sourcing data only from the enterprise ODS, we started seeing a lot of data quality and data governance issues. People started calling data lakes "data swamps."

There was a need to find a middle path between enterprise warehouses and data lakes. It was not possible to put unstructured data in traditional RDBMS and still use relational algebra (SQL) on top of it. This only made RDBMS like Oracle and even cloud-native warehouses like Snowflake clunky, costly, and slow. There is merit in keeping structured transactional systems separate from late-arriving unstructured data.

Another solution that seems to be working is building a strong metadata layer on data lakes to aid schema design, quality, and governance. Such architecture is called a lakehouse. By deploying this metadata layer, lakehouses can provide ACID transactions as well as asynchronous arrival of data with or without high data integrity and structure.

Apache Iceberg tables are one such technology. However, big players like Oracle and even relatively new cloud-first players like Snowflake could not address the need for ever-increasing data governance. A middle path was required.

The data lakehouse architecture provides several key benefits. First, it offers technical foundations like ACID transactions on cloud storage, schema enforcement and evolution, time travel and versioning, and optimized file formats. Second, it provides governance features, including robust metadata management, data quality controls, access control and security, and lineage tracking. Third, it delivers performance capabilities, such as query optimization, data skipping, caching mechanisms, and concurrent access support.

When implementing a data lakehouse, consider these modern implementation considerations. For the storage layer, think about optimal file sizes and partitioning, compression strategies, data lifecycle management, and multi-format support. For the processing layer, focus on distributed query optimization, resource management, workload isolation, and caching strategies. And for the metadata layer, prioritize schema evolution, quality enforcement, access control, and lineage tracking.

Looking ahead, we face several key challenges. These include technical challenges like scaling metadata operations, optimizing real-time processing, improving query performance at extreme scale, and optimizing costs. We also face governance challenges, including data privacy compliance, cross-border regulations, security requirements, and quality maintenance.

The data lakehouse represents a culmination of our journey in data management, combining traditional database reliability with modern scalability, preserving data quality while enabling flexibility, supporting both traditional and emerging workloads, and providing a foundation for future innovation.

Remember, while technologies evolve, our fundamental goals remain constant: ensuring data reliability, optimizing performance, maintaining governance, and enabling valuable insights.

As we continue this journey, our experience with traditional systems becomes even more valuable, helping us build robust, scalable, and efficient data architectures for the future.
