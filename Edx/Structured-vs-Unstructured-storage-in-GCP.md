
Let’s start with unstructured versus structured data.

- Unstructured data is information stored in a non-tabular form such as documents, images,
and audio files.
- Unstructured data is usually best suited to Cloud Storage.
- It’s estimated that around 80 percent of all data is unstructured.
- It’s far more difficult to process or analyze unstructured data using traditional methods
because the data has no internal identifier to enable search functions to identify it.
- Unstructured data often includes text and multimedia content, for example, email messages,
documents, photos, videos, presentations, and web pages.
- Organizations are focusing increasingly on mining unstructured data for insights that
will provide them with a competitive edge.

Alternatively, there is structured data, which represents information stored in tables, rows,
and columns.

- Structured data is what most people are used to working with and typically fits within
columns and rows in spreadsheets or relational databases.
- You can expect this type of data to be organized and clearly defined and usually easy to capture,
access, and analyze.
- Examples of structured data include names, addresses, contact numbers, dates, and billing
info.
- The benefit of structured data is that it can be understood by programming languages
and can be manipulated relatively quickly.

Structured data comes in two types: transactional workloads and analytical workloads.

- Transactional workloads stem from Online Transaction Processing systems, which are used when fast
data inserts and updates are required to build row-based records.
- This is usually to maintain a system snapshot.
- They require relatively standardized queries that affect only a few records.
- So, if your data is transactional and you need to access it using SQL, Cloud SQL and
Cloud Spanner are two options.
- Cloud SQL works best for local to regional scalability,
- But Cloud Spanner is best to scale a database globally.
- If the transactional data will be accessed without SQL,
- Firestore might be the best option.
- Firestore is a transactional NoSQL, document-oriented database.

Then there are analytical workloads, which stem from Online Analytical Processing systems,
which are used when entire datasets need to be read.
- They often require complex queries, for example, aggregations.
- If you have analytical workloads that require SQL commands, BigQuery may be the best option.
- BigQuery, Google’s data warehouse solution, lets you analyze petabyte-scale datasets.
- Alternatively, Bigtable provides a scalable NoSQL solution for analytical workloads.
- It’s best for real-time, high-throughput applications that require only millisecond
latency.
