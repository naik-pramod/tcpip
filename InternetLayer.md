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