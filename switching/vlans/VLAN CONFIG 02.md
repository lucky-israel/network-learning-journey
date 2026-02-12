SOHO Network Design Lab – VLAN Segmentation with VLSM and ROAS

This lab environment was designed to strengthen practical knowledge of VLAN segmentation, Variable Length Subnet Masking (VLSM), subnet allocation, and inter-VLAN routing using a Router-on-a-Stick (ROAS) architecture.

The objective was to implement logical separation between departments while optimizing IP address utilization and maintaining structured gateway assignment.

Network Architecture Overview

Routing Model: Router-on-a-Stick (ROAS)
Addressing Strategy: VLSM
Segmentation Method: VLAN-based isolation
Default Gateway (DG): Configured as the last usable IP address in each subnet

VLAN and Subnet Allocation
**VLAN 10 – Accounts Department**

Network: 192.168.1.0/28
Usable Range: 192.168.1.1 – 192.168.1.14
Broadcast: 192.168.1.15
Default Gateway: 192.168.1.14

This subnet provides 14 usable host addresses, allowing room for departmental growth while maintaining efficient address allocation.

**VLAN 20 – IT Department**

Network: 192.168.1.16/30
Usable Range: 192.168.1.17 – 192.168.1.18
Broadcast: 192.168.1.19
Default Gateway: 192.168.1.18

A /30 subnet was selected to support a minimal host requirement, demonstrating precise IP allocation using VLSM principles.

**VLAN 30 – HR Department**

Network: 192.168.1.20/29
Usable Range: 192.168.1.21 – 192.168.1.26
Broadcast: 192.168.1.27
Default Gateway: 192.168.1.26

This subnet supports up to six usable devices while maintaining segmentation from other departments.



**Design Principles Applied**

* Subnet design using VLSM to prevent address waste

* VLAN configuration and broadcast domain isolation

* 802.1Q trunk configuration and sub-interface routing

* Default gateway placement and inter-VLAN traffic flow validation

* Structured IP planning aligned with departmental size requirements

* Security-conscious segmentation approach to limit lateral movement


<img width="1917" height="778" alt="image" src="https://github.com/user-attachments/assets/47d6e519-c721-42f6-a91e-645eb88181fc" />



