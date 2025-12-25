# Networking Commands in Linux

Linux provides various command-line tools to check network connectivity,
interface details, and DNS resolution.

---

## ip

Displays and manages network interfaces and routing.

**Syntax:**
ip [object] [command]

**Common Examples:**
ip addr  
ip link  
ip route  

**Explanation:**
Replaces older tools like `ifconfig` and `route`.

---

## ping

Checks network connectivity to a host.

**Syntax:**
ping destination

**Example:**
ping google.com

**Explanation:**
Sends ICMP packets to verify if the host is reachable.

---

## ss

Displays socket statistics.

**Syntax:**
ss [options]

**Example:**
ss -tuln

**Explanation:**
Shows listening TCP and UDP ports.

---

## netstat

Displays network connections and routing tables.

**Example:**
netstat -tuln

**Explanation:**
Older tool, mostly replaced by `ss`, but still commonly used.

---

## traceroute

Shows the path packets take to reach a destination.

**Example:**
traceroute google.com

**Explanation:**
Useful for identifying network delays or failures.

---

## nslookup

Queries DNS to obtain domain information.

**Example:**
nslookup google.com

**Explanation:**
Checks DNS resolution.

---

## curl

Transfers data from or to a server.

**Example:**
curl https://example.com

**Explanation:**
Commonly used to test APIs and web services.

---

## When to Use

- `ping` → connectivity check
- `ip` → interface and routing info
- `ss` / `netstat` → open ports
- `traceroute` → path issues
- `curl` → service availability
