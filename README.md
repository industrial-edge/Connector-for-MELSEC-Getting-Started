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
## Requirements

### Prerequisites

What are the requirements on the user knowledge, HW components before starting the how-to?

### Used components

List the used software and hardware components that were tested with this how-to.
Add the used components here (e.g.)

* Industrial Edge App Publisher V1.0.8
* Docker Engine 18.09.6
* Docker Compose V2.4
* S7 Connector V 1.0.22
* S7 Connector Configurator V 1.0.9
* Industrial Edge Device V 1.0.0-34
* TIA Portal V16
* PLC: CPU 1511 FW 2.8.3

## Installation

How to install/run this application example? (i.e. how to deploy it to Industrial Edge device?) How to build this application? How to set up configurations in IE?

To keep the readme.md file as short as possible please add more detailed information in the docs folder.

* [Build application](docs/Installation.md#build-application)

## Usage

When the app is installed, how can I use it? Usually some basic UI description to prove that the app is working correctly.

## Documentation

Add links to documentation. Either on external URL or in the doc folder. Please use always link to a file not to a directory (it doesn't work with static site generator engines).

Add these links:

You can find further documentation and help in the following links

* [Industrial Edge Hub](https://iehub.eu1.edge.siemens.cloud/#/documentation)
* [Industrial Edge Forum](https://forum.industrial-edge.siemens.cloud)
* [Industrial Edge Documentation](https://docs.industrial-edge.siemens.cloud/)
* [Industrial Edge landing page](https://new.siemens.com/global/en/products/automation/topic-areas/industrial-edge/simatic-edge.html)
* [Industrial Edge GitHub page](https://github.com/industrial-edge)

## Contribution

Thank you for your interest in contributing. Anybody is free to report bugs, unclear documentation, and other problems regarding this repository in the Issues section.
Additionally everybody is free to propose any changes to this repository using Pull Requests.

If you haven't previously signed the [Siemens Contributor License Agreement](https://cla-assistant.io/industrial-edge/) (CLA), the system will automatically prompt you to do so when you submit your Pull Request. This can be conveniently done through the CLA Assistant's online platform.
Once the CLA is signed, your Pull Request will automatically be cleared and made ready for merging if all other test stages succeed.

## License and Legal Information

Please read the [Legal information](LICENSE.txt).

```
TO BE DELETED: Depending on the content of your repository either choose the
- LICENSE.md (In case no Source code is included) or the
- LICENSE.txt file (Source Code is included)
```

## Disclaimer

```
Please add this Disclaimer in case your repository contains a Dockerfile otherwise you can remove the whole section
```

IMPORTANT - PLEASE READ CAREFULLY:

This documentation describes how you can download and set up containers which consist of or contain third-party software. By following this documentation you agree that using such third-party software is done at your own discretion and risk. No advice or information, whether oral or written, obtained by you from us or from this documentation shall create any warranty for the third-party software. Additionally, by following these descriptions or using the contents of this documentation, you agree that you are responsible for complying with all third party licenses applicable to such third-party software. All product names, logos, and brands are property of their respective owners. All third-party company, product and service names used in this documentation are for identification purposes only. Use of these names, logos, and brands does not imply endorsement.
