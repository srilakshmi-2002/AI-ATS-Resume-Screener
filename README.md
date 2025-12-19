# 🤖 AI-Powered ATS Resume Screener & Automation

This project is a fully automated recruitment workflow built with **n8n**. It uses **Google Gemini AI** to screen resumes received via **Telegram** and automatically manages candidate data in **Google Sheets**.

## 🚀 How it Works
1. **Input:** Candidates send their resume (PDF or ZIP) to a Telegram Bot.
2. **Processing:** 
   - The workflow identifies the file type.
   - For ZIP files, it extracts and loops through multiple resumes.
   - For PDF files, it extracts the text directly.
3. **AI Analysis:** **Google Gemini LLM** analyzes the resume, extracts contact details, and assigns an **ATS Score** based on industry standards.
4. **Decision Logic:** 
   - **Score > 70:** Candidate is "Accepted" and logged into the 'Accepted' Google Sheet.
   - **Score < 70:** Candidate is "Rejected" and logged into the 'Rejected' Google Sheet.
5. **Feedback:** The bot sends an instant personalized message to the candidate via Telegram with their score and status.

## 🛠️ Tech Stack
- **Workflow Orchestration:** [n8n](https://n8n.io/)
- **AI Model:** Google Gemini (Generative AI)
- **Messaging API:** Telegram Bot API
- **Database/Tracking:** Google Sheets
- **Custom Logic:** JavaScript (n8n Code Nodes)

## 📁 Project Structure
- `My workflow.json`: The complete n8n workflow export.
- `README.md`: Project documentation.

## ⚙️ Setup Instructions
1. Import the `My workflow.json` into your n8n instance.
2. Configure credentials for:
   - Telegram API (via BotFather)
   - Google Gemini API (via Google AI Studio)
   - Google Sheets API (via Google Cloud Console)
3. Activate the workflow and start the Telegram Bot.

---
**Developed by:** [Your Name]
