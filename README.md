# SOC Network Security Monitoring Lab

A hands-on Security Operations Center (SOC) network monitoring lab built using Kali Linux, Snort, Suricata, Zeek, Filebeat, Elasticsearch, and Kibana.

## Project Overview

This project demonstrates how network security telemetry can be collected, analyzed, and visualized in a SOC environment.

## Tools Used

- Kali Linux
- Snort 3
- Suricata
- Zeek
- Filebeat
- Elasticsearch
- Kibana

## Architecture

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
Kibana
↓
SOC Monitoring Dashboard

## Detection

A custom ICMP detection rule was created for the lab environment and tested using ICMP traffic.

The Snort alert was successfully collected and indexed in Elasticsearch.

## Zeek Monitoring

Zeek was used to monitor:

- Network connections
- DNS activity
- Source IP addresses
- DNS queries

## Suricata Monitoring

Suricata was used to generate and analyze network security events and alerts.

## Elasticsearch

Security telemetry from Snort, Suricata, and Zeek was successfully ingested into Elasticsearch.

Example datasets:

- `snort.alert`
- `suricata.eve`
- `zeek.connection`
- `zeek.dns`

## Kibana Dashboard

The Kibana dashboard provides visibility into:

- Zeek network connections
- Zeek DNS activity
- Top DNS queries
- Top source IPs
- Security events by dataset
- Suricata events
- Snort alerts

## Screenshots

Screenshots of the Snort alert and Kibana dashboard are available in the `screenshots/` directory.

## Skills Demonstrated

- Network traffic monitoring
- IDS/IPS concepts
- Security event analysis
- Log ingestion
- SIEM concepts
- Elasticsearch
- Kibana
- Filebeat
- Snort
- Suricata
- Zeek
- Linux command line
- SOC investigation workflow
