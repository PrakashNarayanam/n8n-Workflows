# n8n-Workflows

This repository contains n8n workflow templates that use the **Google Gemini Chat Model** and the **AI Agent** node for various automation tasks.
The workflows are saved as `.json` files and can be easily imported into your n8n instance.

## Workflows

### **1. MAIL-REPLY.json (Gmail AI Auto-Reply Agent)**

This workflow is a simple AI agent designed to trigger on new emails, generate a reply, and then send it using the Gmail node.
* **Trigger:** **Gmail Trigger** (on new email)
* **Core Logic:** **AI Agent** node using the **Google Gemini Chat Model** and the **Send a message in Gmail** tool.
* **Purpose:** Automatically draft or send replies to incoming emails based on the AI's logic.

* <img width="996" height="351" alt="Screenshot 2025-10-25 121208" src="https://github.com/user-attachments/assets/a1c506be-1fed-4c67-8db0-bfa5f75ec792" />


### **2. Telegram event booking.json (Telegram Calendar Booking Agent)**

This workflow acts as a Telegram bot that can book events in Google Calendar based on conversational input from a user.
* **Trigger:** **Telegram Trigger** (on new message)
* **Core Logic:** **AI Agent** node using the **Google Gemini Chat Model**, **Simple Memory** for conversation history, and the **Create an event in Google Calendar** tool.
* **Purpose:** Allows users to interact with a Telegram bot to schedule events in their Google Calendar.

Here is the small video of how it works.
https://youtu.be/5_7ao5Aquag?si=2e1USZll94GIlPHE
