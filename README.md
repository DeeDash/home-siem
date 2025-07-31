# Home SIEM: ELK + BlackArch + Python Threat Hunting

A full-stack SIEM system for home environments, running on BlackArch and powered by the ELK stack and a Python-based threat hunting module using an MCP server for modular intelligence.

## Features:

* Full ELK stack (Elasticsearch, Logstash, Kibana) for log aggregation and visualization
* Python-based threat hunting plugin with modular control via an MCP server
* Real-time monitoring of:
    * 2 wireless networks
    * 8 endpoints (Windows, Linux, Android, Raspberry Pi honeypot)
* Integration with:
    * Vulnerability feeds (e.g. CVE/NVD)
    * Adversarial datasets (MITRE ATT&CK, Caldera, APT reports)
    * Custom signature and IOC databases

## Architecture:
Wireless Networks -> BlackArch Host (ELK + MCP + Plugins)
├─ Threat Hunter (Python)
├─ Logstash Pipelines
├─ Kibana Dashboard
└─ MCP Server
└─ Endpoints (Windows, Linux, Android)

## Threat Intelligence Features:

* IOC scanning and signature matching
* Passive scanning and anomaly detection
* Sigma rule correlation
* Ingests threat feeds:
    * CVE/NVD API
    * OSINT sources
    * Adversarial datasets (MITRE Caldera, APTs)

## Dashboards via Kibana:

* Endpoint Activity Overview
* Suspicious Authentication Events
* IOC Matches Timeline
* MITRE ATT&CK Technique Mapping
* CVE Vulnerability View

## Monitored Devices:

* 3 Linux workstations
* 2 Windows 10 clients
* 2 Android mobile devices (via syslog agent)
* 1 Raspberry Pi honeypot

## Roadmap:
* Integrate Zeek for deeper packet inspection
* Add ML-based anomaly detection
* Build a Web UI for MCP control
* Create deployable agents for endpoints

## References:

* **BlackArch Linux:** https://blackarch.org/
* **Elastic Stack:** https://www.elastic.co/elk-stack
* **MITRE ATT&CK:** https://attack.mitre.org/
* **Sigma Rules:** https://sigmahq.io/
