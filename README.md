# Data Culpa Validator Documentation

This repository contains all the documentation for [Data Culpa Validator](https://www.dataculpa.com/what-we-do/).

We are importing articles from our KB and setting up examples for APIs, etc.

Our open source Python API is in its own repository.


## Overview

Data Culpa Validator provides analytics and alerting for both data at rest and data in motion. You can send data to Validator from an API for processing during your data operations. You can tag the data with metadata to enable you to organize the downstream analysis and we also have APIs to enable including your own log or error messages that you want to see in the data analysis flows.

In addition, you can use our "connectors" to regularly query the contents of a file system (data lake or buckets), databases, or data warehouses. This means you can regularly monitor the contents of MongoDB, Snowflake, BigQuery, CSV files, JSON files, and many other databases and cloud storage buckets. We provide open source connectors that use our simple API, as well as a higher performance FastCols™ built-in connectors that leverage massive paralel computation for the best processing throughput. We have scaled this solution to billions of records per hour on thousands of compute jobs.

## Splitting Environments

You can load data from multiple environments for comparison; for example, you can load data tagged for QA to compare to production. You can rev a version tag to compare the behavior of an updated cleaning function or a changed data model to verify that the results are as expected.

## Watchpoints

Watchpoints are a specific place where you want to observe your data. This can be a specific point in a pipeline, or it can be a specific table or view in a database.

## Alerts and Feedback Loops

When Data Culpa generates an alert, you can confirm its accuracy so that the alert condition will not be learned. Validator works by self-adjusting its expectation of "normal" behavior as your data moves; an alert that is trigged due to a change that reflects a "new normal" will self-clear itself. Upcoming visualizations will help communicate where the data is moving and approaching limits as a leading indication of alerts to come.

## Anomaly Detection

Validator considers the data from a hierarchy of throughput, schema, data types, and distribution of values. 
