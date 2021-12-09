### TCP/IP
Transmission Control Protocol/Internet Protocol (TCP/IP) is a protocol system—a collection of protocols that supports network communications.

### A network
A network is a collection of computers or computer-like devices that can communicate across a common transmission medium.

### Network Protocol
A network protocol is a system of common rules that helps define the complex process of network communication.

The protocols of TCP/IP define the network communication process and, more importantly, define how a unit of data should look and what information it should contain so that a receiving computer can interpret the message correctly. 

### TCP/IP Features

The TCP/IP protocol suite addresses the following problems:

- #### Logical addressing
On a LAN, low-lying hardware-conscious protocols deliver data across the physical network using the adapter’s physical address. 
On a basic ethernet network, for example, a computer sends messages directly onto the transmission medium. The network adapter of each computer listens to every transmission on the local network to determine whether a message is addressed to its own physical address.

On large networks, every network adapter can’t listen to every message. (ex Internet).
Network administrators often segment networks using devices such as routers to reduce network traffic. On routed networks, administrators need a way to subdivide the network into smaller subnetworks (called subnets), and impose a hierarchical design so that a message can travel efficiently to its destination. TCP/IP provides this subnetting capability through logical addressing. A logical address is an address configured through the network software. In TCP/IP, a computer’s logical address is called an IP address. 

- #### Routing
A router is a special device that can read logical addressing information and direct data across the network to its destination.
At the simplest level, a router divides a local subnet from the larger network.

![router](/images/router.PNG "router")


TCP/IP includes protocols that define how the routers find a path through the network. 

- #### Name resolution
 The IP address is still designed for the convenience of the computer rather than the convenience of the user.
 TCP/IP, provides for a parallel structure of user-oriented alphanumeric names, called domain names or Domain Name System (DNS) names. 
 This mapping of domain names to an IP address is called name resolution. 
 Special computers called name servers store tables showing how to translate these domain names to and from IP addresses.

- #### Error control and flow control
The TCP/IP protocol suite provides features that ensure the reliable delivery of data across the network.
TCP/IP’s Transport layer defines many of these error-control, flow-control, and acknowledgment functions through the TCP protocol. 
Lower-level protocols at TCP/IP’s Network Access layer also play a part in the overall system of error control.

- #### Application support
Several network applications might be running on the same computer. The protocol software must provide a means for determining which incoming packet belongs with each application. In TCP/IP, this interface from the network to the applications is accomplished through a system of logical channels called ports.
![ports](/images/ports.PNG "ports")