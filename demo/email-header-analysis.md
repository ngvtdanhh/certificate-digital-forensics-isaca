# 📧 Email Header Analysis

## 🧩 Scenario
An employee reported a phishing attempt. The suspicious email was forwarded to the incident response team.

---

## 🛠️ Tools Used
- Email Header Analyzer (MxToolbox)
- Python script for decoding Base64
- WHOIS lookup

---

## 🧪 Steps Taken
1. Extracted raw email headers from Outlook
2. Analyzed **Received** fields for source IP
3. Used WHOIS to trace IP back to a foreign ISP
4. Decoded email body and checked embedded links

---

## 📌 Findings
- Source IP: 185.XX.XX.13 (Russia)
- Return-Path domain had no SPF/DKIM
- Malicious link redirected to credential-harvesting page

---

## ✅ Conclusion
Phishing attempt confirmed. Blocked domain/IP and added indicators to SIEM watchlist.
