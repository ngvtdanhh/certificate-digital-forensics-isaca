# 🔍 USB Drive Artifact Analysis

## 🧩 Scenario
A USB flash drive was seized during a corporate data theft investigation. You are tasked with identifying deleted files and signs of data exfiltration.

---

## 🛠️ Tools Used
- Autopsy
- FTK Imager
- ExifTool

---

## 🧪 Steps Taken
1. Created forensic image of the USB using **FTK Imager**
2. Verified image hash for integrity (SHA256)
3. Loaded image into **Autopsy**
4. Recovered deleted files using file carving
5. Analyzed file metadata using **ExifTool**

---

## 📌 Findings
- Recovered 3 deleted `.docx` files with sensitive HR data
- File timestamps suggest manual deletion post-copy
- Exif data shows USB was last mounted on a personal laptop

---

## ✅ Conclusion
USB device was actively used to exfiltrate internal HR data. Artifacts are admissible in court.
