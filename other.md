# Addressing 
![image](https://github.com/brahmbeyond/Notes-App/assets/65112908/10593620-48b2-4f83-988c-6ea3e3c83e41)

subnet /ip adress /interface 
https://youtu.be/OqsXzkXfwRw?si=tOrFredXi8c-7rdJ

subnetting - https://youtu.be/ecCuyq-Wprc?si=qOfZXqQbhsfi8rO5

# NEWORK LAYER PROTOCOLS
### Address Resolution Protocol(ARP)
While communicating, a host needs Layer-2 (MAC) address of the destination machine which belongs to the same broadcast domain or network. A MAC address is physically burnt into the Network Interface Card (NIC) of a machine and it never changes.

On the other hand, IP address on the public domain is rarely changed. If the NIC is changed in case of some fault, the MAC address also changes. This way, for Layer-2 communication to take place, a mapping between the two is required.

To know the MAC address of remote host on a broadcast domain, a computer wishing to initiate communication sends out an ARP broadcast message asking, “Who has this IP address?” Because it is a broadcast, all hosts on the network segment (broadcast domain) receive this packet and process it. ARP packet contains the IP address of destination host, the sending host wishes to talk to. When a host receives an ARP packet destined to it, it replies back with its own MAC address.

Once the host gets destination MAC address, it can communicate with remote host using Layer-2 link protocol. This MAC to IP mapping is saved into ARP cache of both sending and receiving hosts. Next time, if they require to communicate, they can directly refer to their respective ARP cache.

Reverse ARP is a mechanism where host knows the MAC address of remote host but requires to know IP address to communicate.


### Internet Control Message Protocol (ICMP)
ICMP is network diagnostic and error reporting protocol. ICMP belongs to IP protocol suite and uses IP as carrier protocol. After constructing ICMP packet, it is encapsulated in IP packet. Because IP itself is a best-effort non-reliable protocol, so is ICMP.

Any feedback about network is sent back to the originating host. If some error in the network occurs, it is reported by means of ICMP. ICMP contains dozens of diagnostic and error reporting messages.

ICMP-echo and ICMP-echo-reply are the most commonly used ICMP messages to check the reachability of end-to-end hosts. When a host receives an ICMP-echo request, it is bound to send back an ICMP-echo-reply. If there is any problem in the transit network, the ICMP will report that problem.

### IPv4
Internet Protocol Version 4 is a network layer protocol that addresses and controls information and is used to transport packets in a network. To transport data packets across a network, IP and TCP work together. Each host is given a 32-bit IP address consisting of the network and host ID. The host number identifies a host on the network, assigned by a network administrator, whereas the network number identifies a network and is assigned by the internet. The IP is only responsible for delivering the packets, and TCP(a transport layer protocol) helps put them back in the correct order.

#### **Types of IPv4**

Classful:- In classful IP addressing, some bits are reserved for network ID, and the remaining bits are used to represent the host in the network. The classful IP addressing can be further classified into five classes: class A, class B, class C, class D, and class E.
Classless:- In classless IP, adding the number of network bits and number of host bits is variable and can be modified according to need. Classless addressing avoids the problem of IP address exhaustion that can arise with classful addressing. The format of classless IP addressing is x.u.v.z/n, where n represents the number of network bits.


### IPv6
Internet Protocol Version 6 is the latest version of the Internet Protocol. It is a network layer protocol containing addressing and control information for packet routing. IPv6 was established to address the exhaustion of IPv4. To accommodate more levels of addressing, it raises the IP address size from 32 bits to 128 bits.

IPv6 has introduced Anycast addressing and removed the concept of broadcasting. Devices can self-acquire an IPv6 address and interact within that subnet using IPv6. The Dynamic Host Configuration Protocol (DHCP) servers are no longer reliant on this auto-configuration. The hosts can connect even if the DHCP server on that subnet is down.

IPv6 introduces a new mobility feature. Mobile IPv6-enabled devices can roam without having to change their IP addresses. IPv6 is currently in its early stages of development, but it is expected to totally replace IPv4 in the next years. IPv6 is now used by a small number of networks.

-----





