<h1 align="center">Analyze a Packet with Wireshark</h1>

<h2 align="center">Project Description</h2>

<p align="center">As a security analyst, analyzing network traffic is crucial to understanding the types of traffic sent to and from systems on the networks you work with.</p>

<h3 align="center">Task 1 - Apply a Basic Wireshark Filter and Inspect a Packet</h3>

<p align="center"><img src="https://github.com/GeoffreyMorren/Wireshark/assets/152500568/43df6898-761c-4ebf-838f-86637a041764" alt="1a" /></p>

<p align="center">The filter <code>ip.addr == 142.250.1.139</code> is used to filter packets where either the source or destination IP address matches the provided address.</p>

<p align="center"><img src="https://github.com/GeoffreyMorren/Wireshark/assets/152500568/55da0688-1c6c-428a-80f0-ed3ebd9719a2" alt="1b" /></p>

<ul align="center">
  <li><strong>Frame:</strong> Contains details about the packet at the Ethernet level, including source and destination MAC addresses and the type of internal protocol.</li>
  <li><strong>Internet Protocol Version 4 (IPv4):</strong> Provides data about the IP data contained in the Ethernet packet, including source and destination IP addresses and the Internet Protocol (e.g., TCP or UDP).</li>
  <li><strong>Transmission Control Protocol (TCP):</strong> Provides detailed information about the TCP packet, including source and destination TCP ports, sequence numbers, and TCP flags.</li>
</ul>

<h3 align="center">Task 2 - Use Filters to Select Packets</h3>

<p align="center"><img src="https://github.com/GeoffreyMorren/Wireshark/assets/152500568/4837db22-c33b-4a02-8aa0-9458aaaf60ec" alt="2a" /></p>

<ul align="center">
  <code>ip.src == 142.250.1.139</code>: Returns packets that came from 142.250.1.139.
</ul>

<p align="center"><img src="https://github.com/GeoffreyMorren/Wireshark/assets/152500568/8339b1f5-2df5-4c17-8212-9f05262bfdff" alt="2b" /></p>

<ul align="center">
  <code>ip.dst == 142.250.1.139</code>: Returns packets that were sent to 142.250.1.139.
</ul>

<p align="center"><img src="https://github.com/GeoffreyMorren/Wireshark/assets/152500568/5384f66c-f200-4442-ad90-067f54754538" alt="2c" /></p>

<ul align="center">
  <code>eth.addr == 42:01:ac:15:e0:02</code>: Returns packets of traffic to or from a specific Ethernet MAC address.
</ul>

<p align="center"><img src="https://github.com/GeoffreyMorren/Wireshark/assets/152500568/c6d4b1ed-2795-4408-b8a7-61a176342987" alt="2d" /></p>

<h3 align="center">Task 3 - Use Filters to Explore DNS Packets</h3>

<p align="center"><img src="https://github.com/GeoffreyMorren/Wireshark/assets/152500568/dbca9730-9fa4-448a-bcfa-d677da241c35" alt="3a" /></p>

<ul align="center">
  <code>udp.port == 53</code>: Selects UDP port 53 traffic, used for DNS traffic.
</ul>

<p align="center"><img src="https://github.com/GeoffreyMorren/Wireshark/assets/152500568/6764c5af-333a-4e13-bb34-719954cc45f4" alt="3b" /></p>

<ul align="center">
  The website queried can be found under Queries.
  Answers data includes the queried name and associated addresses.
</ul>

<h3 align="center">Task 4 - Use Filters to Explore TCP Packets</h3>

<p align="center"><img src="https://github.com/GeoffreyMorren/Wireshark/assets/152500568/0cd5ed04-7f98-4723-86b9-8642fddb3267" alt="4a" /></p>

<ul align="center">
  <code>tcp.port == 80</code>: Selects TCP port 80 traffic, the default port associated with web traffic.
</ul>

<p align="center"><img src="https://github.com/GeoffreyMorren/Wireshark/assets/152500568/4088618a-cc2c-4985-a381-73ac6b13557a" alt="4b" /></p>

<ul align="center">
  <code>tcp contains "curl"</code>: Filters for packets containing web requests made with the curl command in the sample packet capture file.
</ul>

<h2 align="center">Summary</h2>

<p align="center">In this exercise, I learned to open saved packet capture files, view high-level packet data, and use filters to inspect detailed packet data.</p>
