 Project Overview: AI-Powered Video Creation Pipeline
This project automates the entire short-form video creation pipeline using a combination of AI tools and no-code automation. The system transforms rough content ideas into polished scripts and full videos — with minimal human involvement, only needed for final approval.

 Workflow Summary:
Input Ideas
Content ideas are submitted into a Google Sheet.

Script Generation (AI)
Using OpenAI, each idea is converted into a compelling short-form video script in fluent, engaging American English.

Approval Step
The system waits for manual approval inside the same sheet. Only approved scripts proceed further.

Video Generation (Auto)
Once approved, a vertical 9:16 video is auto-generated using HeyGen, featuring a preset avatar and voice.

Smart Filtering
Ideas marked as rejected or pending are automatically skipped or paused.

🛠️ Tools Used:
n8n – Core automation engine that manages the entire flow from Sheets to video output.

Google Sheets – Acts as the content database and approval dashboard.

OpenAI – Enhances and formats content ideas into professional video scripts.

HeyGen – Converts approved scripts into high-quality avatar-led videos with voiceovers.
Setup Instructions
✅ Prerequisites
Before using this workflow, make sure you have:

n8n account 
→ Sign up or install n8n

Google Account with:

Access to Google Sheets

A Sheet with:

Column A: Idea's

Column B: Generated Script

Column C: Approval Status

Tavily API Key
→ Get a free key for AI-powered search.

OpenAI or Gemini API Key
(You're currently using Google Gemini through LangChain. Make sure you’ve connected it in n8n.)

HeyGen API Key
→ Apply for an API Key

📦 Installation Steps
1. Import the Workflow into n8n
Open your n8n editor.

Click “Import” in the top-right menu.

Upload Idea_s_to_script.json.

Save the workflow.

2. Set Up Google Sheets Integration
Go to the Google Sheets Trigger node.

Authenticate with your Google account.

Select your spreadsheet and sheet tab (already prefilled if using the provided template).

3. Configure API Keys
In these nodes, update your API credentials:

🔎 Tavily API

Node: Search Internet

Replace api_key in the JSON body with your actual key.

🧠 Google Gemini (LLM)

Node: Google Gemini Chat Model

Use your Gemini credentials set in n8n.

🗣  HeyGen API

Node: HTTP Request

Replace the "X-API-KEY" header with your actual HeyGen API key.

4. Set Up Your Google Sheet
Make sure the column headers match:

Idea's

Generated Script

Approval Status (set to “Approved” to trigger video creation)

5. Run or Activate the Workflow
You can trigger manually or set the workflow to active so it watches for changes in your sheet.

Approved ideas will auto-generate HeyGen videos.

Rejected or pending ones will be skipped.


