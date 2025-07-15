📄 My Sub-workflow
This repository contains an n8n sub-workflow that integrates AI-powered conversation handling with Gmail to automatically respond to chat messages.

✨ Features
✅ Listens for incoming chat messages via a webhook
✅ Uses Google Gemini (PaLM) as the AI language model to generate responses
✅ Automatically composes and sends emails with Gmail
✅ Modular and easily extendable for additional actions

🛠️ Workflow Overview
This workflow includes the following main components:

Chat Trigger

Starts the workflow when a new chat message is received.

Google Gemini Chat Model

Processes and understands the message using AI.

AI Agent

Orchestrates the flow, combining language understanding and tools.

Gmail Tool

Sends emails based on AI-generated content.

🔗 Node Connections
From	To	Purpose
Chat Trigger	AI Agent	Begin processing the chat message
Google Gemini Chat Model	AI Agent	Provide natural language replies
Gmail Tool	AI Agent	Send generated emails

⚙️ Configuration
Credentials Required:

Google Gemini API
Configure your PaLM (Gemini) API credentials in n8n.

Gmail OAuth2
Set up Gmail OAuth2 credentials to enable email sending.

Webhook Setup:

The chat trigger uses this webhook ID:
2aedd0ad-6b6d-4bfd-858c-be439fae8cc7

Make sure to register this endpoint with your chat application or webhook provider.

🧩 Example Use Case
✅ A new chat message is received, e.g.:
“Can you send me the latest update?”

The workflow will:

Use Gemini to draft a response and generate an email

Populate the recipient, subject, and message body automatically

Send the email through Gmail

🚀 Deployment
Import My Sub-workflow.json into your n8n instance.

Configure your credentials.

Activate the workflow.

Register the webhook URL in your chat platform.

Test by sending a message.

📂 File Structure
nginx
Copy
Edit
My Sub-workflow.json     # Workflow definition
README.md                # Project documentation
📝 License
This project is provided for educational and demonstration purposes. Ensure compliance with Google and OpenAI API usage policies.
