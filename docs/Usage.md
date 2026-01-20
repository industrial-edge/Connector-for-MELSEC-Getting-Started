# Usage

- [Usage](#usage)
  - [Read metadata](#read-metadata)
  - [Read data](#read-data)
  - [Write data](#write-data)
  - [Use IIH Essentials](#use-IIH-Essentials)
  
Via the Flow Creator, we can write and read the MELSEC data.

The used flow can be downloaded [here](/src/flow.json) and imported into the Flow Creator, that is running on the same IED as the MELSEC Connector.

## Read metadata

To print out the MELSEC Connector metadata, follow these steps:

- create a mqtt in node
- set the server to 'ie-databus' with port 1883 and corresponding user name/password ('edge'/'edge')
- set the topic to `ie/m/j/simatic/v1/melsec1/dp/r`
- create a debug node and connect to the mqtt in node
- deploy the flow and watch the debug window

![metadata_flow](/docs/graphics/Metadatanode.PNG)

![metadataflowcreator](/docs/graphics/metadatamsg.PNG)

Now you can see the configured datapoint according to the MELSEC settings:

- ***Data_INT*** with unique id **1**
- ***Data_WORD*** with unique id **2**


## Read data

To print out the transfered MELSEC Connector data, follow these steps:

- create a mqtt in node
- set the server to "ie-databus" with port 1883 and corresponding user name/password ('edge'/'edge')
- set the topic to `ie/d/j/simatic/v1/melsec1/dp/r/#`
- create a debug node and connecto to the mqtt in node
- deploy the flow
- as soon as the value for a configured tag changes, you can see it in the debug window

![read_data_flow](/docs/graphics/Readdatamqqtin.PNG)

Since the read payload only contains the tag ID and not the tag name, you need to assign the tag ID according to the metadata. Here the parameter ***Data_INT*** (tag ID **1**) is incremented automatically by the PLC, so we can read each single value:

![Datapoints](/docs/graphics/datapintpayload.PNG)

## Write data

To write some data on the MELSEC tag, you must fetch the tag ID from metadata payload based on the tag name. Here we want to write to the parameter ***Data_WORD*** (tag ID **2**). Please follow these steps:

- create an inject node with this JSON payload: `{ "vals": [ { "id": "2", "val": "111" } ] }`
- create a mqtt out node
- set the server to 'ie-databus' with port 1883 and corresponding user name/password ('edge'/'edge')
- set the topic to `ie/d/j/simatic/v1/melsec1/dp/w/IQR/1000ms`
- connect the inject node to the mqtt out node
- deploy the flow
- click the inject button, to write the value

![writedata](/docs/graphics/writedatamqtti.PNG)

![payload](/docs/graphics/writedatadebug.PNG)

## Use IIH Essentials

The app IIH Essentials collects the data out of different connectors and stores it for a defined time period. This is a prerequisite for other apps like Performance Insight.

To activate the data transfer from the MELSEC Connector, proceed as following:

- open the IED web interface
- open the app IIH Essentials
- select the settings button and enter the user name and the password for the Databus user 'edge' and 'edge'

![DatabusEIP](/docs/graphics/IIHessentialsdatabus.PNG)

- go to tab 'Connectors' and select 'MELSEC Connector'
- activate the adapter and save

![EIPIIH](/docs/graphics/Activateadapter.PNG)


- go to tab 'Manage data' and add the asset 'IQR'

![Assetsandstructure](/docs/graphics/AddassetIIHessentials.PNG)

- add the Attributes that were configured within the MELSEC Connector
  
![IIHesentialsoverview](/docs/graphics/Addatributes.PNG)


- data is now collected by the IIH Essentials and can be used by further apps

