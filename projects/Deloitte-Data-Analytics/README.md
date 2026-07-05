# Deloitte Data Analytics Virtual Experience (Forage)
## Forensic Technology and Operational Performance Optimization

This repository contains the deliverables and analytical models built during the Deloitte Data Analytics Virtual Experience simulation on Forage. The project spans two distinct domains: industrial telemetry diagnostic mapping and workforce compensation compliance audits.

## Project 1: Factory Telemetry Analysis (Tableau)
### Objective
To analyze global manufacturing logs across four distinct Daikibo production plants to identify persistent operational bottlenecks and reduce costly machine downtime.

### Key Insights
* Primary Bottleneck: Isolated 480 minutes of total downtime to a single facility, daikibo-factory-seiko.
* Root Cause Diagnostics: Discovered that downtime was completely localized within LaserWelder structural components rather than being evenly distributed across device classifications.
* Interactive Tooling: Designed and deployed a dynamic dashboard featuring filter actions that allow leadership to drill down from high-level operational metrics to asset-level failure records in one click.

---

## Project 2: Workforce Pay Equality Tracking (Excel)
### Objective
To build an automated screening model for HR compliance data that checks compensation gaps across various operational job roles and automatically highlights potential discrimination risks.

### Logic Framework
The classification parameters evaluate the absolute difference from the ideal score, where 0 represents parity:
* Fair: Within a variance of 10 or less
* Unfair: Variance between 10 and 20
* Highly Discriminative: Extreme variance exceeding 20

### Technical Implementation
* Symmetric absolute tracking via ABS formulas:
  ```excel
  =IFS(ABS(C2)<=10,"Fair",ABS(C2)>20,"Highly Discriminative",TRUE,"Unfair")
