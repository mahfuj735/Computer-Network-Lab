# 04 - Practice and Exercises

This directory contains experimental simulations, laboratory viva practice setups, and troubleshooting scenarios created during the course.

---

## 📁 Practice Simulation Topologies

| File | Type / Scope | Description |
| :--- | :--- | :--- |
| [`p1.pkt`](./p1.pkt) | **Drill 1 - Basic Subnetting** | Point-to-point host connectivity and default gateway validation. |
| [`p2.pkt`](./p2.pkt) | **Drill 2 - Multi-Switch LAN** | Cross-switch frame forwarding and MAC table convergence testing. |
| [`p3.pkt`](./p3.pkt) | **Drill 3 - Multi-Router Link** | WAN serial link clock rate configuration and gateway routing tests. |
| [`p4.pkt`](./p4.pkt) | **Drill 4 - Routing Protocol Debug** | Routing table convergence, route redistribution, and ping latency analysis. |

---

## 🛠️ Recommended Troubleshooting Steps
When testing network connectivity in these scenarios, follow standard Layer 1 through Layer 3 diagnostics:
1. **Physical / Link Layer Check**:
   - Verify all link lights are green. Amber ports on switches indicate Spanning Tree negotiation or blocked state. Red indicators indicate interface shutdown or cable mismatch.
2. **Interface Status**:
   ```ios
   Router# show ip interface brief
   ```
   Ensure status and protocol are both `up/up`.
3. **Routing Table Validation**:
   ```ios
   Router# show ip route
   ```
   Confirm destination subnet exists in the routing table.
4. **End Device Gateway**:
   - Check host IP configuration to confirm the Default Gateway matches the connected router interface IP.
