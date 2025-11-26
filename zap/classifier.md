# 📬 Email Classifier Zap (Zapier AI + Gmail + Labels)

This document explains the full logic behind the **email classification system** that sorts incoming emails using Zapier AI and applies Gmail labels based on importance.

---

# 🔥 Overview

The classifier Zap does 3 major things:

1. **Takes every new email**
2. **Runs AI classification + keyword fallback**
3. **Routes the email into one of 3 categories**:
   - SUBMISSION (assignments, hackathons, coursework)
   - OPPORTUNITIES (job/internship related)
   - PROMO (newsletter, marketing, spam)

Each category gets a Gmail label:
- `Important` → SUBMISSION  
- `Opportunities` → JOB/INTERNSHIP  
- `Promo` → PROMO emails  

---

# 🧠 Step-by-step Logic

## **1. Trigger**
- App: **Gmail**
- Event: **New Email **
  **2. AI Classification (Zapier Prompt Builder)**

### Prompt Used:
You are a strict email classifier.

Read the email content provided in {{email_body}} and classify it into EXACTLY one of these categories:

1.)SUBMISSION

2.)JOB/INTERNSHIP

3.)PROMOTIONAL/OTHER

Return ONLY the category name.

### Inputs Mapped:
- `email_body` → Gmail → **Body Html**

---

## **3. Keyword Fallback (Optional)**

If AI misses something, fallback keywords:
- "assignment"
- "submission"
- "hackathon"

Used inside Path rule groups.

---

## **4. Paths Logic**

### Path A: SUBMISSION
Condition:
AI Output Contains "SUBMISSION"
OR Body Contains "assignment"
OR Body Contains "submission"
OR Body Contains "hackathon"

Action:
- Gmail → Apply Label: **Important**

---

### Path B: OPPORTUNITIES
Condition:
AI Output Contains "JOB"
OR AI Output Contains "INTERNSHIP"


Action:
- Gmail → Apply Label: **Opportunities**

---

### Path C: PROMO
Condition:


AI Output Contains "PROMO"


Actions:
- Gmail → Apply Label: **Promo**
- (Optional) Gmail → Archive Email

---

# 📎 Screenshots

Screenshots for this Zap are in `/assets` folder.



### Search Query Used:
