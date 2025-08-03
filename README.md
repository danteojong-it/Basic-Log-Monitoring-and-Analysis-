# Log Monitoring and Analysis SIEM with Splunk

## Objective

In this project, I installed and configured Splunk Enterprise on a Windows desktop operating system to collect local system event logs. Specifically, I ingested key Windows event logs: Application, Security, and System logs. These logs provide foundational information on system operations, security events, and application behavior, which are critical for monitoring system health and security.


### Skills Learned

- Installed and configured Splunk Enterprise on a Windows desktop environment to collect and manage local system event logs.

- Ingested Windows Application, Security, and System logs into a centralized SIEM platform for efficient monitoring.

- Wrote and refined Search Processing Language (SPL) queries to analyze large volumes of log data effectively.

- Identified and analyzed critical security events, to detect potential unauthorized privileged access.

- Created custom dashboards to visualize security events and present actionable insights to technical and non-technical stakeholders.

- Gained practical experience in incident detection and continuous monitoring of security logs.


### Tools Used

- Splunk Enterprise — for log ingestion, search, analysis, and dashboard creation

- Windows Event Viewer — to manage and clear local Windows event logs during testing

- Windows 11 — the operating system hosting Splunk and generating event logs

- Web Browser (Chrome) — to access and interact with the Splunk web interface

## Startup Configurations

Ref 1: This dashboard was likely custom-built to:

Monitor and analyze Windows Event Logs (e.g., Security, Application, System).

Identify trends like:

Unauthorized logins.

Security-related alerts.

Application errors.

![Filtered Log Search](https://i.imgur.com/unwrWZ9.png)


Ref 2: Cleared Windows Event Viewer logs (Application, Security, and System) prior to ingesting fresh event data into Splunk for a controlled log monitoring and analysis environment.

![Filtered Log Search](https://i.imgur.com/IZj0TUP.png)

## Steps To Follow

Ref 3: First, I performed a broad search (*) to view all incoming events.

![Splunk Dashboard Screenshot](https://i.imgur.com/lmiDd1U.png)

Ref 4-5: Then, I narrowed searches by specific fields such as host, source, and event code. For example, I searched for Event ID (4624, 4674, 5061) which corresponds to "audit log cleared" events. This event is crucial to monitor because it can indicate potentially malicious activity like log tampering or deletion.

![Filtered Log Search](https://i.imgur.com/2fboJW9.png)
![Filtered Log Search](https://i.imgur.com/dj96gra.png)

Ref 6: I created table views to organize the search results for easier interpretation and built a custom dashboard to visualize the event log clearances in real-time.

![Filtered Log Search](https://i.imgur.com/KkPWv4m.png)

Ref 7-8: This custom Splunk dashboard displays security events where special privileges were assigned during a logon. It provides a clear table view of each event, including the timestamp, host, source, and user account involved. Monitoring these events is essential for detecting potential privilege misuse or unauthorized administrative access. This dashboard was created to simplify ongoing visibility into high-privilege logon activity.

![Filtered Log Search](https://i.imgur.com/46nV44r.png)
![Filtered Log Search](https://i.imgur.com/NLBcCFK.png)

Ref 9-12: To make this dashboard easily accessible, I set it as the home dashboard within Splunk. This means it now appears immediately on the main page after logging in, allowing quick visibility into privileged logon events without needing to run manual searches. Setting a custom dashboard as the homepage is a useful feature for streamlining daily monitoring tasks and ensuring that high-priority alerts are front and center.

![Filtered Log Search](https://i.imgur.com/QFkJTFJ.png)
![Filtered Log Search](https://i.imgur.com/OnD8GGA.png)
![Filtered Log Search](https://i.imgur.com/nmgxyCZ.png)
![Filtered Log Search](https://i.imgur.com/1HInLoi.png)
