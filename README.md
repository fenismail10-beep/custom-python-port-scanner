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

## <img width="1600" height="789" alt="resultat scan massar" src="https://github.com/user-attachments/assets/918eb4d3-f2f0-43dd-a104-661a2b05b823" />
<img width="1600" height="789" alt="resultat scan my site" src="https://github.com/user-attachments/assets/1340586d-1558-4ad3-afe2-845a6220dffe" />
<img width="795" height="687" alt="mousepad scanner py 2" src="https://github.com/user-attachments/assets/1fc639d1-6868-4eca-a55c-b6c07cd130f9" />
<img width="689" height="586" alt="mousepad scanner py 1" src="https://github.com/user-attachments/assets/5b9da313-ed88-48fe-9ce9-5ae970a1545c" />
 Project Portfolio Links
Full Pentest report metrics, PowerPoint design, and architecture summaries are published inside my web archive:
👉 **[Check My Cyber Labs Portfolio]([https://google.com](https://sites.google.com/view/ismailfendou-cybersec/my-cyber-labs))**
