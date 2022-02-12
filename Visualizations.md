# Data Culpa Validator Visualizations

This article describes how to interpret the data visualizations provided by Validator.

In the upper left corner of the main screen, there's a drop-down menu listing your active watchpoints. (A watchpoint represents a specific point in a pipeline or a data set in a data warehouse or data lake.)

Pull down the menu and click on the watchpoint you want to view.

The Visualization window opens. Columns on this window represent watchpoint activity on a given day.

Below the column headings listing dates, the Visualization window presents five sections of analytical data, stacked vertically. The sections are:

### Alerts
A list of outstanding alerts per day.

### Throughput
A bar graph reporting number of records processed at this watchpoint per day.

### Cohesion graph
A graph representing the cohesiveness of data analyzed at this watchpoint over time. The tighter the graph, the more consistent the data. Mouse over each node to see more information about that day's data. 

### Values
For numeric data histograms show the distribution of values in a field for the data ingested on a single day. The width of each histogram is normalized based on the maximum value for that field. The vertical access is fixed across the value. For string data, we calculate a propriety complexity measure and present it as a histogram in yellow. The length of the histogram represents the relative complexity of the string. Symbols in circles next to field names identify types.

### Schema
The final section reports the occurrence of fields in the schemas detected at this watchpoint.         

