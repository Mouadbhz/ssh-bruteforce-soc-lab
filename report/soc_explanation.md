# SOC Analysis Explanation – SSH Brute Force Detection

## 1. Objective
The objective of this lab is to simulate a real-world SSH brute-force attack and detect it using a SIEM system (Splunk).

## 2. Attack Scenario
A Kali Linux machine was used to perform SSH login attempts against an Ubuntu server using both manual login attempts and Hydra brute-force tool.

## 3. Log Generation
All authentication logs are generated on the Ubuntu machine in:
- /var/log/auth.log

These logs include:
- Failed password attempts
- Invalid user attempts
- Authentication failures

## 4. SIEM Analysis (Splunk)
Logs were ingested into Splunk and analyzed using search queries:

- Failed password detection
- Invalid user detection
- Time-based attack visualization

## 5. Detection Logic
Brute-force activity is identified by:
- High frequency of failed login attempts
- Repeated authentication failures from the same source IP
- Presence of invalid user attempts

## 6. Results
The attack was successfully detected in Splunk dashboards showing:
- Spike in authentication failures
- Continuous login attempts over short time period
- Source IP identified as Kali machine

## 7. Conclusion
This lab demonstrates how SIEM tools like Splunk can detect SSH brute-force attacks in real time by analyzing authentication logs and identifying abnormal login behavior.
