# CCNA Labs

Hands-on Cisco networking labs built in the **PingMyNetwork Sandbox**, following CCNA topics. Each lab has its own README with a topology diagram, addressing plan, configuration walkthrough, verification steps, guided challenges and the exported Sandbox JSON, so you can load it and try it yourself.

## Labs

| # | Lab | Topics | Devices |
|---|---|---|---|
| 01 | [Simple Switch Network with VLANs](lab-01-vlan-segmentation/) | VLAN creation, access ports, Rapid-PVST+, broadcast-domain isolation | 1 × 2960, 2 PCs |
| 02 | [Inter-VLAN Routing and ACL-Based VLAN Isolation](lab-02-inter-vlan-routing-acl/) | 802.1Q trunking, Layer 3 switching, SVIs, named extended ACLs | 1 × 3560, 1 × 2960, 2 PCs |
| 03 | [Spanning Tree Protocol (STP) and Failover](lab-03-stp-failover/) | Rapid-PVST+, root bridge election, port roles, LACP EtherChannel, failover | 4 × 2960, 4 PCs |
| 04 | [EtherChannel (LACP, PAgP and Static)](lab-04-etherchannel/) | LACP, PAgP, static EtherChannel, trunking over port-channels, member consistency | 3 × 2960, 2 PCs |

The labs build on each other. Lab 01 shows that VLANs isolate hosts at Layer 2. Lab 02 adds a Layer 3 switch so the VLANs *can* talk, then uses ACLs to decide that they *shouldn't*. Lab 03 adds redundant links between switches and shows how spanning tree keeps them loop-free and fails over. Lab 04 bundles parallel links with all three EtherChannel modes and compares how they negotiate.

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
