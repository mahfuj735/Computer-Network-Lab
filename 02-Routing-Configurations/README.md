# 02 - Routing Configurations

This module explores Layer 3 inter-network routing principles implemented in **Cisco Packet Tracer**, contrasting deterministic manual routing (**Static Routing**) with automated protocol-driven routing (**Dynamic Routing**).

---

## 📂 Sub-Directories & Labs

| Lab Directory | Experiment Title | Protocol / Mode | Simulation Files | Description |
| :--- | :--- | :--- | :--- | :--- |
| [**Lab03-Static-Routing**](./Lab03-Static-Routing/) | **Static Routing for Interconnected Networks** | Manual `ip route` configuration | [`four_router_static.pkt`](./Lab03-Static-Routing/four_router_static.pkt), [`three_router_static.pkt`](./Lab03-Static-Routing/three_router_static.pkt) | Explicit next-hop definition across 3 and 4 router networks. |
| [**Lab04-Dynamic-Routing**](./Lab04-Dynamic-Routing/) | **Dynamic Routing for Interconnected Networks** | Distance-Vector / Link-State (RIP / OSPF) | [`four_router_dynamic.pkt`](./Lab04-Dynamic-Routing/four_router_dynamic.pkt), [`three_router_dynamic.pkt`](./Lab04-Dynamic-Routing/three_router_dynamic.pkt) | Automated route discovery and convergence across 4 routers. |

---

## ⚖️ Static vs Dynamic Routing Comparison

| Metric | Static Routing | Dynamic Routing |
| :--- | :--- | :--- |
| **Route Configuration** | Manually configured by network engineer | Discovered and maintained by protocols automatically |
| **Scalability** | Best for small, simple topologies (≤ 3 routers) | Scales effortlessly to large, complex enterprise networks |
| **CPU / RAM Overhead** | Negligible router CPU and memory utilization | Requires memory for routing tables and CPU for calculations |
| **Bandwidth Overhead** | Zero routing update packets on links | Periodic or event-triggered protocol advertisement packets |
| **Network Changes** | Administrator must reconfigure all affected routers | Routers automatically converge on new paths upon failure |
| **Security** | High (No route advertisements sent over links) | Authentication should be configured (e.g. MD5 in OSPF) |

---

## 💡 Quick Cisco IOS CLI Routing Cheatsheet

```ios
! Enable privileged EXEC mode
Router> enable

! Enter configuration mode
Router# configure terminal

! View routing table
Router# show ip route

! View IP interface status
Router# show ip interface brief

! Static route command
Router(config)# ip route <destination-network> <subnet-mask> <next-hop-ip>

! RIP configuration
Router(config)# router rip
Router(config-router)# version 2
Router(config-router)# no auto-summary
Router(config-router)# network <network-id>
```
