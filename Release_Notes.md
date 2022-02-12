### 1.4.2 (Feb 12, 2022)
GUI:
* New dashboard page providing a summary of all watchpoints.
* New free trial welcome panel.
* Fixed cohesion graph rendering issues, especially when cohesion is very tight.

Backend:
* Enhanced automatic internal state backups
* Push connector errors up to alerts/GUI.


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
