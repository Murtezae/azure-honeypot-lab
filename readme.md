# Azure Honeypot Lab

This project sets up a Windows honeypot in Azure, forwards security logs to Sentinel, enriches logs with GeoIP data, and visualizes brute-force login attempts on a world map.

---

## 1. Setup Azure Subscription
Created a free Azure subscription and logged into the portal.

---

## 2. Create the Honeypot VM
- Deployed a Windows 10 VM in Azure.
- Configured the NSG to allow all inbound traffic.
- Disabled Windows Firewall.

![VM NSG Settings](images/vm-nsg.png)

---

## 3. Failed Login Attempts
- Attempted 3 failed logins as "employee".
- Verified failed login logs in Event Viewer (Event ID 4625).

![Event Viewer Failed Logins](images/event-viewer.png)

---

## 4. Log Analytics Workspace & Sentinel
- Created a Log Analytics Workspace.
- Connected Azure Sentinel.
- Configured security event forwarding via AMA.

![Sentinel Logs](images/sentinel-logs.png)

---

## 5. Log Enrichment
- Imported a GeoIP watchlist (≈54,000 rows).
- Used KQL query to join logs with geographic data.

![KQL Query GeoIP](images/kql-query.png)

---

## 6. Attack Map
- Built an Azure Sentinel Workbook using JSON.
- Visualized attacker IPs on a live map.

![Attack Map](images/attack-map.png)

---

## Skills Demonstrated
- Azure VM setup & network security configuration
- Log collection & analysis
- KQL querying
- SIEM enrichment & visualization
