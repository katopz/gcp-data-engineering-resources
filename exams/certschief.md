## Question 1
Your company is evaluating moving to Google Cloud. You will need to migrate your 3 TB on-premises MySQL databases to a managed database service in order to reduce administrative overhead. Minimal modification to the database is desired for the move. What managed database service would best meet this requirement?

- [ ] A. Cloud Spanner
- [ ] B. Cloud Datastore
- [ ] C. `Cloud SQL`
- [ ] D. Cloud `BigTable`

<details><summary>ANSWER</summary>
<b>
C. `Cloud SQL`
</b>

> `Cloud SQL` is the direct lift and shift option for existing MySQL workloads and requires minimal modification.
> `Cloud `BigTable`` is a NoSQL analytics database, and not a direct equivalent to a MySQL lift and shift operation.
</details>

---

## Question 2
You are evaluating a storage solution for your data. Your data is in structured, non-relational format, and will be used for analysis. You need low latency reads to your data, which is at least 40TB in size and growing. What solution should you use?

- [ ] A. Cloud `BigTable`
- [ ] B. Cloud Spanner
- [ ] C. `Cloud SQL`
- [ ] D. Cloud Datastore

<details><summary>ANSWER</summary>
<b>
A. Cloud `BigTable`
</b>

> `BigTable` meets the requirements of _low latency_ analysis on _non-relational_ data.
> `Cloud Datastore` supports _non-relational_ data, but is geared more toward transactional uses than analytics.
</details>

---

## Question 3
You need to correct streaming messages that arrive out of order due to latency. Which Google Cloud service would you use to resolve this?

- [ ] A. `BigQuery`
- [ ] B. Cloud Dataflow
- [ ] C. Cloud Pub/Sub
- [ ] D. `Cloud SQL`

<details><summary>ANSWER</summary>
<b>
B. Cloud Dataflow
</b>
</details>

---

## Question 4
How would you best connect your `Dataflow` pipeline to `BigTable` for output?

- [ ] A. Use `Cloud Storage` as a staging ground for outputting into `BigTable`. 
- [ ] B. You cannot connect `BigTable` to `Dataflow`.
- [ ] C. Use the `Cloud Dataflow` connector for `BigTable`.
- [ ] D. `Dataflow` connects natively to `BigTable`.

<details><summary>ANSWER</summary>
<b>
C. Use the `Cloud Dataflow` connector for `BigTable`.
</b>
</details>

---

## Question 5
Which of these open source technologies is the direct equivalent to Google `BigQuery`?

- [ ] A. Hive
- [ ] B. Spark
- [ ] C. Hadoop
- [ ] D. Pig

<details><summary>ANSWER</summary>
<b>
A. Hive
</b>

> `Hive` is a data warehouse application that uses SQL queries, which is exactly what `BigQuery` performs.
> `Hadoop` is not a data warehouse solution.
</details>

---

## Question 6
What is a requirement for running preemptible workers on a `Dataproc` cluster?

- [ ] A. You can only have a maximum of a 2:1 ratio of preemptible to standard worker nodes.
- [ ] B. Preemptible nodes are only available on high availability master node configurations.
- [ ] C. The cluster must also have at least two standard worker nodes
- [ ] D. You must configure the startup and shutdown scripts to gracefully handle preemptible nodes being shut down.

<details><summary>ANSWER</summary>
<b>
C. The cluster must also have at least two standard worker nodes
</b>
</details>

---

## Question 7
You need to extract an address field from a multi-column element using `Dataflow`. Which mechanism is able to help with this task?

- [ ] A. Window
- [ ] B. ParDo
- [ ] C. PCollection
- [ ] D. Transform

<details><summary>ANSWER</summary>
<b>
B. ParDo
</b>

> `ParDo` is a type of transform that can extract data from a data source.
> You need to use a transform, but a `ParDo` is the specific type of function we are looking for.
</details>

---

## Question 8
You want to use an open source framework for constructing unified batch and data stream pipelines. Which open source framework should you choose?

- [ ] A. Cassandra
- [ ] B. Apache Hadoop
- [ ] C. Apache Beam
- [ ] D. HBase

<details><summary>ANSWER</summary>
<b>
C. Apache Beam
</b>

> `Hadoop` does not support batch and stream processing.
> `Apache Beam` is the open source framework that `Dataflow` is built on, and supports unified batch and data stream pipelines.
</details>

---

## Question 9
Which `Dataflow` concept determines when the contents of a window should be submitted, based on certain conditions being met?

- [ ] A. Watermark
- [ ] B. Trigger
- [ ] C. Condition
- [ ] D. Windows

<details><summary>ANSWER</summary>
<b>
B. Trigger
</b>

> Triggers are what determine when a window's contents should be.
</details>

---

## Question 10
How can you connect to the web interface of a `Dataproc` cluster? (Choose two)

- [ ] A. VPN proxy
- [ ] B. Allow the necessary web ports access via firewall rules, and limit access to your network.
- [ ] C. HTTP proxy
- [ ] D. SOCKS proxy

<details><summary>ANSWER</summary>
<b>
B. Allow the necessary web ports access via firewall rules, and limit access to your network.
D. SOCKS proxy
</b>
</details>

---

## Question 11
Which of these actions can you not perform with the `BigQuery` Web UI?

