*This project has been created as part of the 42 curriculum by hiouzddo.*

# NetPractice

## Description

**NetPractice** is a networking project from the 42 curriculum designed to introduce and reinforce the fundamentals of computer networking.

The goal of the project is to understand how devices communicate with each other through networks and how to correctly configure network interfaces, subnet masks, routers, and routing tables.

Throughout the project, different network topologies must be analyzed and configured so that the required hosts and interfaces can communicate correctly.

The project focuses mainly on:

* IPv4 addressing
* Subnet masks and CIDR notation
* Network, host, and broadcast addresses
* Valid IP address ranges
* Routers and routing tables
* Default gateways
* Switches

The project contains **10 levels**, with each level introducing or combining different networking concepts. The objective is to correctly configure the provided network so that all required communication goals are satisfied.

---

## Instructions

### Running the Training Interface

The NetPractice training interface is provided by the project files.

To start the training interface, run:

```bash
./run.sh
```

Depending on the provided project files, the script may start a local web interface that can be accessed through a browser.

If necessary, make the script executable first:

```bash
chmod +x run.sh
```

Then:

```bash
./run.sh
```

Follow the instructions displayed by the training interface.

### Solving the Levels

Each level provides a network topology containing hosts, routers, switches, interfaces, and network information.

The objective is to configure the missing values correctly so that the required communication paths work.

When solving a level, pay particular attention to:

1. IP addresses
2. Subnet masks
3. Network addresses
4. Valid host ranges
5. Default gateways
6. Router interfaces
7. Routing tables
8. The direction of traffic
9. Whether a route is required in the reverse direction

The training interface indicates whether the configuration successfully satisfies the required communication goals.

### Exporting Configurations

After successfully completing each level, export the configuration using the export functionality provided by the NetPractice interface.

Each exported configuration should correspond to one completed level.

The repository must contain **10 exported configuration files**, one for each level.

The files must be placed directly at the **root of the repository**.

Example:

```text
.
├── README.md
├── level1.conf
├── level2.conf
├── level3.conf
├── level4.conf
├── level5.conf
├── level6.conf
├── level7.conf
├── level8.conf
├── level9.conf
└── level10.conf
```

The exact filenames may depend on the export format provided by the NetPractice interface.

### Submission Requirements

Before submitting the project, make sure that:

* All **10 levels** have been completed.
* Each level has been successfully validated by the training interface.
* **10 exported configuration files** are present.
* There is **one exported configuration file per level**.
* All 10 configuration files are located at the **repository root**.
* `README.md` is located at the repository root.
* The repository contains all files required for evaluation.

---

## Networking Concepts

NetPractice introduces several fundamental networking concepts.

### TCP/IP Addressing

An IPv4 address identifies a network interface using four decimal octets:

```text
192.168.1.10
```

An IP address is divided into a **network portion** and a **host portion** according to the subnet mask.

### Subnet Masks

A subnet mask determines which part of an IP address represents the network and which part represents the host.

For example:

```text
IP address:  192.168.1.10
Mask:        255.255.255.0
CIDR:        /24
```

With `/24`, the first 24 bits identify the network and the remaining 8 bits identify hosts.

Understanding subnet masks is essential for determining:

* Network addresses
* Broadcast addresses
* Valid host ranges
* Whether two interfaces belong to the same network

### Default Gateway

A **default gateway** is the router interface used when a host needs to communicate with a destination outside its local network.

For example:

```text
Host
  |
  | local network
  |
Router
  |
  | other network
  |
Destination
```

The host sends traffic for remote networks to its default gateway.

### Routers

A **router** connects different networks.

A router can have multiple interfaces, with each interface belonging to a different network.

Routers use **routing tables** to determine where packets should be forwarded.

Example:

```text
Network A
   |
   | Router
   |
Network B
   |
   | Router
   |
Network C
```

### Routing Tables

A routing table contains information that allows a router to determine where traffic should be sent.

A route generally contains information such as:

```text
Destination network
Next hop
Interface
```

A correct route is necessary when a destination network is not directly connected to the router.

### Switches

A **switch** connects devices within the same local network.

Unlike a router, a switch normally operates within a local network and does not perform the same network-to-network routing function.

### OSI Model

The project also relates to the **OSI model**, which divides networking communication into seven conceptual layers:

1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

NetPractice focuses particularly on concepts related to the **Network layer**, including IP addressing and routing, while also helping understand the role of lower-level networking components such as switches.

### TCP/IP Model

The project also reinforces the TCP/IP networking model and the relationship between:

* IP addressing
* Network interfaces
* Routing
* Transport protocols
* Applications

Understanding these concepts helps explain how data can travel from one host to another across multiple networks.

---

## Resources

The following resources were used to understand the networking concepts required for this project.

### Networking Documentation and References

* **RFC 791 — Internet Protocol (IPv4)**
  Reference for IPv4 addressing and the Internet Protocol.

* **RFC 4632 — Classless Inter-Domain Routing (CIDR)**
  Reference for CIDR notation and network prefix concepts.

* **OSI Model**
  Used to understand the different layers involved in network communication.

* **TCP/IP Networking Documentation**
  Used to understand IP addressing, routing, network interfaces, and communication between hosts.

### Concepts Studied

The main networking concepts studied during the project include:

* TCP/IP addressing
* IPv4 addresses
* Subnet masks
* CIDR notation
* Network addresses
* Broadcast addresses
* Host ranges
* Default gateways
* Routers
* Router interfaces
* Routing tables
* Next-hop routing
* Switches
* Local networks
* Remote networks
* Network segmentation
* OSI layers
* TCP/IP model
* Packet forwarding
* Bidirectional connectivity

### AI Usage

AI tools were used as a learning and debugging aid during the project.

They were used mainly to:

* Explain networking concepts such as subnet masks, CIDR notation, gateways, routers, and routing tables.
* Help understand how to calculate network and host ranges.
* Explain why a particular network configuration succeeds or fails.
* Analyze connectivity problems between hosts and routers.
* Provide step-by-step explanations of networking exercises.
* Help clarify concepts from the OSI and TCP/IP models.
* Review and improve understanding of configurations after attempting the exercises.

AI was used as a **learning support tool**, while the network configurations and solutions were tested and validated through the NetPractice training interface.
