# mailclassifierAgent
# 📧 Email Intelligence Automation (Zapier + Notion)
A lightweight automation system that classifies incoming emails into categories and logs important ones into a Notion dashboard for easy tracking — built using Zapier, Gmail, Notion, and AI-powered classification.

---

## 🚀 What This Project Does
This automation solves a real student problem: **important emails getting lost** in a busy inbox.

Here’s what the system does:

### 1️⃣ Classifies every new email using AI
- **Submission** (assignment deadlines, project submissions, hackathon updates)  
- **Opportunities** (job mails, internship offers, recruiter updates)  
- **Promotional/Other** (newsletters, ads, spam)

### 2️⃣ Routes emails automatically using Zapier Paths
Each email is passed through:
- **Path 1: Submission**
- **Path 2: Opportunities**
- **Path 3: Promotional/Other**

Zapier Paths decide what happens next.

### 3️⃣ Auto-applies Gmail labels
- `Important` → For Submissions  
- `Opportunities` → For job/internship emails  
- `Promo` → For newsletters and advertisements  

### 4️⃣ Logs important emails into Notion
Each important email is saved automatically with:
- Subject  
- Sender  
- Category  
- Snippet  
- Received time  
- Direct Gmail link  

This creates a **clean Notion dashboard** where you can see all deadlines and opportunities in one place.

---

## 🛠 Tools & Technologies Used
| Tool | Purpose |
|------|---------|
| **Zapier** | Automation logic, AI text classification, Gmail triggers |
| **Gmail** | Email intake + labeling |
| **Notion** | Dashboard for tracking important emails |
| **AI Prompting** | Classify emails using structured categories |
| **Paths in Zapier** | Workflow segmentation |


## 📚 Workflow Architecture

---

## 📄 Notion Dashboard Structure
| Field | Type | Description |
|-------|------|-------------|
| Subject | Title | Email subject |
| From | Text | Sender name or email |
| Category | Select | Submission / Opportunity / Promo |
| Snippet | Text | Preview of the email body |
| Received At | Date | When the mail arrived |
| Gmail Link | URL | Opens the exact email in Gmail |

---

## ⚙️ Setup Instructions
1. Create a Notion database  
2. Create a new Zap in Zapier  
3. Add Gmail trigger with search query:  
4. Add AI classification step  
5. Add Paths for each category  
6. Add Gmail Label action inside each path  
7. Add Notion “Create Database Item” action  
8. Test & Activate

---

## 🎯 Why I Built This  
As a college student, I often missed important assignment and internship emails because my inbox was flooded.  
So I built a smart, automated solution to:
- Reduce inbox noise  
- Highlight important deadlines  
- Track job/internship mails  
- Stay consistent and organized  

---

## 🔍 Future Improvements
- Telegram real-time notifications  
- Weekly digest email  
- Priority scoring model  
- Google Sheets integration  
- Add a UI dashboard  

---

## 👤 Author
**Khushi Jha**  
Automation Enthusiast | Student   

---

## 🤝 Contributions
Pull requests, improvements, and suggestions are welcome!



