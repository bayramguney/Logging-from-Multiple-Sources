# Logging-from-Multiple-Sources

# Packet Tracer Lab – Logging from Multiple Sources

## Overview
This lab demonstrates how multiple network monitoring technologies work together to provide visibility into network activity. Using Cisco Packet Tracer, I captured and analyzed **Syslog**, **AAA Accounting (TACACS+)**, and **NetFlow** data to monitor device events, user authentication, and network traffic.

## Objectives
- Configure and observe Syslog logging from multiple network devices.
- Monitor user authentication using AAA Accounting.
- Capture and visualize network traffic with NetFlow.

## Technologies Used
- Cisco Packet Tracer
- Syslog
- AAA (Authentication, Authorization, and Accounting)
- TACACS+
- NetFlow
- EIGRP
- Cisco IOS CLI

## Tasks Performed

### Part 1 – Syslog Logging
- Enabled the Syslog service on the Syslog Server.
- Generated debug-level EIGRP messages using:
  ```bash
  debug eigrp packets
  ```
- Verified that routers, switches, and the firewall sent log entries to the Syslog Server.
- Observed Syslog severity levels and remote logging functionality.

**Information displayed in Syslog messages included:**
- Timestamp
- Device hostname
- Severity level
- Logging facility
- Interface or protocol information
- EIGRP packet events
- Debug message details

### Part 2 – AAA Accounting
- Logged into R2 using TACACS+ authentication.
- Username:
  ```
  analyst
  ```
- Password:
  ```
  cyberops
  ```
- Verified AAA Accounting records on the Syslog Server.

**AAA log entries included:**
- Username
- Login status (successful authentication)
- Device accessed
- Login time/date
- Authentication method
- Session information

After issuing the `logout` command, the AAA Accounting window recorded the user logout and updated the session record to indicate the session had ended.

### Part 3 – NetFlow Monitoring
- Opened the NetFlow Collector on the Syslog Server.
- Generated traffic by pinging the Corporate Web Server.
- Observed NetFlow statistics and traffic visualization.
- Verified that the firewall exported flow information to the NetFlow Collector.

## Skills Demonstrated
- Centralized Syslog monitoring
- Cisco IOS debugging
- Remote logging analysis
- AAA authentication and accounting
- TACACS+ user logging
- NetFlow traffic monitoring
- Basic network security monitoring
- Network traffic analysis

## Key Takeaways
- Syslog centralizes log messages from multiple network devices for easier monitoring and troubleshooting.
- AAA Accounting records user authentication and session activity for auditing and security.
- NetFlow provides detailed visibility into network traffic patterns without capturing packet contents.
- Combining Syslog, AAA, and NetFlow creates a comprehensive view of network operations and security events, laying the foundation for SIEM-based monitoring.

---
**Lab Environment:** Cisco Packet Tracer  
**Topics:** Syslog, AAA, TACACS+, NetFlow, Network Monitoring, Cisco IOS, Cybersecurity
