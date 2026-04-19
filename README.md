# Erpitone
Network scanner.

# 🚀 Erpitone – Network Scanner

**Erpitone v1.0.0** is a lightweight Python-based network scanner designed to perform basic reconnaissance on IP addresses and web servers. It supports ICMP checks, port scanning, and simple server detection via HTTP headers.

> ⚠️ This project is still a work in progress.

---

## 📌 Features

* <img width="1002" height="582" alt="Screenshot 2026-04-19 201425" src="https://github.com/user-attachments/assets/d5a3a8db-a616-4bff-b9c7-f9e6e673a1cc" />
 ICMP Echo Request (Ping)
*  Scan 30 most common ports
*  Full port scan (1–65535)
*  Basic HTTP/HTTPS server detection
*  Logging with `loguru`

---

## ⚙️ Requirements

Make sure you have Python 3 installed.

### Required libraries:

* `argparse` (built-in)
* `requests`
* `loguru`
* `scapy`

Install dependencies with:

```bash
pip install requests loguru scapy
```

---

## 🛠️ Usage

```bash
python erpitone.py -ip <IP_ADDRESS> [OPTIONS]
```

### Required argument:

| Argument                  | Description                         |
| ------------------------- | ----------------------------------- |
| `-ip`, `--ip`, `-address` | Target IP address (e.g., `8.8.8.8`) |

---

## 🔍 Available Options

### 1. ICMP Scan

Send a ping request to check if the host is reachable:

```bash
python erpitone.py -ip 8.8.8.8 -icmp
```

---

### 2. Common Port Scan

Scan the 30 most common ports:

```bash
python erpitone.py -ip 8.8.8.8 -ports
```

---

### 3. Full Port Scan

Scan all 65535 ports (⚠️ slow):

```bash
python erpitone.py -ip 8.8.8.8 --full-ports
```

---

### 4. Server Detection

Retrieve HTTP/HTTPS headers to identify server information:

```bash
python erpitone.py -ip <IP_ADDRESS> --server-detection example.com
```

---

## 🧾 Logging

All scan results are saved in:

```
scan.log
```

---

## 📂 Example

```bash
python erpitone.py -ip 154.22.3.14 -icmp -ports
```

---

## Disclaimer

This tool is intended for **educational and authorized testing purposes only**.

> Any unauthorized or unethical use of this software may be illegal in your country.
> The author is not responsible for misuse or damage caused by this tool.

---

## Author

Created by **flavio400**

---

## Status

* Version: `1.0.0`
* Status: 🟡 Work in Progress
* 
---
