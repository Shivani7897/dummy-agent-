# 🤖 n8n AI Personal Assistant Workflow

## 🚀 Overview

This project is an **AI-powered automation workflow built using n8n** that acts as a personal assistant.

It can handle multiple tasks like:

* Managing expenses
* Sending & reading emails
* Creating and managing tasks
* Google Calendar operations
* Document handling
* Web search queries

---

## ⚙️ Features

* 🧠 AI Agent using Google Gemini
* 📅 Google Calendar integration (create & fetch events)
* 📧 Gmail automation (send & read emails)
* 💰 Expense tracking using Google Sheets
* 📝 Notes & document management
* ✅ Task creation, deletion & tracking
* 🔍 Web search capability
* 🧮 Built-in calculator tool

---

## 🏗️ Workflow Architecture

1. **Webhook Trigger**
2. **AI Agent (Gemini Model + Memory)**

### Connected Tools:

* Google Calendar
* Gmail
* Google Sheets (Expenses)
* Task Manager
* Docs Manager
* Calculator
* Search API

3. **Respond to Webhook**

---

## 📥 Input Format

Send a POST request to webhook:

```json
{
  "query": "Add expense of 200 for food"
}
```

---

## 📤 Output

* Returns AI-generated response
* Executes action (like adding expense / sending email / creating task)

---

## 🛠️ Setup Instructions

### 1. Install n8n

* Use Docker / npm / desktop app

### 2. Import Workflow

* Download `workflow.json`
* Import into n8n

### 3. Configure Credentials

You need to set up:

* Google Account (OAuth2)

  * Google Sheets
  * Gmail
  * Calendar
* Google Gemini API (if used)
* Any Search API (if configured)

---

### 4. Update Nodes

Replace:

* Google Sheet ID
* Document IDs
* Task configurations

Also ensure:

* Column names match in Google Sheets

---

### 5. Activate Workflow

* Enable workflow
* Test via webhook
