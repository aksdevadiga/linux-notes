# Network Troubleshooting in Linux

Network issues are common in Linux systems.
Troubleshooting requires checking connectivity, configuration,
and services step by step.

---

## Step 1: Check Network Connectivity

Use `ping` to verify basic connectivity.

**Example:**
ping google.com

If this fails, the system may not have internet access.

---

## Step 2: Check Network Interface

Verify if network interfaces are up.

**Command:**
ip addr

Look for:
- Interface status (UP/DOWN)
- Assigned IP address

---

## Step 3: Check Routing

Ensure a default route exists.

**Command:**
ip route

If no default gateway is present, traffic cannot leave the system.

---

## Step 4: Check DNS Resolution

Test DNS functionality.

**Command:**
nslookup google.com

If DNS fails but ping to IP works, the issue is DNS-related.

---

## Step 5: Check Open Ports and Services

Verify whether required services are listening.

**Commands:**
ss -tuln  
netstat -tuln  

Useful when applications are not reachable.

---

## Step 6: Test Application Access

Use `curl` to test web services or APIs.

**Example:**
curl http://localhost:8080

Confirms whether the service is responding.

---

## Common Issues and Causes

| Issue | Possible Cause |
|-----|---------------|
| No internet | Network interface down |
| Can ping IP but not domain | DNS issue |
| Service unreachable | Port not listening or firewall |
| Slow network | Routing or bandwidth issue |

---

## Basic Troubleshooting Approach

1. Start from local system
2. Check connectivity
3. Verify configuration
4. Test services
5. Narrow down the root cause
