# Demo Mode

Data Culpa Validator offers two ways get up and running and testing alerts rapidly.

## Instant Training

You can load historical data using the Instant Training feature, which enables backdating of data, as directed by the data. You can backdate by "seconds ago from now" in API calls and Validator will slot the data into truncated day slots.

Instant Training data must be loaded from oldest to newest. The built-in Snowflake and BigQuery connectors support Instant Training. The open source MongoDB connector does as well, and by default will extract dates from the MongoID on fields.

Your own connectors can do this too; you can leverage the "mod time" on files or other heuristics.

Once four days of data are loaded, Validator will begin calculating alerts and issueing back-dated alerts.


## Demo Mode

_1.6.5 and later_

Demo Mode can be configured in the Alerts configuration dialog per watchpoint. When using Demo Mode, Data Culpa Validator will synthesize a baseline of data based on your first day of data loaded, if you do not have more than four days of data available. The synthetic baseline will not show up in the user interface, but is computed "just in time" when checking for alert conditions.

Validator will only synthesize data for sequential alerts (i.e., no synthetic data will be computed for week over week alerting).

Alerts generated with the synthetic data are tagged as "Demo Mode" alerts and the number of days synthesized. The demo mode will be disabled automatically once sufficient real data has been loaded into the watchpoint.

This configuration is per watchpoint.



