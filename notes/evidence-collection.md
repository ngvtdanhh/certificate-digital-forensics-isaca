# 📦 Evidence Collection in Digital Forensics

## 🧭 Overview

Evidence collection is the foundational step in any digital forensics investigation. It ensures data is captured in a secure, forensically sound manner without altering the original source.

---

## 🧰 Common Sources of Digital Evidence

- 💻 **Hard Drives** – System files, user data, deleted files
- 📱 **Mobile Devices** – Texts, GPS, app data
- ☁️ **Cloud Storage** – Email, documents, user logs
- 🌐 **Network Logs** – Firewall, router, SIEM logs
- 🧠 **Memory (RAM)** – Running processes, encryption keys

---

## 🔐 Collection Best Practices

- Use **write blockers** for physical drives
- Capture **volatile memory** (RAM) quickly before shutdown
- Ensure **hashing** before and after collection (MD5/SHA1/SHA256)
- Document every step (device type, serial, time, tool used)

---

## ⚠️ Legal & Ethical Considerations

- Adhere to proper **authorization** (e.g., warrant or consent)
- Ensure **chain of custody** is strictly maintained
- Respect **data privacy** and scope of investigation

---

> 📝 Tools: FTK Imager, dd, Autopsy, EnCase, Magnet AXIOM
