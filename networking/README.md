# Networking

- [Networking](#networking)
  - [What is Networking?](#what-is-networking)
    - [Public IP](#public-ip)
    - [Private IP](#private-ip)
    - [Latency](#latency)
    - [Throughput](#throughput)
  - [Questions](#questions)

## What is Networking?

TODO

### Public IP

[Wikipedia](): "A public IP address, in common parlance, is a globally routable unicast IP address, meaning that the address is not an address reserved for use in private networks"

From system design perspective, when you have a resources or a component, you would like everyone to be able to access to, whether for direct communication (like a web server) or as a gateway for other components (like a load balancer), you should use a public IP

### Private IP

Whenever you DON'T want users to be able to globally interact with a certain component or resource, you should use a private IP address. Few examples:

  * Web servers that only the load balancer should communicate with them directly and not the users/clients themselves
  * Internal servers that users outside the organization shouldn't access

Private IPs, as opposed to public IPs, don't have to be unique and each separate network, can use the same addresses (because it's private :) )

### Latency

The time it takes to perform a certain task/action

### Throughput

The number of tasks/actions per unit of time


### DNS (Domain Name System)

Definition:
DNS translates human-readable domain names (e.g., www.example.com) into IP addresses (e.g., 192.0.2.1). This system enables users to access resources on the internet using easy-to-remember names rather than numerical IP addresses.

From a System Design Perspective:

DNS helps in load balancing by directing traffic to multiple servers.

DNS caching can reduce latency but may also lead to stale records.

Strategies like TTL (Time-To-Live) optimization are crucial for DNS performance.



### Load Balancing

Definition:
Load balancing is the process of distributing network traffic across multiple servers to ensure availability, scalability, and fault tolerance.

Key Considerations in System Design:

Types: Hardware load balancers, software load balancers (e.g., Nginx, HAProxy), and cloud-based solutions (e.g., AWS ELB).

Algorithms: Round Robin, Least Connections, IP Hashing, etc.

Load balancers often use public IPs for external communication and private IPs for internal communication.



### NAT (Network Address Translation)

Definition:
NAT allows multiple devices on a private network to share a single public IP address for internet access. It modifies the source IP of outgoing packets and the destination IP of incoming packets.

Use Cases in System Design:

Conserves public IP addresses.

Provides a layer of security by hiding internal network details from external users.

Facilitates communication between private and public networks.



### CDN (Content Delivery Network)

Definition:
A CDN is a network of distributed servers that deliver web content and other data to users based on their geographic location.

System Design Benefits:

Reduces latency by serving content from the nearest server.

Decreases load on the origin server.

Improves fault tolerance and scalability.


---

## Questions

<details>
<summary>What is a public IP? In which scenarios, one should use a public IP?</summary><br><b>
</b></details>

<details>
<summary>What is a private IP? In which scenarios, one should use a private IP?</summary><br><b>
</b></details>

<details>
<summary>What is latency?</summary><br><b>
</b></details>

<details>
<summary>What is latency of L1 cache reference vs. L2 cache reference?</summary><br><b>

L1 cache reference latency is 0.5 nanosecond
L2 cache reference latency is 7 nanosecond

So basically the latency of L2 cache reference is 14x L1 cache reference.
</b></details>
