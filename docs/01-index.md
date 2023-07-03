---
layout: default
title: Home
description: "Datavillage Documentation"
---

# Datavillage Documentation

Learn how to use Datavillage to combine data with partners and run AI algorithms without disclosing it.

#### Getting started with Datavillage
Learn about Datavillage, setup and run a basic data collaboration, explore features and use cases.



## How can Datavillage help you ?



Datavillage enables organizations to collaborate on data with other organizations and their consumers with privacy. Organizations gain access to sensitive and personal data of other parties while confidentiality and integrity of data and algorithms are guaranteed.
Organizations and consumers can share data without fear of it being misused or of losing their competitive advantage. It’s about <b>sharing without showing</b>.

Datavillage provides the <b><u>D</u>ata <u>C</u>ollaboration <u>P</u>latform</b> implementing privacy by design and automating trusted and transparent insights generation.

Privacy by design is implemented based on end-to-end data encryption and transparent governance:
- Data are encrypted at rest and in transit
- Data are encrypted while beeing processed
- Confidential algorithm is running is a fully sandboxed environment
- Only derived data can be accessed by data consumer
- Consumers are in control of their data and can join collaborations with explicit consent


## Data collaboration spaces
Organizations can create <b>data collaboration spaces</b> involving other organizations and their consumers directly. The participants meet in the confidential environment:
- The <b>data providers</b> that provide the raw data. The data providers can be organizations providing enterprise data or consumers directly connecting zero-party personal data through their data vault. The data is only visible in the secure environment by the trusted algorithm.
- The <b>code provider</b> that provides the algorithm that will run on the data. The code provider describes the algorithm and the output model (ontology) for derived data.
- The <b>data consumers</b> who access the results of the algorithm (derived data). Only data consumers can access the result from the confidential environment. Consumers get result directly in their personal data vault.

As illustrated in the diagram below, a participant can have several roles.

![](assets/images/collaboration-space.png)

## End-to-end confidentiality
End-to-end confidentiality guarantees each participant a <b>complete level of control and transparency</b> over the collaboration:
- The <b>identity</b> of each participant both organizations and consumers is known and validated
- The <b>data</b> can only be accessed in the confidential environment by the approved code. Personal data are stored in the data vault of consumers.
- Only the <b>derived data</b> (results) can leave the confidential environment by the authorized participant
- The <b>purpose</b> of the collaboration is validated by each participant including consumers via their explicit consent
- The <b>attestation</b> that the confidential environment is indeed a trusted environment and complies with the requirements
- The confidential environment, also called `Datacage`, operates on TEE enclaves, sanboxed via micro-firewalls.