# What is Data Culpa Validator?

Data Culpa Validator is an application that checks the consistency of ingested — whether in a data feed, database, data warehouse, or in files deposited in a data lake — before you perform further operations on that data, such as transforming the data or loading it in your processing pipeline. With Validator, you can catch problems at the source before they turn into errors in your data warehouse, ML model, or analytical reports.

# What are the system requirements for running Validator?

For on-premesis deployments, you need a Docker and, for our proprietary FastCols™ ingest, a Kubernetes environment. (FastCols™ is available on Medium Pro and up subscriptions.)

# Can I run Validator as a SaaS?

Yes; this is our preferred deployment method. We offer private tenet deployments in our cloud starting at $50/mo.

# What is a watchpoint in Validator?

# A watchpoint is the location in your pipeline or business process where you invoke Validator to analyze your data.

# What is a session in Validator?

A session in a single instance of a data set. For example, if your pipeline imports data once a day, five days a week, the data imported on Monday would be one session, the data imported on Tuesday another session, and so on.

Think of sessions as data sets associated with a time.

# What types of alerts does Validator produce?

Anomalous row counts
Probability distribution changes
Duplicate and near-duplicate data
Schema changes
Type changes
Corrupted inputs
Lack of activity

# How can I receive alerts from Validator?

Alerts can be pushed to Slack or accessed via our API. They are also visible in the Validator GUI.

# What is a gold standard in Validator?

A gold standard is a session that you have selected an identified as representative of the sessions you expect your pipeline to process for a specific use case.

# How do I run comparisons in Validator?

Create a Validator watchpoint in the pipeline or repository you want to monitor. Validator will report on differences in the data processed over time.

# Can I print reports from Validator?

In version 1.0, you can print the graphs and dashboard data you see in your browser.

# What data platforms does Validator support?

Data Culpa provides ope source connectors to the following data platforms:

Azure Data Lakes
BigQuery
MongoDB
Snowflake

# Who should I contact for help with Validator?

Write to support@dataculpa.com.
