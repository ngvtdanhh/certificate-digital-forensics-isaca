# ☁️ Cloud Forensics Workflow

## 🎯 Objective

Guide to conducting digital forensic investigations in cloud environments (e.g., AWS, Azure, GCP) with chain-of-custody integrity and data preservation.

---

## 🔍 Common Scenarios

- Insider data theft via cloud drives
- Misconfigured storage buckets (S3 leaks)
- Compromised IAM accounts
- Malware execution on cloud VMs

---

## 🛠️ Tools & Services

| Tool/Service            | Description                            |
|-------------------------|----------------------------------------|
| AWS CloudTrail          | API activity logs                      |
| Azure Monitor/Log Analytics | Event and resource logs               |
| GCP Audit Logs          | Admin activity and data access logs   |
| Velociraptor            | Live forensics on cloud endpoints      |
| AWS Snapshot            | Volume backup for evidence extraction  |

---

## 📋 Workflow Steps

1. **Preserve Evidence**
   - Snapshot VMs or block storage
   - Export logs (CloudTrail, Activity Log)
   - Lock down access via IAM changes

2. **Triage & Scope**
   - Identify compromised accounts/IPs
   - Determine lateral movement or privilege escalation

3. **Log Correlation**
   - Cross-match timestamps, user agents, IPs
   - Use SIEM tools (e.g., Splunk, Sentinel)

4. **Artifact Collection**
   - Download relevant logs, auth tokens, metadata
   - Use Volatility/Velociraptor if endpoint access allowed

5. **Chain of Custody**
   - Record snapshot hashes
   - Timestamp log exports and analyst access

---

## 📁 Output Files

- `cloudtrail-incident-YYYYMMDD.json`
- `snapshot-evidence-hash.txt`
- `iam-change-log.csv`

---

## ✅ Recommendations

- Always enable audit logging **before** incidents occur  
- Train teams on **cloud-native forensic readiness**  
- Automate snapshotting of high-risk resources

---

> 🧠 Tip: For sensitive environments, use **dedicated investigation accounts** to isolate forensic actions from regular operations.
