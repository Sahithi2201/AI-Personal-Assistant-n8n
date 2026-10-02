# 🤖 AI Personal Assistant – n8n

An AI-powered personal assistant built with **n8n, Google Gemini, Gmail, and Google Calendar** that understands natural-language requests and performs real-world tasks through an intelligent conversational interface.

The assistant can send emails, view calendar events, create events, delete events, and respond to users through chat.

---

## 🌟 Project Overview

The **AI Personal Assistant** is an AI Agent-based automation system developed using **n8n**.

Instead of manually opening Gmail or Google Calendar, users can simply communicate with the assistant using natural language.

For example:

> "Show me my calendar events for tomorrow."

> "Create a meeting tomorrow at 10 AM for one hour."

> "Delete the Project Meeting from my calendar."

> "Send an email to my teammate with the subject Meeting Reminder."

The AI Agent understands the request and automatically selects the appropriate tool to perform the required action.

---

# 🎯 Objectives

The main objectives of this project are:

- Build an AI-powered personal assistant using n8n.
- Integrate Google Gemini with an AI Agent.
- Automate Gmail operations.
- Automate Google Calendar operations.
- Enable natural-language interaction.
- Use AI tool calling for task execution.
- Maintain conversation context using memory.
- Return task results directly through chat.

---

# ✨ Key Features

### 🤖 AI Agent
Understands natural-language requests and decides which tool should be used.

### 🧠 Google Gemini
Provides the natural-language understanding and reasoning capability of the assistant.

### 📧 Gmail Automation
Allows the assistant to send emails automatically.

### 📅 Google Calendar Automation
Supports:

- View calendar events
- Create calendar events
- Delete calendar events

### 🧠 Conversation Memory
Maintains conversation context during interactions.

### 💬 Chat Interface
Allows users to interact with the assistant using normal conversational messages.

### ⚡ Automated Tool Selection
The AI Agent automatically selects Gmail or Google Calendar based on the user's request.

---

# 🏗️ System Architecture

The overall system works as follows:

```mermaid
flowchart TD

    A["👤 User"] --> B["💬 Chat Interface"]

    B --> C["🤖 AI Agent"]

    C --> D["🧠 Google Gemini"]
    C --> E["🧠 Simple Memory"]

    C --> F{"🔍 Select Tool"}

    F --> G["📧 Gmail"]
    F --> H["📅 Google Calendar"]

    H --> I["📋 Get Events"]
    H --> J["➕ Create Event"]
    H --> K["🗑️ Delete Event"]

    G --> L["📨 Email Sent"]

    I --> M["📋 Calendar Information"]
    J --> N["✅ Event Created"]
    K --> O["🗑️ Event Deleted"]

    L --> P["💬 AI Response"]
    M --> P
    N --> P
    O --> P

    P --> Q["👤 User Receives Response"]
