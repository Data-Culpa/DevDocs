# Demo Mode

Data Culpa Validator offers two ways get up and running and testing alerts rapidly.

## Instant Training

You can load historical data using the Instant Training feature, which enables backdating of data, as directed by the data. You can backdate by "seconds ago from now" in API calls and Validator will slot the data into truncated day slots.

Instant Training data must be loaded from oldest to newest. The built-in Snowflake and BigQuery connectors support Instant Training. The open source MongoDB connector does as well, and by default will extract dates from the MongoID on fields.

Your own connectors can do this too; you can leverage the "mod time" on files or other heuristics.

Once four days of data are loaded, Validator will begin calculating alerts and issueing back-dated alerts.


## Demo Mode

_Coming in 1.5.0_

Demo Mode can be configured in the Alerts configuration dialog per watchpoint. When enabled, Data Culpa Validator will treat successive sessions as different days of data and alarm once four sessions of data have been loaded.



