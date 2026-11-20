# IT Infrastructure & Networking Portfolio

Practical networking, security, and systems administration case studies built in Cisco Packet Tracer, demonstrating end-to-end LAN design, CLI configuration, security enforcement, and handover documentation.

---

## Case Study 1: AutoMoto Dealership (LAN Segmentation & Security)

**Objective:** Redesign a flat, unmanaged two-floor dealership network into a segmented, secure architecture isolating confidential finance workstations from public showroom PCs while maintaining shared access to an internal inventory server.

**Technologies Applied:** Cisco IOS, VLANs, 802.1Q Trunking, Router-on-a-Stick, DHCP, Extended Access Control Lists (ACLs), Internal DNS & HTTP.

### Project Deliverables
* [View Complete Technical Case Study (PDF)](./Case-Study-1-AutoMoto-Dealership/AutoMoto%20Dealership.docx)
* [Download Cisco Packet Tracer Topology (.pkt)](./Case-Study-1-AutoMoto-Dealership/AutoMoto%Dealership.pkt)

### Key Technical Achievements
* **Layer 2 Segmentation:** Partitioned a two-floor office into 3 VLANs (`VLAN 10` Showroom, `VLAN 20` Finance, `VLAN 30` Server) across two Cisco 2960 switches linked via 802.1Q trunking.
* **Inter-VLAN Routing & DHCP Automation:** Configured Router-on-a-Stick sub-interfaces and excluded-address DHCP pools on a Cisco 1941 router to automate IPv4 addressing across 10 workstations.
* **Traffic Isolation (Extended ACL):** Deployed an inbound Extended ACL on the Showroom sub-interface to block cross-department access to Finance (`192.168.20.0/24`) while permitting HTTP/DNS access to `inventory.automoto.local` (`192.168.30.10`).
