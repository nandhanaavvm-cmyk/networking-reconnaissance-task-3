# Task 3: Networking & Reconnaissance

This repository documents my fundamental networking concepts and passive/active reconnaissance exercises for **Task 3 (Networking & Reconnaissance)** of my Ethical Hacking Internship at VirtualWorks.

---

## 1. Fundamental Networking Concepts

* **IP Address (Internet Protocol Address):** A unique numerical label assigned to every device connected to a computer network so it can be identified and communicate with other devices.
  * *IPv4 Example:* `93.184.216.34` (32-bit address)
  * *IPv6 Example:* `2606:2800:220:1:248:1893:25c8:1946` (128-bit address)
* **DNS (Domain Name System):** Often called the "phonebook of the internet," DNS translates human-readable domain names (like `example.com`) into machine-readable IP addresses.
* **Ports:** Virtual communication endpoints on a device that identify specific network services or applications. Ports range from `0` to `65535`:
  * `21` – FTP (File Transfer Protocol)
  * `22` – SSH (Secure Shell)
  * `53` – DNS (Domain Name System)
  * `80` – HTTP (Web Traffic)
  * `443` – HTTPS (Encrypted Web Traffic)
* **Protocols:** Standardized rules that govern how data is formatted, transmitted, and received across a network (e.g., **TCP**, **UDP**, **ICMP**, **HTTP/HTTPS**, **DNS**).

---

## 2. What is Reconnaissance?

**Reconnaissance (Footprinting / Information Gathering)** is the first phase of ethical hacking. It involves collecting publicly available and technical information about a target domain or system before testing for vulnerabilities.

* **Passive Reconnaissance:** Gathering information without directly interacting with the target system (e.g., WHOIS lookups, DNS records, search engine dorking).
* **Active Reconnaissance:** Directly probing the target system to gather details, which may be logged by the target's firewall or IDS (e.g., `ping`, `traceroute`, `nmap` port scanning).

---

## 3. Performing Basic Reconnaissance (Commands & Output)

*Target used for educational demonstration: `example.com` (IANA-reserved documentation domain)*

### A. Connectivity & Path Tracing (`ping` & `traceroute`)

#### 1. `ping` — Check if the host is alive and measure response time
```bash
ping -c 4 example.com
