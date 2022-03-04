### Upcoming:
* Alert confirmation button for training.
* Improved alert configuration parameters.
* "Run now" button for in-product controlled data.
* Improved data prediction... :-)
* And much more :-)

### 1.5.0 (Mar 3, 2022)
Alerts:
* Improved alert wording, clarifying many aspects of the alerts.
* Significant improvements to alert thresholding and sensitivity to noise.
* Fixed bugs with duplicate data detection.

GUI:
* Fixed sankey schema rendering bug when rendering an "empty time" period.
* Fixed a number of bugs and error paths with the BigQuery wizard.
* Fixed a number of small nits.

Backend:
* Improved logging from fastcols processing.
* Implemented multi-streaming for watchpoints, enabling multiple concurrent streams into a single endpoint.
* Implemented timeout configuration for watchpoints (and associated GUI).
* Improved time to detect new data for trial installations.
___

### 1.4.6 (Feb 17, 2022)
GUI:
* Fix schema bubble sizing to start its scale at 0, so the bubbles are more clearly comparable.
* Fix bug with week-over-week alert configuration.
* Fix context/stage label mismatch on watchpoints.

Backend:
* Adjust garbage collection behavior.
___

### 1.4.2 (Feb 12, 2022)
GUI:
* New dashboard page providing a summary of all watchpoints.
* New free trial welcome panel.
* Fixed cohesion graph rendering issues, especially when cohesion is very tight.

Backend:
* Enhanced automatic internal state backups
* Push connector errors up to alerts/GUI (mostly an issue with FastCols-enabled connectors).
___

### 1.4.0 (Jan 25, 2022)
GUI:
* Add archive pipeline UI and backend support.
* Fixed location of alert icons on watchpoint view.
* Added tooltip to alert icons.

Instant Training:
* Enhanced events and alerts support with Instant Training.
* Improve alerts display for the displayed time period on the main watchpoint view.
* Add Instant Training support to BigQuery built-in connector.

Backend:
* Garbage collection for data caches.
* Fixed bug in clearing events/alerts that was over aggressive in updating cleared timestamps.
* Fix alerts when no pipeline activity.
* Fix a "data tearing" issue when collapsing sessions with certain types of sparse data.
* Improve error reporting when things go wrong from built-in BigQuery connector.


_Older release notes are archived; available upon request._
