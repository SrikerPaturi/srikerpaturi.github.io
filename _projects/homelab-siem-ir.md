---
title: "Homelab — SIEM Detections & Incident Workflow"
excerpt: "ELK/Wazuh pipeline, detections for auth anomalies and suspicious processes, plus an IR mini runbook."
date: 2025-09-30
tags: [SIEM, ELK, Wazuh, IR, Detections]
---

## Stack
Filebeat → Elasticsearch → Kibana (or Wazuh), test Windows host, Linux server.

## Detections
- Multiple failed logons → success sequence (probable brute force)  
- New admin user creation on workstation  
- Suspicious process tree (script interpreters spawning network tools)

## What I Did
- Built ingest pipeline, index patterns, dashboards.  
- Auth + process rules with thresholds and suppression.  
- **IR Mini-Runbook** with triage, containment, owner handoffs.

## Artifacts
- [Sample Detections (YAML)](/assets/resources/siem-detections.yaml)  
- [IR Mini-Runbook (PDF)](/assets/resources/ir-mini-runbook.pdf)  
- Dashboard screenshots in `/assets/img/homelab/`
