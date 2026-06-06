# Extending Your Network

## Introduction to port forwarding

Port forwarding allows to expose a port of a device on the local network to devices outside the network. This is done at the router level.

## Firewalls 101

A firewall's responsibility is to decide what can go in and out of a network:

* Where the traffic is coming from or going to ?
* Which is it headed to ?
* What protocol is used ?

There are two types of firewalls:

* stateless: the firewall inspects individual packets of data
* stateful : the firewall inspects entire connections

## VPN Basics

VPN stands for Virtual private Network. It allows to connect devices on separate local networks via a tunnel on the Internet. Connected devices therefore form their own network, that can't be accessed by other devices (even those on the same local network).

## LAN Networking Devices

Routers operate at layer 3 of the OSI model and connect networks between them, effectively routing data with considerations such as "Which path is the shortest ?" or "Which path is the most reliable ?"

Switch however can operate at both layer 2 and layer 3 of the OSI model but exclusively: there are dedicated layer 2 switches and layer 3 switches. Their job is to connect multiple devices in a network.

What's the difference between these two types of routers ?

Layer 2 routers will only forward frames (layer 2 data) to devices using their MAC addresses.

Layer 3 routers forward frames as well, but can also route packets (layer 3 data) within the network. This allows to create VLAN (Virtual Local Area Networks), which separate devices into groups although they are on the same network. For example, you could have VLAN 1 with base IP address 192.168.1.1 and VLAN 2 with base IP address 192.168.2.1. Devices on VLAN 1 cannot communicate with devices on VLAN 2.
