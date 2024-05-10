# Addressing 
![image](https://github.com/brahmbeyond/Notes-App/assets/65112908/10593620-48b2-4f83-988c-6ea3e3c83e41)

subnet /ip adress /interface 
https://youtu.be/OqsXzkXfwRw?si=tOrFredXi8c-7rdJ

subnetting - https://youtu.be/ecCuyq-Wprc?si=qOfZXqQbhsfi8rO5

![image](https://github.com/brahmbeyond/Notes-App/assets/65112908/aa3f7ff4-ec3e-48d9-94d5-2ac3390f9473)


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



https://youtu.be/aor29pGhlFE?si=qK7FWy56xBFNBaDL   = linus

IPv6 why not beigns used -

-  https://hostio.solutions/blog/why-isnt-everyone-using-ipv6-yet/#:~:text=IPv6%20was%20not%20designed%20to%20be%20IPv4%20compatible,that%20each%20IPv6%20address%20needs%20an%20IPv4%20address.

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


**Network Address Translation (NAT)** is a service that enables private IP networks to use the internet and cloud. Let me break it down for you:

1. **Purpose of NAT**: When devices within a private network (like your home or office network) want to communicate with the internet, they need a public IP address. However, there are usually more devices in the private network than available public IP addresses. NAT solves this problem by translating private IP addresses to a single public IP address before sending data outside the network.

2. **How NAT Works**:
   - Imagine you have several devices (computers, smartphones, etc.) connected to your home Wi-Fi. Each of these devices has a private IP address (e.g., 192.168.1.2, 192.168.1.3, etc.).
   - When any of these devices wants to access a website (e.g., www.example.com), NAT steps in:
     - The device's private IP address is replaced with the router's public IP address (the one assigned by your internet service provider).
     - The router keeps track of which internal device made the request.
     - The router sends the request to the external server (www.example.com) using its own public IP address.
     - When the server responds, the router uses its tracking information to forward the response to the correct internal device.
   - This way, multiple devices share the same public IP address, and the internet sees them as a single entity.

3. **Security Aspect**:
   - NAT acts as a security feature by hiding internal private networks from public networks. Without NAT, external public IPs cannot directly communicate with internal private IP hosts.
   - By separating public and private networks, NAT helps reduce security risks.
   - Organizations can implement additional security layers alongside NAT to block threats and protect against malicious activity.

4. **Transition to IPv6**:
   - While IPv6 provides a large address space, many networks still rely on IPv4.
   - NAT allows coexistence by enabling communication between IPv6-only and IPv4-only devices.
   - Organizations can connect IPv6 and IPv4 networks using NAT64 translations.

5. **Carrier-Grade NAT (CGN)**:
   - For large-scale networks (such as service providers), CGN handles millions of NAT translations.
   - CGN helps manage the limited supply of IPv4 addresses.
   - NAT444 architecture is sometimes used in CGN scenarios, allowing customer connections to pass through three different IPv4 addressing domains: the customer's private network, the carrier's private network, and the public internet¹³.

Remember, NAT plays a crucial role in allowing our devices to communicate with the vast internet while maintaining security and efficient resource utilization. 🌐🔒

Source: Conversation with Bing, 10/5/2024
(1) What Is Network Address Translation (NAT)? - Cisco. https://www.cisco.com/c/en/us/products/routers/network-address-translation.html.
(2) Network Address Translation (NAT) - GeeksforGeeks. https://www.geeksforgeeks.org/network-address-translation-nat/.
(3) Network Address Translation Definition | How NAT Works .... https://www.comptia.org/content/guides/what-is-network-address-translation.


