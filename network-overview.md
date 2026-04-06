# Network Overview — Home Lab & SOHO Environment

This document outlines the structure, segmentation, and device inventory of the managed home network environment used as the basis for all projects and case studies in this repository.

---

## Network Summary

This is a small office / home office (SOHO) network managing 25+ active devices across multiple device categories. The network is segmented, managed, and maintained as a practical home lab environment.

| Attribute | Detail |
|---|---|
| Network type | SOHO / Home Lab |
| Infrastructure | Dual-node mesh network |
| Segmentation | Separate networks for managed and unmanaged devices |
| Security | Dedicated IP camera system with hub |
| Parental controls | Device profile-based filtering and scheduling |
| Coverage | Full property coverage via mesh expansion |

---

## Infrastructure

| Device | Role |
|---|---|
| Mesh node 1 (primary) | Main router, DHCP, gateway |
| Mesh node 2 (secondary) | Extended coverage, remote work area |
| Security camera hub | Dedicated IoT device management |

The secondary mesh node was added to eliminate dead zones and ensure reliable connectivity across all areas of the environment, including a dedicated workspace for remote work.

---

## Network Segmentation

The network is divided into two separate SSIDs to isolate device categories and apply appropriate access controls:

| Network | Purpose | Controls Applied |
|---|---|---|
| Primary network | Adult devices, workstations, personal devices | Standard access |
| Secondary network | Managed devices, restricted access | Content filtering, scheduling, device profiles |

Segmenting the network improves security, limits cross-device access, and allows granular control over internet usage per device category.

---

## Device Inventory

| Category | Examples | Approx. Count |
|---|---|---|
| Network infrastructure | Mesh nodes, camera hub | 3 |
| Security cameras | Wireless IP cameras | 5+ |
| Smart TVs | Streaming devices | 4 |
| Mobile phones | iOS / Android | 4 |
| Tablets | Android / Fire OS | 4 |
| Personal computers | Windows workstations | 3 |
| School/work devices | Chromebooks / laptops | 2+ |
| Gaming consoles | Nintendo Switch | 1 |
| **Total managed devices** | | **26+** |

---

## Skills Demonstrated

- SOHO network design and management
- Mesh network setup and expansion
- Network segmentation and SSID management
- IoT device isolation via dedicated hub
- Parental control configuration and device profiling
- Multi-device troubleshooting across platforms and operating systems
- Proactive infrastructure planning for remote work environments

---

*This network serves as the live environment for all case studies and projects documented in this repository.*
