# Multi-Protocol Routing Simulation

A Cisco Packet Tracer project demonstrating **RIP, OSPF, EIGRP, and mutual route redistribution** across multiple routing domains.

## 📌 Project Overview

Built a multi-router network where **Router4 acts as the central route redistribution gateway**, allowing routes to be exchanged between RIP, OSPF, and EIGRP routing domains.

The network was configured and tested using Cisco IOS commands and connectivity tests.

## 🔧 What I Built

* Configured **RIP** routing.
* Configured **OSPF Process 1 in Area 0**.
* Configured **EIGRP AS 1**.
* Connected the three routing domains through **Router4**.
* Configured **route redistribution** between RIP, OSPF, and EIGRP.
* Verified learned and redistributed routes using routing tables.
* Tested connectivity between different networks using `ping`.

## 🌐 Network Topology

![Network Topology](images/Topology.png)

### Main Transit Networks

| Routing Domain | Network           |
| -------------- | ----------------- |
| RIP            | `192.168.10.0/24` |
| OSPF           | `192.168.11.0/24` |
| EIGRP          | `192.168.12.0/24` |

**Router4** is the central redistribution router connecting the three routing domains.

## 🔄 Routing Protocols

| Protocol       | Configuration      |
| -------------- | ------------------ |
| RIP            | RIP routing domain |
| OSPF           | Process 1, Area 0  |
| EIGRP          | AS 1               |
| Redistribution | RIP ↔ OSPF ↔ EIGRP |

## ⚙️ Implementation

1. Created the multi-router topology in Cisco Packet Tracer.
2. Configured IPv4 addresses on router interfaces and end devices.
3. Configured RIP, OSPF, and EIGRP on their respective routers.
4. Configured Router4 for route redistribution between the routing protocols.
5. Verified routing tables and routing protocols.
6. Tested end-to-end connectivity using `ping`.

### Key Verification Commands

```text
show ip interface brief
show ip protocols
show ip route
ping <DESTINATION_IP>
```

## ✅ Verification

### Router4 — Route Redistribution

`show ip protocols` was used to verify the routing protocols and redistribution configured on Router4.

![Router4 Routing Protocols](images/EIGRP_router.png)

### Router6 — OSPF External Routes

RIP-originated networks were observed as **OSPF E2 external routes** in the OSPF routing domain.

![Router6 Routing Table](images/OSPF_router.png)

### Connectivity Test

`ping` was used to verify communication between devices across different routing domains.

![Connectivity Test](images/Ping.png)

## 📚 What I Learned

* Working with RIP, OSPF, and EIGRP.
* Configuring route redistribution between routing protocols.
* Reading and interpreting routing tables.
* Identifying OSPF external routes.
* Testing network connectivity using `ping`.

## 🛠️ Technologies & Skills

* Cisco Packet Tracer
* Cisco IOS
* Computer Networking
* IPv4
* RIP
* OSPF
* EIGRP
* Route Redistribution
* Routing Tables


## 📁 Project Structure

```text
Multi-Protocol-Routing-Simulation/
├── EIGRP_RIP_OSPF.pkt
├── README.md
└── images/
    ├── Topology.png
    ├── RIP_router.png
    ├── OSPF_router.png
    ├── EIGRP_router.png
    └── Ping.png
```
