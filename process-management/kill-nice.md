# Process Control in Linux

Linux provides commands to control running processes,
including stopping, terminating, and changing priority.

---

## kill

Sends a signal to a process using its PID.

**Syntax:**
kill [signal] PID

**Common Examples:**
kill 1234  
kill -9 1234  

**Explanation:**
- `kill 1234` sends SIGTERM (graceful termination)
- `kill -9 1234` sends SIGKILL (forceful termination)

SIGKILL should be used only when a process does not stop normally.

---

## killall

Terminates processes by name.

**Syntax:**
killall process_name

**Example:**
killall nginx

**Explanation:**
Stops all processes matching the given name.

---

## nice

Starts a process with a specific priority.

**Syntax:**
nice -n priority command

**Example:**
nice -n 10 backup.sh

**Explanation:**
- Priority ranges from -20 (highest) to 19 (lowest)
- Default priority is 0

Higher value → lower priority.

---

## renice

Changes the priority of a running process.

**Syntax:**
renice priority -p PID

**Example:**
renice 5 -p 1234

**Explanation:**
Used to adjust resource usage of running processes.

---

## Common Signals

| Signal | Name | Purpose |
|------|------|---------|
| 15 | SIGTERM | Graceful stop |
| 9 | SIGKILL | Force stop |
| 1 | SIGHUP | Reload configuration |

---

## When to Use

- Use `kill` to stop a specific process
- Use `killall` when multiple instances exist
- Use `nice` and `renice` to manage system performance
