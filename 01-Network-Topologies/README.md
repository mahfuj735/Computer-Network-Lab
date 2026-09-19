# 01 - Network Topologies

This module contains practical simulations, design analyses, and verification procedures for fundamental computer network physical and logical topologies implemented in **Cisco Packet Tracer**.

---

## 📂 Sub-Directories & Experiments

| Directory | Experiment Name | Key Device(s) | Description | Simulation File |
| :--- | :--- | :--- | :--- | :--- |
| [**Lab01-Star-Topology**](./Lab01-Star-Topology/) | **Star Topology** | Cisco 2960 Switch, 6 PCs | Central switch connecting 6 independent host PCs. Fast fault isolation and high scalability. | [`star_topology.pkt`](./Lab01-Star-Topology/star_topology.pkt) |
| [**Lab02-Mesh-Topology**](./Lab02-Mesh-Topology/) | **Mesh Topology** | 6 Cisco Switches, 6 PCs | Interconnected mesh configuration offering redundant failover paths and fault tolerance. | [`mesh_topology_switch.pkt`](./Lab02-Mesh-Topology/mesh_topology_switch.pkt) |
| [**Bus-Topology**](./Bus-Topology/) | **Bus Topology** | Hub/Bus Backbone Nodes | Shared transmission medium model with end-terminators. | [`bus_topology.pkt`](./Bus-Topology/bus_topology.pkt) |

---

## 🧠 Core Networking Concepts Covered
1. **Physical vs Logical Topologies**:
   - *Physical Topology*: Physical cabling layout (how wires are strung between devices).
   - *Logical Topology*: Path taken by data frames between endpoints (how signals travel).
2. **Layer 2 Switching & Spanning Tree (STP)**:
   - Eliminating Layer 2 loops and broadcast radiation in redundant topologies using 802.1D Spanning Tree.
3. **Collision vs Broadcast Domains**:
   - Star topology switches create a separate collision domain per port, unlike legacy shared hubs.
