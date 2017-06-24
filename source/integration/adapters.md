title: Adapters
description: Declaring how to search, fetch and interact with specific domains
---
Adapters can be written for a range of domain specific devices, protocols, databases, applications and network services. Each adapter will typically fall into a protocol family. The range of protocols is fully extensible but some common classes of Adapters include.
- HTML - Interacting and fetching information from Open Data Sources and Web Sites
- HTTP - Interfacing to RESTful APIs using Hypertext Transfer Protocol
- JSON-RPC - Network services supporting stateless, light-weight remote procedure calls
- BACnet - Building Automation and Control (BAC) network
- OPC - OLE for Process Control
- Modbus - a serial communication protocol developed by Modicon
- AMQP - Advanced Message Queuing Protocol
- ESB - Enterprise Service Bus
- SQL - Structured Query Language
- NoSQL - non relational stores including document, graph, key-value and column stores 

As many of these protocols are quite generic, it is possible to create an Adapter instance which maximises the integration for a specific domain. This lifts the level of integration above the technical protocol used to communicate. The intent is to extract as much understanding as possible from any exchange, given a specific shared domain knowledge.

The requesting, fetching, parsing and storing of information is typically domain specific. An `Adapter` is used to define how to perform these activities for a given domain and URL template. When registering an `Adapter` the functions to perform these activities are defined.
- registerAdapter ::
