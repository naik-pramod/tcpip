### The Internet Layer

On a routed network, it is not possible to deliver data by physical address. 
The discovery procedures required for delivering by physical address do not work across a router interface. 
Even if they did work, delivery by physical address would be cumbersome because the permanent physical address built in to a network card does not allow you to impose a logical structure on the address space

TCP/IP therefore makes the physical address invisible, and instead organizes the network around a logical, hierarchical addressing scheme.
 This logical addressing scheme is maintained by the IP protocol at the Internet layer. 
 The logical address is called the IP address. 
 
 Another Internet layer protocol called Address Resolution Protocol (ARP) assembles a table that maps IP addresses to physical addresses. 
 This ARP table is the link between the IP address and the physical address associated with the network adapter card.

 ![tcponrouted](/images/tcponrouted.PNG "tcponrouted")

On a routed network, the TCP/IP software uses the following strategy for sending data on the network:

 1. If the destination address is on the same network segment as the source computer, the source computer sends the packet directly to the destination. The IP address is resolved to a physical address using ARP, and the data is directed to the destination network adapter.

2. If the destination address is on a different segment from the source computer, the following process begins:

2.1 The datagram is directed to a gateway. 
 A gateway is a device on the local network segment that is capable of forwarding a datagram to other network segments.
 The gateway address is usually defined through the TCP/IP configuration. If you set up an Internet account with a static IP address through an Internet service provider, the provider will tell you what address to use for the gateway. 
 The gateway address is resolved to a physical address using ARP, and the data is sent to the gateway’s network adapter.

2.2 The datagram is routed through the gateway to a higher-level network segment, where the process is repeated. If the destination address is on the new segment, the data is delivered to its destination. If not, the datagram is sent to another gateway.

2.3 The datagram passes through the chain of gateways to the destination segment, where the destination IP address is mapped to a physical address using ARP and the data is directed to the destination network adapter.