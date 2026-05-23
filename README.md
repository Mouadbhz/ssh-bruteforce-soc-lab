
# SSH Brute Force Detection using Splunk SIEM

## Overview
This project simulates an SSH brute-force attack using Kali Linux against an Ubuntu machine and analyzes the attack using Splunk SIEM.

## Technologies Used
- Kali Linux
- Ubuntu 24.04
- Splunk Enterprise
- Hydra
- OpenSSH

## Attack Simulation
- SSH login attempts
- Hydra brute-force attack

## Splunk Detection Queries

### Failed Password Attempts
```spl
index=* "Failed password"
```
### Invalid Users
```spl
index=* "Invalid user"
```
### Attack Timeline
```spl
index=* ("Failed password" OR "Invalid user")
| timechart span=30s count
```
