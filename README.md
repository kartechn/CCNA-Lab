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

The labs build on each other. Lab 01 shows that VLANs isolate hosts at Layer 2. Lab 02 adds a Layer 3 switch so the VLANs *can* talk, then uses ACLs to decide that they *shouldn't*. Lab 03 adds redundant links between switches and shows how spanning tree keeps them loop-free and fails over. Lab 04 bundles parallel links with all three EtherChannel modes and compares how they negotiate. Lab 05 makes the bundle routed, tunes LACP and connects two subnets with static routes. Lab 06 combines both: LACP trunk bundles to a Layer 3 core that routes between VLANs. Lab 07 breaks an EtherChannel on purpose and walks through finding and fixing each fault. Lab 08 runs spanning tree over a triangle of EtherChannels and fails over between bundles. Lab 09 moves inter-VLAN routing to a router-on-a-stick, with the VLANs carried over an EtherChannel trunk. Lab 10 tests four mode pairings side by side and shows the result of each. Lab 11 pushes a bundle past the 8-active-member limit and shows how LACP priorities choose which links forward.

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
