# Alerts

### Alert Windowing

By default, Validator breaks time into days. This makes it easy to understand data flows over time and lets you compare flows day to day or week to week.

When multiple data streams arrive within a day, they are rolled up into a model for the given day. If a stream rolls over midnight, all of its data is considered to be part of the previous day.

To reduce alerts on expected seasonality and trending, Validator uses an extended set of windows for data comparison: a "week over week" comparison for up to the last 7 days of the week, and a rolling sequential window of data that has arrived in the last 7 days of data activity. These days can be sparse; there is no requirement to have data activity daily. Validator can handle irregular patterns of data, such as bi-weekly, weekly, every 3 days, and so on.


### Demo Mode

When using demo mode on a watchpoint, we replicate the first set of data that we saw to build a history of data to enable alerts right away. Alerts generated in demo mode will be annotated as such. We also support "Instant Training" of data to load historical data and generate historical alerts.

### Alert Types

The bulk of alert configuration lives in the 'single gear' configuration dialog.

![Alert Config Screenshot](https://bits.dataculpa.com/docs-screenshots/config-alerts.png)

* Missing data activity - This can refer to no data logged with Validator or no attempt to create a data session. When using Validator from a pipeline through the Validator API, we recommend opening and closing an empty queue when there is no data so that Validator can note that no activity occurred, but the pipeline was running.

* Schema changes - Validator tracks any change to the schema layout, such as a missing field or a new field being added.

* Duplicate data - We have heard horror stories of stale files being processed as if they were new. Duplicate data detection enables you to find big groups of duplicate columns that are not changing. If very few columns are present in the data set, Validator will "fuzzily" round down the threshold, but with 20+ columns, this is not necessary. Validator can rapidly search a month's worth of data looking for repeated sections of columns.

* *Note:* Validator does not attempt to find chunks of rows that are duplicate; these can be identified with either sub-views that split the data to look for this kind of behavior or potentially using the Validator pivot schema feature.

* Zeroes and nulls - This refers to big jumps of zeroes and nulls in a single column. When we talk about "deviations", we usually mean a median absolute deviation of motion over our data window. Sometimes we use the std deviation, depending on the data set.

* Data types - Validator ignores metadata about data types if available (e.g., SQL types) and attempts to promote data to its native type. As of version 1.8, Validator looks for numeric data, string data, inferred categories, and dates. We have found many data and numbers stored as strings (for example) intentionally, but our alerting is focused on changes in the underlying types that may not be expected.

* Distribution - Validator looks for changes in distributions. For strings we compute an entropy complexity so that we can map arbitrary strings into a meaningful distribution and for numeric data, we use a proprietary histogram method.

* Field throughput changes - When using pivot schemas or JSON data (for example), individual records in a data set may have different schema arrangements. We predict the throughput of the fields and alert if a field begins appearing a lot (surge) or very little (drop). In the case of no throughput, we may alert to a missing field (which can also appear in structured data such as SQL or CSV sources).

* Categories - With Validator 1.9, we infer categories from dates and apply our distribution alerting on the categories. We also can alert if a new category value appears; otherwise big changes in the categories will be reflected in the distribution.

#### Additional Alerts:

In addition to the configurable alert knobs, Validator will generate alerts for the following:

* Misconfigured gold standard situations.
* Log 'alert' messages pushed from the Validator API from connectors or your API calls (enabling your application to augment the log and alert streams found in the Watchpoint activity)
* Invalid, not parseable, CSV, Parquet, etc files pushed to Validator.


### Data Flows

In private beta, we enable correlation of alerts across linked watchpoints. Contact us for more information.



_Patents pending._