- [ ] A. Assign IAM roles.
- [ ] B. Toggle Legacy SQL to off on queries.
- [ ] C. Load multiple files at once
- [ ] D. Create dataset

<details><summary>ANSWER</summary>
<b>
C. Load multiple files at once
</b>

> You can toggle Legacy SQL to off using the Web UI.
> You cannot load multiple files with the web UI, but can with others methods such as the command line.
</details>

---

## Question 12
You have a very large table with many columns that are not immediately relevant to your non-IT team members. You want to reduce the amount of irrelevant column data available in your table in order to keep from confusing your team members that need to run queries against it. What is a valid method of achieving this task?

- [ ] A. Create a copy of the table, and delete the unneeded columns.
- [ ] B. Assign IAM roles to only the columns that your staff needs access to.
- [ ] C. Use views to restrict the amount of data available, and have team members run their query against the view.
- [ ] D. Hide the unneeded columns from the table.

<details><summary>ANSWER</summary>
<b>
C. Use views to restrict the amount of data available, and have team members run their query against the view.
</b>

> You cannot assign `IAM` roles by columns.
> A view offers a virtual table that uses data pulled from a more restrictive query, giving less information to work with.
</details>

---

## Question 13
Which of these is not a valid `BigQuery` data format?

- [ ] A. JSON
- [ ] B. AVRO
- [ ] C. CSV
- [ ] D. DOC

<details><summary>ANSWER</summary>
<b>
D. DOC
</b>

> `BigQuery` can natively load `CSV` files. `BigQuery` cannot load `.DOC` files.
</details>

---

## Question 14
Choose two best practices for creating more efficient queries and saving costs.

- [ ] A. Save your biggest `JOINs` for last
- [ ] B. Avoid using `SELECT *` for column selection.
- [ ] C. Normalize your data when possible.
- [ ] D. Filter early and big with `WHERE` clauses

<details><summary>ANSWER</summary>
<b>
B. Avoid using `SELECT *` for column selection.
D. Filter early and big with `WHERE` clauses
</b>

> Since `BigQuery` is columnar, choosing unnecessary columns greatly increases query amounts.
> You want to de-normalize when possible, with nested/repeating columns.
> The more data you can filter out at the start, the more efficient your queries will be.
</details>

---

## Question 15
You want to analyze data in `BigQuery` that currently sits in the `Cloud SQL` service. How can you best get your `Cloud SQL` data into `BigQuery`?

- [ ] A. It is not possible to view `Cloud SQL` data in `BigQuery`
- [ ] B. Use the `BigQuery` connector in `Cloud SQL` to export from `Cloud SQL` to `BigQuery`
- [ ] C. In `Cloud SQL`, designate `BigQuery` as an alternative write location.
- [ ] D. Export your `Cloud SQL` data to `Cloud Storage`, and then import from `Cloud Storage` to `BigQuery`.

<details><summary>ANSWER</summary>
<b>
D. Export your `Cloud SQL` data to `Cloud Storage`, and then import from `Cloud Storage` to `BigQuery`.
</b>

> You need to use `Cloud Storage` as your staging ground for importing `Cloud SQL` data into `BigQuery`.
</details>

---

## Question 16
Which of these are you not charged for in `BigQuery`?

- [ ] A. Queries
- [ ] B. Loading batch data
- [ ] C. Streaming Inserts
- [ ] D. Table storage

<details><summary>ANSWER</summary>
<b>
B. Loading batch data
</b>

> You are not charged for load and export operations in `BigQuery`.
> You are charged a small premium for streaming inserts.
</details>

---

## Question 17
You are viewing the details of a recent large query and notice that Stage 1 has a full purple bar. What does this tell you?

- [ ] A. Stage 1 spent most of its time reading from a large dataset.
- [ ] B. Stage 1 had a heavy computation procedure
- [ ] C. Your query could not be successfully completed.
- [ ] D. Your query stage spent a long time waiting for additional input.

<details><summary>ANSWER</summary>
<b>
A. Stage 1 spent most of its time reading from a large dataset.
</b>

> The purple indicator indicates high read time.
> Computation is designated by the orange bar, not purple.
</details>

---

## Question 18
Which Hadoop ecosystem service is most suited to storing on `BigQuery` instead?

- [ ] A. HDFS
- [ ] B. PySpark
- [ ] C. Hive
- [ ] D. Spark

<details><summary>ANSWER</summary>
<b>
C. Hive
</b>

> `Hive` is a data warehousing service, which is suited for `BigQuery`.
> `Spark` is a machine learning service, not suited to `BigQuery`.
</details>

---

## Question 19
To run a local training job using the `Google Cloud SDK`, what command would you run?
- [ ] A. gcloud ml-engine jobs submit training --local
- [ ] B. gcloud ml-engine job submit local
- [ ] C. gcloud ml-engine local train
- [ ] D. You cannot use the Google Cloud SDK for local training.

<details><summary>ANSWER</summary>
<b>
C. gcloud ml-engine local train
</b>
</details>

---

## Question 20
You need to give a team member the ability to use a training model for predictions, but not have the ability to create or delete models. What `IAM` role should you assign to achieve this task with the minimum necessary permissions?

- [ ] A. Cloud ML Engine Developer
- [ ] B. Project Editor
- [ ] C. Model User
- [ ] D. Model Owner

<details><summary>ANSWER</summary>
<b>
C. Model User
</b>
</details>

---
