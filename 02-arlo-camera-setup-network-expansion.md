# Case Study 02 — Arlo Security Camera System: Setup, Troubleshooting & Network Expansion

**Issue:** Security cameras experiencing connectivity glitches after initial Wi-Fi setup  
**Root Cause:** 5+ wireless cameras overloading home Wi-Fi without a dedicated hub  
**Resolution:** Deployed Arlo hub and expanded mesh network coverage  
**Time to Resolve:** Multiple days across setup and optimization phases  

---

## Problem Description

A home security camera system consisting of 5+ Arlo wireless cameras was initially configured to connect directly to the home Wi-Fi network. After setup, the cameras exhibited persistent connectivity issues that degraded the reliability of the security system.

### Symptoms
- Cameras frequently dropping offline
- Delayed or missed motion detection alerts
- Poor video quality and buffering
- Inconsistent connectivity across cameras despite full Wi-Fi signal

---

## Environment

| Component | Detail |
|---|---|
| Cameras | 5+ Arlo wireless IP cameras |
| Initial setup | Cameras connected directly to home Wi-Fi |
| Router | Dual-node mesh network |
| Network load | 25+ total devices on network |

---

## Troubleshooting Process

### Step 1 — Identified the pattern
All cameras showed similar issues regardless of their physical location. This ruled out signal strength as the root cause and pointed toward a network capacity or device management issue.

### Step 2 — Analyzed network load
With 25+ devices already on the network, adding 5+ cameras connecting directly to Wi-Fi created significant congestion. Wireless cameras are bandwidth-intensive devices that stream continuously — placing them all on a shared Wi-Fi network alongside other household devices created resource contention.

### Step 3 — Researched dedicated hub solution
Investigated the Arlo hub as an alternative to direct Wi-Fi connectivity. The hub uses a dedicated radio frequency to communicate with cameras, offloading them entirely from the Wi-Fi network and reducing congestion.

### Step 4 — Deployed Arlo hub
Installed the Arlo hub and migrated all cameras from direct Wi-Fi to hub-based connectivity. The hub connects to the router via ethernet, providing a stable wired backbone for the camera system while freeing up Wi-Fi bandwidth for other devices.

### Step 5 — Expanded mesh network coverage
Identified that certain areas of the environment had weaker signal coverage, affecting both camera reliability and general device connectivity. Added a second Eero mesh node to eliminate dead zones and provide consistent coverage across the full property.

---

## Results

| Issue | Before | After |
|---|---|---|
| Cameras dropping offline | Frequent | Rare |
| Motion alert delays | Common | Minimal |
| Video quality | Inconsistent | Stable |
| Network congestion | High | Reduced |
| Full property coverage | Partial | Complete |

---

## Root Cause Summary

| Factor | Detail |
|---|---|
| Primary cause | 5+ cameras connected directly to Wi-Fi on an already congested 25+ device network |
| Contributing factor | Insufficient mesh coverage creating weak signal zones |
| Resolution 1 | Arlo hub offloaded cameras from Wi-Fi to dedicated radio frequency |
| Resolution 2 | Second mesh node eliminated coverage dead zones |

---

## Key Takeaways

- IoT devices like security cameras should be isolated from general Wi-Fi traffic where possible — dedicated hubs or VLANs prevent network congestion
- A high device count network requires infrastructure planning, not just more devices
- Mesh network expansion is an effective solution for coverage dead zones in larger environments
- Adding infrastructure proactively (second mesh node) can solve multiple problems simultaneously — in this case both coverage and remote work readiness

---

## Skills Demonstrated

- IoT device setup and network integration
- Network congestion diagnosis and resolution
- Mesh network expansion and optimization
- Infrastructure decision making (hub vs direct Wi-Fi)
- Multi-device environment planning
- Security camera system administration

---

*Part of the [Home Network Projects — Setup & Troubleshooting](../README.md) portfolio.*
