# 📊 Log Correlation Analysis Workflow

## 🧩 Scenario

An internal security monitoring system triggered an alert due to a high number of failed login attempts followed by suspicious outbound traffic from a workstation within the finance department.

---

## 🛠️ Tools Used

- 📌 SIEM Platform (e.g., Splunk, Graylog, ELK)
- 📌 Windows Event Viewer (Security, System logs)
- 📌 Firewall logs (pfSense, Cisco ASA)
- 📌 Timesketch or Timesifter for timeline analysis

---

## 🧪 Investigation Steps

1. **Initial Alert Review**  
   Reviewed the SIEM alert: 30+ failed RDP login attempts within 10 minutes.

2. **Event Log Correlation**  
   Pulled related Event IDs:
   - `4625` – Failed login attempts
   - `4624` – Successful login
   - `1102` – Audit log cleared

3. **Timeline Reconstruction**  
   - Normalized timestamps (UTC)
   - Rebuilt activity timeline from endpoint, domain controller, and firewall logs.

4. **Firewall Analysis**  
   - Detected outbound connections to suspicious IPs (outside organization’s ASNs)
   - Matched timestamps to `.7z` file creation and outbound transfer over HTTPS

5. **Host-Level Indicators**  
   - Discovered unapproved 7-Zip portable binary
   - PowerShell execution logs showed base64-encoded payloads

---

## ✅ Key Findings

- Multiple failed brute-force attempts from a foreign IP
- Successful login via compromised credentials
- File compression and exfiltration using HTTPS
- Evidence of anti-forensics (cleared logs)

---

## 📁 Artifacts Collected

- Security logs: `Security.evtx`
- Compressed data: `exported-data.7z`
- PowerShell transcripts
- Full timeline from Timesketch

---

## 📝 Recommendations

- Enforce account lockout policy after N failed attempts
- Enable logging of archive tool execution
- Implement outbound data exfiltration detection
- Regular log backup & tamper protection

