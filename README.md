# CCNA Labs

Hands-on Cisco networking labs built in the **PingMyNetwork Sandbox**, following CCNA topics. Each lab has its own README with a topology diagram, addressing plan, configuration walkthrough, verification steps, guided challenges and the exported Sandbox JSON, so you can load it and try it yourself.

## Labs

| # | Lab | Topics | Devices |
|---|---|---|---|
| 01 | [Simple Switch Network with VLANs](lab-01-vlan-segmentation/) | VLAN creation, access ports, Rapid-PVST+, broadcast-domain isolation | 1 × 2960, 2 PCs |
| 02 | [Inter-VLAN Routing and ACL-Based VLAN Isolation](lab-02-inter-vlan-routing-acl/) | 802.1Q trunking, Layer 3 switching, SVIs, named extended ACLs | 1 × 3560, 1 × 2960, 2 PCs |
| 03 | [Spanning Tree Protocol (STP) and Failover](lab-03-stp-failover/) | Rapid-PVST+, root bridge election, port roles, LACP EtherChannel, failover | 4 × 2960, 4 PCs |
| 04 | [EtherChannel (LACP, PAgP and Static)](lab-04-etherchannel/) | LACP, PAgP, static EtherChannel, trunking over port-channels, member consistency | 3 × 2960, 2 PCs |
| 05 | [Layer 3 EtherChannel](lab-05-l3-etherchannel/) | Routed LACP port-channel, lacp rate fast, max-bundle, static routing | 2 × 3560, 2 PCs |
| 06 | [EtherChannel and Inter-VLAN Routing](lab-06-etherchannel-inter-vlan/) | LACP trunk bundles, active/passive, SVIs, inter-VLAN routing | 1 × 3560, 2 × 2960, 2 PCs |
| 07 | [EtherChannel Troubleshooting](lab-07-etherchannel-troubleshooting/) | LACP mode mismatch, member inconsistency, wrong access VLAN, fault isolation | 2 × 2960, 2 PCs |
| 08 | [STP over EtherChannel](lab-08-etherchannel-stp/) | LACP trunk triangle, root primary/secondary, port-channel cost, bundle failover | 2 × 3560, 1 × 2960, 2 PCs |
| 09 | [Router-on-a-Stick over EtherChannel](lab-09-etherchannel-roas/) | ROAS subinterfaces, 802.1Q, LACP trunk bundle, inter-VLAN packet path | 1 × ISR4331, 2 × 2960, 2 PCs |
| 10 | [EtherChannel Mode Matrix](lab-10-etherchannel-mode-matrix/) | LACP/PAgP/static compatibility, port flags, EtherChannel guard, err-disable | 5 × 2960 |
| 11 | [10-Link LACP Bundle](lab-11-etherchannel-10-link-bundle/) | LACP member limits, system/port priority, hot-standby, single-member failover | 2 × 2960, 2 PCs |
| 12 | [Collapsed Core with EtherChannel and HSRP](lab-12-collapsed-core-hsrp/) | Routed core Po, dual-homed LACP trunks, HSRP priority/preempt, STP/HSRP alignment, core failover | 2 × 3560, 2 × 2960, 2 PCs |
| 13 | [OSPF over EtherChannel (ECMP)](lab-13-ospf-etherchannel-ecmp/) | Single-area OSPF, reference bandwidth, port-channel cost, equal-cost multipath | 2 × 3560, 2 PCs |
| 14 | [The "Fake MLAG" EtherChannel Trap](lab-14-etherchannel-fake-mlag/) | One bundle across two switches, load-balancing black hole, LACP partner rules, MLAG concepts | 3 × 2960, 2 PCs |
| 15 | [The Golden Rule: Configure the Po, Not the Members](lab-15-etherchannel-po-inheritance/) | Member consistency, CANNOT_BUNDLE2, silent suspended member, Po-to-member inheritance | 2 × 2960, 2 PCs |
| 16 | [DHCP Relay over EtherChannel](lab-16-dhcp-relay-etherchannel/) | IOS DHCP server pools, exclusions, ip helper-address, giaddr, return routing | 1 × ISR4331, 1 × 3560, 1 × 2960, 2 PCs |
| 17 | [HSRP Basics and Failover](lab-17-hsrp-basics-failover/) | HSRP virtual IP/MAC, priority, preempt, hello/hold timers, STP root alignment, gateway failover | 2 × 3560, 1 × 2960, 1 PC, 1 server |
| 18 | [HSRP Load Sharing and Uplink Tracking](lab-18-hsrp-load-sharing-tracking/) | Per-VLAN HSRP Active, object tracking, priority decrement, preempt, dual uplinks to an ISP | 2 × 3560, 1 × 2960, 1 × ISR4331, 1 PC, 1 server |
| 19 | [HSRP Dual-Active Troubleshooting](lab-19-hsrp-dual-active-troubleshooting/) | Dual-active symptoms, `%HSRP-4-BADAUTH`, MD5 authentication mismatch, group-number mismatch, virtual MACs | 2 × 3560, 1 × 2960, 1 × ISR4331, 1 PC, 1 server |
| 20 | [Layer 2 Security: BPDU Guard, Port Security, DHCP Snooping](lab-20-layer2-security/) | Rogue root bridge, BPDU/root guard, port security (sticky, violation), DHCP snooping trust and option 82, err-disable recovery | 1 × ISR4331, 1 × 3560, 3 × 2960, 4 PCs |
| 21 | [Capstone: Enterprise Campus + Branch](lab-21-capstone-campus-branch/) | NAT/PAT, central DHCP + relay, multi-area OSPF, LACP, native VLAN, Rapid-PVST, HSRP (MD5, tracking), DHCP snooping, port security, BPDU guard, ROAS, guest ACL | 3 × ISR4331, 2 × 3560, 3 × 2960, 4 PCs, 1 server |
| 22 | [Router Between Two Networks](lab-22-router-two-networks/) | **Start here:** router interfaces, `no shutdown`, connected/local routes, default gateway, TTL hop count | 1 × ISR4331, 2 PCs |
| 23 | [Inter-Subnet Routing](lab-23-inter-subnet-routing/) | Router as gateway for two switched LANs, `down` vs `administratively down`, same-subnet vs routed traffic, TTL hop count | 1 × ISR4331, 2 × 2960, 2 PCs, 1 server |
| 24 | [Static Routing with Two Routers](lab-24-static-routing-two-routers/) | `/30` transit link, `ip route` next hop, two-way routing, administrative distance, TTL across two hops | 2 × ISR4331, 2 × 2960, 2 PCs |
| 25 | [OSPF Single-Area with Three Routers](lab-25-ospf-single-area-three-routers/) | `router ospf`, wildcard masks, router ID, passive interfaces, 2WAY → FULL, DR/BDR, wait timer, OSPF cost and ECMP | 3 × ISR4331, 3 PCs |
| 26 | [DHCP and NAT/PAT to the Internet](lab-26-dhcp-nat-pat-internet/) | IOS DHCP pool and exclusions, `ip nat inside/outside`, PAT (overload), inside/outside local/global, default route, loopback as remote host | 2 × ISR4331, 1 × 2960, 2 PCs |

