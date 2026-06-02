# Intro to LAN

LAN stands for Local Area Network : it is a set of locally / physically connected devices, sharing a common network.

## LAN topologies

There are three LAN topologies :

* Bus topology:  each device is connected to a single cable (the "backbone") where data travels from left to right
* Ring topology: each device is connected to exactly two other devices, and the data travels from one device to another, sequentially ; data travels in a single direction and a device can receive data only if it has no data to send
* Star topology: every device is connected to a central device, a "switch" or a "hub" for example

Devices are connected to a switch through ports (they come in power of 2: 4, 8, ... up to 64); the switch retains a map of the ports where each device is connected, making it more efficient than hubs or repeaters.

Finally, a router is a device that connects multiple networks: routing (passing the data) can be difficult as there can be many paths leading from a network to another !

## Primer on subnetting

Is is possible to subdivide a network in subnets. We use IP addresses to separate subnets:

* the network address: the start of the subnet (e.g. 192.168.1.0)
* the host address:    the address of a device on the subet (e.g. 192.168.123)
* the default gateway: the address of a special device on the network that can send information to another network (usually the first or last IP address on the subnet, i.e 192.168.1.1 or 192.168.1.255)

## ARP

ARP stands for Address Resolution Protocol. Each device has two addresses : a physical identifier, the MAC address, and a logical identifier, the IP address. When devices communicates, they need to resolve the physical identifier from the logical identifier.

Typically, a device will broadcast an *ARP request* on the network such as "Who has IP address 192.168.1.29 ?"; only the device with such IP address will answer with an *ARP reply* like "I have IP address 192.168.1.29, here is my MAC address AC:01:33:D3:88:31"

## DHCP

DHCP stands for Dynamic Host Configuration Protocol. It is used when connecting a device to a network :

1) DHCP Discover: if the device has not been manually assigned an IP address, it sends a request on the network trying to reach out a DHCP server
2) DHCP Offer:    the DHCP server responds with an IP address for the device to use
3) DHCP Request:  the device replies to the server, confirming the use of the IP address
4) DHCP ACK:      the DCHCO server acknowledges the use of the IP address by the device

