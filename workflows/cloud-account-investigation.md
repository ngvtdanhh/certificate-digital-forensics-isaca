# ☁️ Cloud Account Investigation Workflow

## 🧩 Scenario
An employee is suspected of uploading confidential files to a personal cloud account (e.g., Google Drive, Dropbox).

---

## 🛠️ Tools Used
- Browser history parser (e.g., BrowsingHistoryView)
- Network capture tools (Wireshark)
- Endpoint Detection & Response (EDR) logs

---

## 🧪 Steps
1. Exported browser history (Chrome/Edge) from suspect's workstation
2. Filtered visits to `drive.google.com`, `dropbox.com`, etc.
3. Correlated timestamps with internal file access logs
4. Checked EDR logs for unauthorized file movements
5. Captured network traffic to confirm file upload events

---

## ✅ Findings
- Suspect accessed Dropbox during working hours
- Several sensitive PDFs matched upload timestamps
