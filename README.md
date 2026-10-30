#  Custom Network Infrastructure Probing & Reconnaissance

This repository hosts a personal cybersecurity project (Lab 19) focused on programming a low-level network port discovery tool from scratch using Python 3. The tool operates within a Kali Linux CLI environment to map network perimeters without relying on third-party commercial applications.

---

##  Project Specifications
- **Language:** Python 3 (Native socket API) [1, 2]
- **Environment:** Kali Linux Terminal [1, 2]
- **Target Array:** Multi-domain assessment (Decentralized Web Cluster & Centralized Administrative Portal) [1, 2]
- **Ports Probed:** 22 (SSH), 80 (HTTP), and 443 (HTTPS) [1, 2]

---

##  Tool Architecture & Logic
The network probing engine directly interfaces with the operating system kernel network stack:
1. **Layer-4 Transport Handling:** Implements `socket.SOCK_STREAM` bindings to isolate dedicated TCP connection streams.
2. **Automated Name Resolution:** Integrates `socket.gethostbyname` to execute in-line DNS translation.
3. **Probing Validation Loop:** Employs `s.connect_ex()` checks. A return code of `0` flags the port state as `OPEN`, while non-zero values reflect `CLOSED` or filtered infrastructure lines.
4. **Log Output System:** Utilizes automated context managers (`with open`) to export real-time findings into an immutable `scan_report.txt` file.

---

##  Live Audit Documentation

### Audit A: Decentralized Web Cluster (`fenismail10-beep.github.io`)
Verified cloud delivery infrastructure pathways and verified perimeter configurations.
- **Resolved IP:** 185.199.111.153 [1, 2]
- **States Captured:** Port 22 CLOSED | Port 80 OPEN | Port 443 OPEN [1, 2]

### Audit B: Centralized Administrative Network (`massarservice.men.gov.ma`)
Audited the national student portal connection matrix.
- **Resolved IP:** 196.200.143.196 [1, 2]
- **States Captured:** Port 22 CLOSED | Port 80 OPEN | Port 443 OPEN [1, 2]
---
<img width="689" height="586" alt="mousepad scanner py 1" src="https://github.com/user-attachments/assets/64c6c1af-dcc3-4ab4-8cf7-47522fc61284" />
<img width="795" height="687" alt="mousepad scanner py 2" src="https://github.com/user-attachments/assets/a332db56-5fe5-44f3-8adc-0802c2772f1e" />
<img width="1600" height="789" alt="resultat scan my site" src="https://github.com/user-attachments/assets/08d5d887-c118-4234-835e-257f48ec8fc7" />
<img width="1600" height="789" alt="resultat scan massar" src="https://github.com/user-attachments/assets/8208e320-205c-4d85-a144-6141c89bcd6d" />
 Project Portfolio Links
Full Pentest report metrics, PowerPoint design, and architecture summaries are published inside my web archive:
👉  **[Check My Cyber Labs Portfolio]([https://google.com](https://sites.google.com/view/ismailfendou-cybersec/my-cyber-labs))**
