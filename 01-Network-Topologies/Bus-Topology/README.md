# Supplemental Experiment: Bus Topology Simulation

## 📋 Overview
A **Bus Topology** is a network configuration in which all devices are connected sequentially to a single shared central backbone cable (the "bus"). Terminators are placed at both ends of the backbone to absorb signals and prevent reflection. This experiment demonstrates the architecture, operation, advantages, and drawbacks of a classic Bus Topology.

---

## 🎯 Objectives
- Study the operational principles of shared broadcast medium architectures (CSMA/CD).
- Understand why terminators are essential at both ends of a bus network.
- Simulate and inspect frame transmission across shared nodes in Cisco Packet Tracer.
- Compare Bus topology with modern Star and Mesh architectures.

---

## 📁 Included Files
- [`bus_topology.pkt`](./bus_topology.pkt): Ready-to-run Cisco Packet Tracer simulation file.
- [`Bus_Topology_Guide.pdf`](./Bus_Topology_Guide.pdf): Supplementary documentation and theoretical background guide.

---

## ⚖️ Trade-offs Analysis
| Feature | Bus Topology | Star Topology | Mesh Topology |
| :--- | :--- | :--- | :--- |
| **Cabling Cost** | Minimal (Single backbone) | Moderate (Cable per device) | High (Redundant links) |
| **Fault Tolerance** | Low (Backbone break halts all) | High (Single node failure ok) | Highest (Multiple failovers) |
| **Troubleshooting** | Difficult | Easy | Moderate to Complex |
| **Collision Domain** | Single shared collision domain | Split per switch port | Split per switch/router link |
