# SIEM-Implementation-and-SSH-Log-Analysis


## Objective

This lab focuses on developing practical skills in log analysis and threat detection with security monitoring tools. The goal is to take in and analyze system logs. Participants will identify failed login attempts, spot potential brute-force attacks caused by repeated authentication failures, track successful logins, and find suspicious connections that happen without proper authentication.

### Skills Learned

- Log ingestion and parsing using security monitoring tools
- Analyzing authentication logs to identify failed login attempts
- Detecting brute-force attacks through patterns of repeated failures
- identifying suspicious, unauthenticated connection attempts
- Recognizing indicators of compromise (IOCs) in log data
- Developing a security analyst mindset through real-world scenarios
### Tools Used

- Splunk – Log ingestion, parsing, and security event analysis
- SSH – Remote access protocol analyzed for login activity

## Steps

   Step 1- Analyzed Event Types Stats by Numbers of Event going Most to Least
 <img width="1698" height="918" alt="Screenshot 2026-04-07 192040" src="https://github.com/user-attachments/assets/f393e9d7-2733-4323-b74d-66b21cc5472c" /> 

 
    Step 2 -Analyze Failed Login Attempts categorize events by type, helping identify failed logins, brute-force attempts, successful access, and suspicious unauthenticated connections.
<img width="1696" height="944" alt="Screenshot 2026-04-07 192904" src="https://github.com/user-attachments/assets/932ce411-808c-4fc5-8fea-d69e928e5637" />
     
    
       Made the stats into a Graph for to better see Patterns and see login anomaly detection
<img width="1705" height="925" alt="Screenshot 2026-04-07 193015" src="https://github.com/user-attachments/assets/2e2b9b0a-ca1d-4395-8d28-5f2b06c1b04c" />

       Step 3- Looked into event_types that were Multiple Failed Login Attempts to find IPs with Suspicious Attempts
       
<img width="1771" height="966" alt="Screenshot 2026-04-07 193830" src="https://github.com/user-attachments/assets/54a5d9eb-73ba-445b-8aa1-05092a116bfa" />

        Step 4- Made a Alert for Multiple Failed Login Attempts So when it happens makes a alert 
        
<img width="1774" height="935" alt="Screenshot 2026-04-07 193927" src="https://github.com/user-attachments/assets/3879a35a-16e9-4207-a39d-804e811cb750" />

       Step 5- Looked into Successful SSH logins to see if the same ip addresses that Failed got Access 

  <img width="1714" height="875" alt="Screenshot 2026-04-07 194239" src="https://github.com/user-attachments/assets/f7af1019-5346-488f-9392-477c2026a746" />

        Step 6- Made new dashboard for Successful login in attempts 
       
<img width="1744" height="858" alt="Screenshot 2026-04-07 194411" src="https://github.com/user-attachments/assets/68461f9d-4e57-445a-8668-0ea47cc3cce5" />

        Step 7- Looked at event_types that connected without Authentication to see if the same ips are also having multiple failed login attempts 

<img width="1727" height="877" alt="Screenshot 2026-04-07 194527" src="https://github.com/user-attachments/assets/22e3648e-0f57-43fa-9e16-66cd861c20ba" />

         Looked at the time that the connection without authentication happened 

<img width="1712" height="884" alt="Screenshot 2026-04-07 194622" src="https://github.com/user-attachments/assets/497e8563-3028-4d48-8442-153e550be7ac" />


