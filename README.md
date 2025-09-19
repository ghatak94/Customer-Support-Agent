# 💬 Support Chat Ticketing System  

A no-code Support Chat automation built using n8n, which allows users to submit their issues through a chat interface. The chatbot automatically creates a support ticket, assigns it to an available agent, updates the database, and notifies the assigned agent via email.

---

## 🚀 Features
📝 Chat Interface – Users can describe their issue in a chat form.
🎫 Auto Ticket Generation – Each submitted issue creates a new ticket record.
👩‍💻 Agent Availability Check – System checks which agents are available.
📍 Auto Assignment – Assigns the ticket to an available agent dynamically.
📬 Agent Notification – Sends an email to the assigned agent with ticket details.
📊 Database Update – Keeps all ticket data and agent assignment updated in your database.
⚡ Built on n8n – Fully no-code and automation-based.

---

## ⚙️ Workflow Overview

Here’s the flow of the automation:

1. Trigger (Webhook/Form) – User submits a support query from chat.
2. Create Ticket – A new row is created in the ticket database (like 3.Airtable or Google Sheets).
3. Search Available Agent – Looks up the agent availability table.
4. IF Node –

✅ If available →
Set assigned agent
Update ticket record
Send email notification to agent
Respond to chat confirming assignment

❌ If not available →
Send fallback message (e.g. “No agent available, we’ll contact you soon”)
Keep the ticket as unassigned for later follow-up.
End Workflow – Ticket is created and tracked.

## 🛠 Tech Stack
---
1. n8n – Workflow automation
2. Airtable / Google Sheets – Ticket & agent database
3. Gmail / Outlook – For email notifications
4. Webhook Forms / Chat Widget – To collect user input

---

## 🚀 How to Use

---

1. Clone this workflow into your n8n instance.
2. Create 2 database tables:
3. Tickets (ticket_id, user_name, user_email, issue, assigned_agent, status)
4. Agents (agent_name, email, availability)
5. Connect credentials for your database and email.
6. Deploy the workflow and embed the chat form on your site.
7. Start receiving tickets automatically!

---


## 📄 License
This project is licensed under the MIT License.  
