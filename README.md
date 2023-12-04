# Analyze a Packet with Wireshark

## Project Description

As a security analyst, analyzing network traffic is crucial to understanding the types of traffic sent to and from systems on the networks you work with.

### Task 1 - Apply a Basic Wireshark Filter and Inspect a Packet



The filter `ip.addr == 142.250.1.139` is used to filter packets where either the source or destination IP address matches the provided address.

- **Frame:** Contains details about the packet at the Ethernet level, including source and destination MAC addresses and the type of internal protocol.
- **Internet Protocol Version 4 (IPv4):** Provides data about the IP data contained in the Ethernet packet, including source and destination IP addresses and the Internet Protocol (e.g., TCP or UDP).
- **Transmission Control Protocol (TCP):** Provides detailed information about the TCP packet, including source and destination TCP ports, sequence numbers, and TCP flags.

### Task 2 - Use Filters to Select Packets

- `ip.src == 142.250.1.139`: Returns packets that came from 142.250.1.139.
- `ip.dst == 142.250.1.139`: Returns packets that were sent to 142.250.1.139.
- `eth.addr == 42:01:ac:15:e0:02`: Returns packets of traffic to or from a specific Ethernet MAC address.

### Task 3 - Use Filters to Explore DNS Packets

- `udp.port == 53`: Selects UDP port 53 traffic, used for DNS traffic.
  - The website queried can be found under Queries.
  - Answers data includes the queried name and associated addresses.

### Task 4 - Use Filters to Explore TCP Packets

- `tcp.port == 80`: Selects TCP port 80 traffic, the default port associated with web traffic.
  - `tcp contains "curl"`: Filters for packets containing web requests made with the curl command in the sample packet capture file.

## Summary

In this exercise, I learned to open saved packet capture files, view high-level packet data, and use filters to inspect detailed packet data.
