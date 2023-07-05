---
layout: default
title: How Datavillage Works
description: "How Datavillage Works"
---

# How Datavillage Works
In a nutshell, the collaboration owner creates a collaboration space and invites participants as data providers, algorithm providers, or data consumers. Multiple roles can be assumed by a single participant. 
Data providers connect their encrypted data via custom APIs or available data connectors, algorithm providers publish their algorithm via Dockerfile and data consumers consume the result via custom APIs, webhooks or data connectors. 
The Datacage associated with the collaboration space handles the events (batch or real time), executes the algorithm on the decrypted data (only the algorithm can access the data in clear) and the result is made available to data consumers in an encrypted way. The Datacage verifies authorization, consent (if required from individuals) and keeps track of all data activity in an immutable audit trail.

## Overview
![Datavillage overview](../assets/images/datavillage-overview.png)
Data Providers are the organizations that link their data to the collaboration and [<b>Data Connectors</b>](docs/page2.md/#heading2) are how they can connect their data in a fully encrypted way.

Code Providers or Algorithm Providers are the organizations that publish their algorithm in the collaboration and [<b>Algorithm Models</b>](docs/page2.md/#heading2) are examples of typical algorithms (rule-based, AI- and ML-based or knowledge graphs based) running in the confidential environment, being able to handle the events sent to the collaboration and to execute to provide an encrypted result on the combined data of the data providers.

Data consumers are the organizations that get access to the decrypted result of the confidential treatment and can use this result with the guarantee that it has been calculated with the agreement of the participants and in compliance with the regulations.

## Sources for connecting data
You can connect all types of data, personal data, sensitive data or proprietary data.

### Big data

### Zero-party data

### Custom data

