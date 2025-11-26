# 🗂️ Notion Logging Zap (Important Emails Dashboard)

This document explains the Notion integration Zap, which logs important and opportunity emails into a Notion database for tracking.

---

# 📦 Overview

Triggered whenever an email is labeled **Important** or **Opportunities** by the classifier Zap.

It adds a row in Notion with:
- Subject  
- From  
- Category  
- Snippet  
- Received At  
- Gmail Link  

---

# 🪄 Step-by-step Logic

## **1. Trigger**
App: **Gmail**  
Event: **New Email Matching Search**

### Search Query:
label:Important OR label:Opportunities

yaml
Copy code

This makes sure the Zap fires only for important emails.

---

## **2. Notion Action**
App: **Notion**  
Event: **Create Database Item**

Database: **Important Emails**

### Field Mapping

| Notion Property | Value from Zapier |
|-----------------|-------------------|
| Subject         | Gmail → Subject |
| From            | Gmail → From Name |
| Category        | AI Classification Output or Gmail Label |
| Snippet         | Gmail → Snippet |
| Received At     | Gmail → Date |
| Gmail Link      | `https://mail.google.com/mail/u/0/#search/rfc822msgid:{{Message-ID}}` |

Insert Message-ID from Gmail trigger.

---

# 🎯 Final Output Example in Notion

| Subject | From | Category | Received At |
|---------|------|----------|-------------|
| Assignment 2 Reminder | Course Team | SUBMISSION | 2025-11-25 |
| Naukri – Interview Round 1 | HR Recruiter | OPPORTUNITIES | 2025-11-24 |

---

# 📎 Screenshots
Add screenshots of:
- Notion database setup  
- Zapier mapping  
- Successful test  

All saved in the `/assets` folder.
