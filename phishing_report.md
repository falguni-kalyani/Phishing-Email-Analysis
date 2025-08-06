# Phishing Email Analysis Report

## 1. Email Content Overview

*Subject:* Monday.com - Invitation to join Board  
*Sender:* support@shared-document.com  
*Content:* Fake invitation to join a Monday.com board, trying to look urgent and legitimate.

###  Phishing Indicators in Content:
- Sender email domain is not related to Monday.com
- Uses brand logo to trick the user
- Generic message (“You were invited to join a Board”) to create confusion
- Attempts to get user to click without verifying source

---

## 2. Email Header Analysis (via MXToolbox)

### Header Info:
- *Return-Path:* support@shared-document.com
- *Received-SPF:* fail
- *Authentication-Results:* dmarc=fail (reason = "SPF and DKIM not aligned")
- *Sender IP:* 192.0.2.1 (suspiciousdomain.com)

###  Header-Based Indicators:
- SPF failed — not verified by sender domain
- DMARC failed — domain misalignment (spoofing risk)
- Email originates from suspicious IP (not linked to Monday.com)

---

##  Conclusion:

This is a clear *phishing attempt* using:
- Spoofed sender address
- Fake branding (Monday.com)
- Failed authentication (SPF, DKIM, DMARC)
