# OSI Model

OSI Model stands for Open Systems Interconnections Model.

The OSI Model is comprised of seven layers. Data travels through each layer, where some piece of information are added to the original data: this processed is called encapsulation.

## Layer 1 - Physical

Basically, the hardware used to transport data (e.g. ethernet cables).

## Layer 2 - Data link

This layer focuses on the physical addressing of the transmission. It uses the MAC (Media Access Control) addresses of network-enabled devices, burnt into the NIC (Network Interface Card).

## Layer 3 - Network

This layer is responsible for routing, delivering and reassembling packets of data. It only deals in IP addresses. It will find the shortest path between two devices to deliver data using OSPF (Open Shortest Path First) and RIP (Routing Information Protocol).

## Layer 4 - Transport

This layer describes how data is actually transmitted between two devices. Data travels through one of two protocols:

* TCP (Transmission Control Protocol): it delivers data reliably albeit slower
* UDP (User Datagram Protocol)       : it delivers data rapidly but with no guarantee of completeness

## Layer 5 - Session

This layer creates and maintains the connection between two devices exchanging data. It can also "checkpoint" data if there is some loss, in order to request only the missing data.

## Layer 6 - Presentation

This layer describes how data is packed together so that different softwares can handle data the same way, without the need for a "translator".

## Layer 7 - Application

Layer where the end-users applications live, allowing them to read, write, modify or delete data from GUI for examples.


