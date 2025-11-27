# Software Architecture

## High-Level Architecture
- **Client:** Kali Linux VM (Penetration Tester)  
- **Target:** Metasploitable 2 VM  
- **Tools:** Nmap (Scanning), Metasploit (Exploitation), Logging & Reporting scripts

### Components
1. **Scanning Module**
   - Handles port scanning and service detection.
2. **Enumeration Module**
   - Collects service information, usernames, and configurations.
3. **Exploitation Module**
   - Executes available exploits and captures proof-of-concept.
4. **Post-Exploitation Module**
   - Performs privilege escalation, persistence, and data extraction.
5. **Reporting Module**
   - Organizes logs, outputs, screenshots, and generates final report.

### Architecture Style
- Modular design: each phase (Scanning → Enumeration → Exploitation → Post-Exploitation → Reporting) is a separate module to ensure reusability and maintainability.
