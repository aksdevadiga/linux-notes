# Package Management in Linux

Linux uses package managers to install, update, and remove software.
Different Linux distributions use different package managers.

---

## APT (Debian / Ubuntu)

APT (Advanced Package Tool) is used in Debian-based systems.

**Update package list:**
sudo apt update

**Install a package:**
sudo apt install package_name

**Remove a package:**
sudo apt remove package_name

**Upgrade installed packages:**
sudo apt upgrade

---

## YUM (RHEL / CentOS)

YUM (Yellowdog Updater, Modified) is used in Red Hat-based systems.

**Install a package:**
sudo yum install package_name

**Remove a package:**
sudo yum remove package_name

**Update packages:**
sudo yum update

---

## DNF (Fedora / Newer RHEL)

DNF is the modern replacement for YUM.

**Install a package:**
sudo dnf install package_name

**Remove a package:**
sudo dnf remove package_name

**Update packages:**
sudo dnf upgrade

---

## Comparison Summary

| Package Manager | Distribution |
|----------------|-------------|
| apt | Ubuntu, Debian |
| yum | CentOS, RHEL (older) |
| dnf | Fedora, RHEL (newer) |

---

## Best Practices

- Always update package lists before installing
- Install only required packages
- Remove unused packages to save space
