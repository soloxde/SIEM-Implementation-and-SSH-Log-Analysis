# SIEM Implementation and SSH Log Analysis

![Splunk](https://img.shields.io/badge/Splunk-000000?style=flat&logo=splunk&logoColor=white)
![SSH](https://img.shields.io/badge/SSH-Log%20Analysis-blue)
![Category](https://img.shields.io/badge/Category-Blue%20Team%20%2F%20SOC-red)

## Table of Contents
- [Objective](#objective)
- [Skills Learned](#skills-learned)
- [Tools Used](#tools-used)
- [Steps](#steps)
  - [Step 1 – Analyze Event Types by Frequency](#step-1--analyze-event-types-by-frequency)
  - [Step 2 – Analyze Failed Login Attempts](#step-2--analyze-failed-login-attempts)
  - [Step 3 – Identify IPs with Multiple Failed Login Attempts](#step-3--identify-ips-with-multiple-failed-login-attempts)
  - [Step 4 – Create an Alert for Multiple Failed Login Attempts](#step-4--create-an-alert-for-multiple-failed-login-attempts)
  - [Step 5 – Review Successful SSH Logins](#step-5--review-successful-ssh-logins)
  - [Step 6 – Build a Dashboard for Successful Login Attempts](#step-6--build-a-dashboard-for-successful-login-attempts)
  - [Step 7 – Investigate Unauthenticated Connections](#step-7--investigate-unauthenticated-connections)
- [Key Takeaways](#key-takeaways)

## Objective
This lab focuses on developing practical skills in log analysis and threat detection using security monitoring tools. The goal is to ingest and analyze system logs to identify failed login attempts, spot potential brute-force attacks caused by repeated authentication failures, track successful logins, and detect suspicious connections that occur without proper authentication.

## Skills Learned
- Log ingestion and parsing using security monitoring tools
- Analyzing authentication logs to identify failed login attempts
- Detecting brute-force attacks through patterns of repeated failures
- Identifying suspicious, unauthenticated connection attempts
- Recognizing indicators of compromise (IOCs) in log data
- Developing a security analyst mindset through real-world scenarios

## Tools Used
- **Splunk** – Log ingestion, parsing, and security event analysis
- **SSH** – Remote access protocol analyzed for login activity

## Steps

### Step 1 – Analyze Event Types by Frequency
Reviewed event type statistics, sorted from most to least occurrences, to get an overview of overall log activity.

<img width="800" height="800" alt="Screenshot 2026-04-07 192040" src="https://github.com/user-attachments/assets/f393e9d7-2733-4323-b74d-66b21cc5472c" />

### Step 2 – Analyze Failed Login Attempts
Categorized events by type to help distinguish failed logins, brute-force attempts, successful access, and suspicious unauthenticated connections.

<img width="800" height="800" alt="Screenshot 2026-04-07 192904" src="https://github.com/user-attachments/assets/932ce411-808c-4fc5-8fea-d69e928e5637" />

Converted the stats into a graph to better visualize patterns and support login anomaly detection.

<img width="800" height="800" alt="Screenshot 2026-04-07 193015" src="https://github.com/user-attachments/assets/2e2b9b0a-ca1d-4395-8d28-5f2b06c1b04c" />

### Step 3 – Identify IPs with Multiple Failed Login Attempts
Investigated event types associated with multiple failed login attempts to identify IP addresses exhibiting suspicious behavior.

<img width="800" height="800" alt="Screenshot 2026-04-07 193830" src="https://github.com/user-attachments/assets/54a5d9eb-73ba-445b-8aa1-05092a116bfa" />

### Step 4 – Create an Alert for Multiple Failed Login Attempts
Configured an alert to trigger whenever multiple failed login attempts occur, enabling faster detection of potential brute-force activity.

<img width="800" height="800" alt="Screenshot 2026-04-07 193927" src="https://github.com/user-attachments/assets/3879a35a-16e9-4207-a39d-804e811cb750" />

### Step 5 – Review Successful SSH Logins
Cross-referenced successful SSH logins against IP addresses that had previously failed authentication, to check whether any of them ultimately gained access.

<img width="800" height="800" alt="Screenshot 2026-04-07 194239" src="https://github.com/user-attachments/assets/f7af1019-5346-488f-9392-477c2026a746" />

### Step 6 – Build a Dashboard for Successful Login Attempts
Created a new dashboard dedicated to tracking successful login attempts.

<img width="800" height="800" alt="Screenshot 2026-04-07 194411" src="https://github.com/user-attachments/assets/68461f9d-4e57-445a-8668-0ea47cc3cce5" />

### Step 7 – Investigate Unauthenticated Connections
Examined event types involving connections made without authentication, to determine whether the same IPs were also responsible for multiple failed login attempts.

<img width="800" height="800" alt="Screenshot 2026-04-07 194527" src="https://github.com/user-attachments/assets/22e3648e-0f57-43fa-9e16-66cd861c20ba" />

Reviewed the timestamps of these unauthenticated connection attempts to identify any timing patterns.

<img width="800" height="800" alt="Screenshot 2026-04-07 194622" src="https://github.com/user-attachments/assets/497e8563-3028-4d48-8442-153e550be7ac" />

## Key Takeaways
- Splunk's stats and visualization tools make it straightforward to spot brute-force patterns hidden in raw SSH logs.
- Correlating failed logins, successful logins, and unauthenticated connections by IP is an effective way to flag indicators of compromise.
- Automated alerting on repeated authentication failures shortens the time between an attack starting and an analyst noticing it.