The labs build on each other. Lab 01 shows that VLANs isolate hosts at Layer 2. Lab 02 adds a Layer 3 switch so the VLANs *can* talk, then uses ACLs to decide that they *shouldn't*. Lab 03 adds redundant links between switches and shows how spanning tree keeps them loop-free and fails over. Lab 04 bundles parallel links with all three EtherChannel modes and compares how they negotiate. Lab 05 makes the bundle routed, tunes LACP and connects two subnets with static routes. Lab 06 combines both: LACP trunk bundles to a Layer 3 core that routes between VLANs. Lab 07 breaks an EtherChannel on purpose and walks through finding and fixing each fault. Lab 08 runs spanning tree over a triangle of EtherChannels and fails over between bundles. Lab 09 moves inter-VLAN routing to a router-on-a-stick, with the VLANs carried over an EtherChannel trunk. Lab 10 tests four mode pairings side by side and shows the result of each. Lab 11 pushes a bundle past the 8-active-member limit and shows how LACP priorities choose which links forward. Lab 12 puts it all together in a production-style collapsed core with HSRP gateway redundancy. Lab 13 runs OSPF over a routed bundle and shows how its bandwidth drives path cost and ECMP. Lab 14 shows why one port-channel can't span two independent switches, even when it looks healthy. Lab 15 shows why settings belong on the port-channel, not on individual members. Lab 16 adds DHCP: a router hands out addresses to both VLANs through a Layer 3 switch acting as relay. Lab 17 covers HSRP from the basics: one virtual gateway, Active/Standby, failover and preempt. Lab 18 shares the load across both cores and uses uplink tracking to move a gateway when its uplink fails. Lab 19 breaks that setup on purpose: an authentication mismatch and a wrong group number leave both cores Active, and you find and fix each fault. Lab 20 returns to the access layer and protects it: a rogue switch that takes over as root bridge, too many MACs behind one port, and DHCP snooping that breaks DHCP until the uplink is trusted. Lab 21 is the capstone: an enterprise campus and branch behind a NAT edge that uses nearly everything from the earlier labs at once. Lab 22 goes back to basics: one router joining two networks. Although it was added last, it's the best place to start if you're new to routing. Lab 23 is the next step: the same single router, now with a switched LAN on each side and a server to reach. Lab 24 adds a second router, so each side needs a static route to reach the other's LAN. Lab 25 replaces static routes with OSPF: three routers in a triangle that learn each other's LANs on their own. Lab 26 moves to the network edge: one router that hands out addresses by DHCP and hides the whole LAN behind one public address with PAT.

## Repository layout

```text
lab-XX-<name>/
├── README.md        # Lab guide: topology, addressing, configs, verification, challenges
├── configs/         # Saved running-config of each network device
├── images/          # Topology diagram
└── lab-files/       # PingMyNetwork Sandbox export (.json)
```

## How to use a lab

1. Open the [PingMyNetwork Sandbox](https://pingmynetwork.com/sandbox).
2. Import the `.json` file from the lab's `lab-files/` folder.
3. Follow the lab README. Run the verification commands, then work through the guided challenges.

**Built with:** [PingMyNetwork Sandbox](https://pingmynetwork.com/sandbox)
