# MELSEC connector application example

- [MELSEC connector application example](#melsec-connector-application-example)
  - [Description](#description)
    - [Overview](#overview)
    - [General task](#general-task)
  - [Requirements](#requirements)
    - [Prerequisites](#prerequisites)
    - [Used components](#used-components)
    - [PLC project](#plc-project)
  - [Configuration](#configuration)
  - [Usage](#usage)
  - [Documentation](#documentation)
  - [Contribution](#contribution)
  - [Licence and Legal Information](#licence-and-legal-information)
    
## Description

### Overview

This tutorial shows how to use the Industrial Edge applications MELSEC Connector to establish a connection between an Industrial Edge Device (IED) and a 3rd party PLC that supports **MELSEC**. These PLC variants are supported:

* Mithsubhusi FX5U
* Mithsubhusi L02
* Mithsubhusi Q00U
* Mithsubhusi FX3U

The MELSEC Connector is an application that runs on the individual IED. Connections can be configured using the Common Configurator for industrial Edge. The connector transfers the value series of selected data points from a PLC to the Databus. From there the data can be used within other Edge apps, e.g. the Flow Creator.


### General Task

Here we configure a connection to a Mithsubhusi FX5U PLC using the Connector for MELSEC. The data is published on the Databus. By using the application Flow Creator, we fetch the metadata of the MELSEC Connector, write some data on the configured tags and the read out the new data.

![Overview](/docs/graphics/Melsecarchi.PNG)


## Requirements

### Prerequisites

- Access to an industrial Edge Managment (IEM) with onboarded Industrial Edge Device (IED)
- IEM: Installed system configurator for Databus
- IED: Installed system app Databus
- IED: Installed app Connector for Melsec
- IED: Installed app Common Configurator
- IED: Installed app Registry Service
- IED: Installed app Common Import Converter
- IED: Installed app IIH Semantics
- IED: Installed app Flow Creator
- IED: Installed app IIH Essentials (optional)
- IED is connected to the Mithsubhusi FX5U PLC via Ethernet
- GX Works2 project loaded on PLC
- Google Chrome (Version ≥ 72)

### Used components

- Industrial Edge Management (IEMV) V2.4.0-11
- Industrial Edge Device (OS) V2.3.0-13
  - Databus V3.0.1
  - Common Configurator V2.0.1
  - Registry Service V1.11.0-2
  - Connector for MELSEC V1.0.0-0
  - Flow Creator V1.17.1-1
  - IIH Essentials V2.0.1
- PLC: Mithsubhusi FX5U
- GX Works2

### PLC project

The used PLC project *Melsectest.gx3* can be found in the [src folder](/src/).

## Configuration

You can find further information about the following steps in the [Configuration](/docs/Installation.md) documentation:

- [Overview](/docs/Installation.md#overview)
- [Install MELSEC Connector](/docs/Installation.md#install-melsec-connector)
- [Configure Databus](/docs/Installation.md#configure-databus)
- [Configure MELSEC via Common Configurator](/docs/Installation.md#configure-melsec-via-common-configurator)

