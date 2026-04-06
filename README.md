# Home Network Projects — Setup & Troubleshooting

A portfolio of real-world home networking projects, troubleshooting case studies, and documentation. Each entry is based on an actual problem encountered and resolved, with full methodology and findings documented.

---

## About This Repository

This repo serves as a living record of hands-on networking experience — covering home network setup, device configuration, parental controls, router management, and systematic troubleshooting. Every case study is real, not simulated.

**Skills covered:**
- Home network troubleshooting methodology
- Router and mesh network configuration
- MAC addressing and DHCP
- IoT device setup and network integration
- Parental control systems and device profiles
- Network segmentation and SSID management
- Root cause analysis and technical documentation

---

## Network Environment

This portfolio is based on a live SOHO network managing 26+ devices across multiple categories including workstations, mobile devices, smart TVs, gaming consoles, tablets, and a dedicated IP security camera system.

See the full [Network Overview](./docs/network-overview.md) for infrastructure details and device inventory.

---

## Case Studies

| # | Title | Key Concepts | Status |
|---|---|---|---|
| 01 | [Amazon Kids Tablet — Wi-Fi & Server Connection Fix](./case-studies/01-amazon-kids-tablet-mac-address.md) | MAC randomization, device profiles, DHCP | ✅ Resolved |
| 02 | [Arlo Camera Setup, Troubleshooting & Network Expansion](./case-studies/02-arlo-camera-setup-network-expansion.md) | IoT isolation, mesh expansion, network congestion | ✅ Resolved |

> More case studies will be added as new issues are encountered and resolved.

---

## Repository Structure

```
home-network-projects-setup-troubleshooting/
├── README.md                  ← You are here
├── case-studies/              ← Individual troubleshooting write-ups
│   ├── 01-amazon-kids-tablet-mac-address.md
│   └── 02-arlo-camera-setup-network-expansion.md
└── docs/                      ← Reference guides and network diagrams
    ├── network-overview.md
    └── (more coming soon)
```

---

## Environment

| Component | Details |
|---|---|
| Router | Dual-node mesh network |
| ISP | Home ISP |
| Parental controls | Device profile-based filtering and scheduling |
| Network segmentation | Separate SSIDs for managed and unmanaged devices |
| Security | Dedicated IP camera system with hub |
| OS | Windows / Android / Apple iOS / Fire OS / Nintendo OS |

---

*This is an active portfolio repository. New projects and case studies are added regularly.*
