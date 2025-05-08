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


