## 1. `ping` (Check Connectivity)
**Purpose:** Sends ICMP echo requests to check if a host is reachable.  
**Usage:**  
```bash
ping <hostname/IP>
```
Example:  
```bash
ping google.com
```
🔹 Stops with `Ctrl + C` on Linux/macOS. On Windows, use `ping -t` for continuous pings.

---

## 2. `traceroute / tracert` (Trace Packet Routes)
**Purpose:** Shows the route packets take to reach a destination.  
**Usage:**  
- **Linux/macOS:**  
  ```bash
  traceroute <hostname/IP>
  ```
- **Windows:**  
  ```cmd
  tracert <hostname/IP>
  ```
Example:  
```bash
traceroute google.com
```
🔹 Helps in identifying network delays or bottlenecks.

---

## 3. `netstat` (Network Statistics)
**Purpose:** Displays active connections, listening ports, and network stats.  
**Usage:**  
```bash
netstat -an
```
🔹 Common options:  
- `-a` → Show all connections  
- `-n` → Show IPs instead of hostnames  
- `-tulnp` (Linux) → Show TCP/UDP listening ports with process info  

---

## 4. `curl` (Make HTTP Requests)
**Purpose:** Fetches data from URLs (useful for API testing, downloading files).  
**Usage:**  
```bash
curl <URL>
```
Example:  
```bash
curl -I google.com  # Fetch headers
curl -O <file_url>  # Download a file
```
🔹 Supports various methods: `-X POST`, `-X PUT`, etc.

---

## 5. `dig` / `nslookup` (DNS Lookup)
**Purpose:** Retrieves DNS information for a domain.  
**Usage:**  
- **Linux/macOS (dig):**  
  ```bash
  dig <domain>
  ```
- **Windows (nslookup):**  
  ```cmd
  nslookup <domain>
  ```
Example:  
```bash
dig google.com
nslookup google.com
```
🔹 `dig +short` gives a cleaner output, `nslookup` can query specific DNS servers.

---
