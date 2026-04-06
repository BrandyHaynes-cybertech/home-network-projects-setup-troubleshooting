# Case Study 01 — Amazon Kids Tablet: Wi-Fi & Server Connection Fix

**Issue:** Amazon Kids tablet repeatedly failed to connect to home Wi-Fi and reach game servers  
**Root Cause:** MAC address randomization conflicting with Eero router device profiles  
**Resolution:** Disabled MAC address randomization on the tablet  
**Time to Resolve:** ~ 30 Minutes  

---

## Problem Description

A child's Amazon Kids tablet on a home Eero mesh network would frequently fail to connect to the internet. The tablet appeared connected to Wi-Fi but displayed a **"Connection Error — Unable to Contact Server"** message, even when it was connected to the internet. 

### Symptoms
- Tablet showed as connected to Wi-Fi but could not reach the internet
- Switching to a mobile hotspot then back to home Wi-Fi temporarily fixed the issue
- Problem returned after every reboot or sleep cycle
- Date/time settings were correct; restarts did not resolve the issue

---

## Environment

| Component | Details |
|---|---|
| Device | Amazon Kids Tablet (Fire OS) |
| Router | Eero mesh network with parental controls |
| ISP | Sparklight |
| App affected | All |
| Network profile | Child's dedicated Eero profile with content filters applied |

---

## Troubleshooting Process

### Step 1 — Ruled out basic connectivity
- Confirmed other devices on the same network connected without issues
- Verified date and time settings were correct on the tablet
- Restarted the router and tablet — problem persisted

### Step 2 — Identified the hotspot pattern
Connecting to a mobile hotspot and switching back to the home Wi-Fi temporarily restored full connectivity. This was a critical clue — it pointed to a **network identity or DHCP issue** rather than a hardware or app fault, since the hotspot gave the tablet a fresh IP and clean connection state.

### Step 3 — Checked Eero parental controls
Reviewed the child's Eero profile for content filters that might be blocking Roblox or Amazon's servers. No filter category clearly mapped to the issue. Filters for gaming, social, and ad-blocking were reviewed but none were definitively the cause.

### Step 4 — Discovered MAC address randomization
The tablet had **MAC address randomization** enabled — a privacy feature that generates a different MAC address each time the device connects to a network.

**Why this caused the problem:**
Eero uses MAC addresses to identify devices and apply the correct profile and filter settings. With randomization on, the tablet presented as a new, unknown device on every reconnect. Eero could not consistently match it to the child's profile, causing erratic filter behavior and broken server connectivity for Roblox.

This also explained the hotspot workaround — reconnecting via hotspot triggered a fresh DHCP lease and briefly reset Eero's device recognition, restoring normal access until the next reconnect.

### Step 5 — Applied the fix

Disabled MAC address randomization on the tablet:

1. Open **Settings → Wi-Fi**
2. Tap the gear icon next to the home network name
3. Tap **MAC address type**
4. Change from **Randomized MAC** → **Device MAC**

After saving, the tablet maintained a consistent MAC address. Eero correctly recognized it as the child's registered device, applied the right profile settings, and Roblox connected successfully.

---

## Root Cause Summary

| Factor | Detail |
|---|---|
| Feature | MAC address randomization (enabled by default on modern devices) |
| Conflict | Eero profile system relies on MAC addresses to identify and manage devices |
| Effect | Tablet appeared as a new unknown device on every reconnect, causing inconsistent profile application and broken server connections |

---

## Resolution

**Disable MAC address randomization** on the tablet and set it to use the permanent hardware MAC address. This gives the Eero router a stable, consistent identity to associate with the child's profile.

---

## Key Takeaways

- MAC address randomization is a common default privacy feature that can silently break router-level parental control and device profile systems
- The "works on hotspot but not home network" pattern is a strong indicator of a **device identity or DHCP conflict**, not a hardware or app issue
- Eero and similar mesh systems tie parental profiles to MAC addresses — randomization breaks that relationship
- Always check MAC address settings when a device behaves inconsistently on a managed network

---

## Skills Demonstrated

- Systematic home network troubleshooting
- Understanding of MAC addressing and DHCP
- Eero mesh router and parental control configuration
- Root cause analysis from behavioral clues
- Clear technical documentation

---

*Part of the [Home Network Projects — Setup & Troubleshooting](../README.md) portfolio.*
