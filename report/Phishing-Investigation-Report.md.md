# Investigation Report

## Incident Information

| Field | Value |
|--------|-------|
| Incident ID | PHISH-2026-001 |
| Incident Type | Phishing Email |
| Severity | High |
| Status | Closed |
| Analyst | Yogesh Mali |
| Investigation Date | 01-Aug-2026 |

---

# Executive Summary

A user reported a suspicious email claiming to be from **Microsoft Security Team**. The email requested the recipient to verify their Microsoft 365 account by clicking a login link.

The investigation confirmed multiple phishing indicators, including a spoofed sender domain, urgent language, and a fake Microsoft login page. Based on the findings, the email was classified as a **phishing attempt**.

---

# Email Details

| Field | Value |
|--------|-------|
| From | support@micr0soft-security.com |
| To | employee@company.com |
| Subject | Action Required: Verify Your Microsoft 365 Account |
| Attachment | None |
| Embedded URL | https://login-micr0soft-security.com |

---

# Investigation Process

## Step 1 – Sender Verification

The sender email address was analyzed.

**Official Domain**

```text
microsoft.com
```

**Received Domain**

```text
micr0soft-security.com
```

### Findings

- Uses **0 (zero)** instead of **o**
- Not an official Microsoft domain
- Possible domain spoofing

**Status:** Suspicious

---

## Step 2 – Subject Analysis

**Subject**

```text
Action Required: Verify Your Microsoft 365 Account
```

### Findings

- Uses urgent language
- Encourages immediate action
- Attempts to create fear

**Status:** Suspicious

---

## Step 3 – Email Content Analysis

The email body requested the user to verify the account within 24 hours to avoid suspension.

### Findings

- Uses social engineering techniques
- Creates urgency
- Attempts credential theft

**Status:** Suspicious

---

## Step 4 – URL Analysis

**URL**

```text
https://login-micr0soft-security.com
```

### Findings

- Domain is not owned by Microsoft
- Mimics the Microsoft login page
- Intended for credential harvesting

**Status:** Malicious

---

## Step 5 – Email Header Analysis

The email header was reviewed.

### Fields Checked

- From
- Return-Path
- Reply-To
- Message-ID

### Findings

- Sender information is inconsistent with Microsoft's official domain
- Indicates possible email spoofing

**Status:** Suspicious

---

## Step 6 – VirusTotal Analysis

The suspicious email and associated indicators were analyzed using VirusTotal.

### Findings

- Reputation analysis performed
- Results documented as supporting evidence

---

# Indicators of Compromise (IOCs)

| IOC Type | Value |
|----------|-------|
| Sender Email | support@micr0soft-security.com |
| Domain | micr0soft-security.com |
| URL | https://login-micr0soft-security.com |
| Subject | Action Required: Verify Your Microsoft 365 Account |

---

# MITRE ATT&CK Mapping

| Tactic | Technique |
|---------|-----------|
| Initial Access | Phishing (T1566) |
| Credential Access | Credential Harvesting |

---

# Impact Assessment

The phishing email attempted to trick the recipient into revealing Microsoft 365 credentials. If successful, an attacker could gain unauthorized access to the user's account and organizational resources.

---

# Recommended Actions

- Block the sender email address.
- Block the malicious domain.
- Block the phishing URL.
- Notify potentially affected users.
- Reset user credentials if the link was accessed.
- Enable or enforce Multi-Factor Authentication (MFA).
- Monitor for similar phishing attempts.

---

# Conclusion

The investigation confirmed that the email was a **phishing attempt**.

## Key Findings

- ✅ Spoofed sender domain
- ✅ Fake Microsoft login URL
- ✅ Urgent language
- ✅ Social engineering tactics
- ✅ Credential harvesting attempt

The email was classified as **Malicious (Phishing)**. Appropriate mitigation actions were recommended to reduce the risk of compromise.

---

# Skills Demonstrated

- Email Security Analysis
- Phishing Investigation
- Email Header Analysis
- IOC Identification
- MITRE ATT&CK Mapping
- Threat Analysis
- Incident Documentation
