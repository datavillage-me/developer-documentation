---
layout: default
title: Participants SDK
nav_order: 4
permalink: /sdk
---

# Participants SDK
Software development kit and code snippets for participants of a collaboration space.

## Data provider SDK
There are two different ways to connect data with the Datacage:
- <b>Push</b> approach where the data provider will push the data, encrypted beforehand with the public key received during the verification of the attestation (a flow based on the exchange of symmetric keys is also possible for large datasets).
<i>The push model is recommended for datasets that do <b>not require frequent synchronization</b>.</i>

- <b>Pull</b> approach where the Data Provider will pull the data from the Datacage. The data can be pre-encrypted on the data provider side, but we recommend transport layer security where the mutual authentication certificate is created and verified based on the enclave key.
<i>The pull model is recommended for datasets that <b>do require more frequent synchronization</b>.</i>

These are the `Data provider connectors` currently supported by the platform:
### Enterprise data systems
<br/>
<img classname="testclassname" style="width: 50px" src="assets/images/logo-s3.png">

Connect enterprise data from amazon S3 buckets (Push) 

<img classname="testclassname" style="width: 60px" src="assets/images/logo-azureblob.png">

Connect enterprise data from Azure blob storage (Push) 

### Personal data systems (data vaults)
<br/>
<img classname="testclassname" style="width: 100px" src="assets/images/ess-logo.jpeg">

Connect directly Enterprise Solid Server (Inrupt) from consumers as data provider (Pull) 

<img classname="testclassname" style="width: 50px" src="assets/images/solid-logo.png">

Connect directly Solid Community Server from consumers as data provider (Pull) 

## Code provider SDK
The [Python SDK](https://datavillage-me.github.io/dv-utils/) allows the code provider to quickly write an algorithm that can work and access the functionality of the `Datacage`.

### Development languages and tools
<br/>

<img classname="testclassname" style="width: 50px" src="assets/images/logo-python.webp">

Use Python as development language for the algorithm

<img classname="testclassname" style="width: 50px" src="assets/images/jupyter-logo.png">

Use Notebook to build your algorithm (on sample datasets) 

## Data consumer SDK
The data consumer SDK is under construction.

