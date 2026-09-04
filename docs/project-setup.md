# SOC Network Security Monitoring Lab - Project Setup



## Overview



This project is a hands-on Security Operations Center (SOC) network monitoring lab built in Kali Linux.



The lab demonstrates how network traffic can be collected, analyzed, detected, forwarded to a centralized platform, and visualized for security monitoring.



## Lab Architecture



Network Traffic

↓

Snort / Suricata / Zeek

↓

Log Files

↓

Filebeat

↓

Elasticsearch

↓

Kibana Dashboard



## Environment



- Operating System: Kali Linux

- Network Interface: eth0

- Lab IP: 192.168.91.128

- Elasticsearch: 9.5.2

- Kibana: 9.5.2

- Filebeat: 9.5.2

- Suricata: 8.0.6

- Zeek: Source-built



## Security Monitoring Tools



### Snort



Snort was configured as a network intrusion detection system (NIDS).



A custom lab rule was used to generate a controlled ICMP alert for testing.



### Suricata



Suricata was used for network intrusion detection and network security event logging.



Suricata EVE JSON logs were collected and forwarded to Elasticsearch using Filebeat.



### Zeek



Zeek was used for network security monitoring and network telemetry.



Zeek generated connection and DNS logs that were collected by Filebeat.



### Filebeat



Filebeat collected security telemetry from:



- Zeek

- Suricata



The logs were forwarded to Elasticsearch.



### Elasticsearch



Elasticsearch stored and indexed the collected security telemetry.



The data included Zeek, Suricata, and Snort-related security events.



### Kibana



Kibana was used to search, investigate, and visualize security telemetry.



A SOC Network Security Monitoring Dashboard was created to display:



- Network connections over time

- DNS activity

- Top DNS queries

- Top source IP addresses

- Security events by dataset

- Suricata events

- Suricata alerts

- DNS response codes



## Testing



Controlled network traffic was generated in the lab using tools such as:



```bash

ping

dig

