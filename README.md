# Primovis Agent Solution

The **Primovis Agent** is a Microsoft Power Platform (Copilot Studio) solution designed to showcase **agent workflows** with multiple tools, AI integration, and conversational management.  
This package provides reusable components, workflows, and topics for building intelligent, automated agents.

---

## 📦 Solution Contents

### 1. Core Solution Files
- `solution.xml` – Solution manifest  
- `customizations.xml` – Metadata for entities, components, and configurations  
- `[Content_Types].xml` – Internal solution content definitions  

### 2. Workflows
Located under `/Workflows/`:
- `CoAExample-3Agent-*.json` → Demonstrates **agent orchestration**  
- `CoAExample-3Tool-*.json` → Demonstrates **tool execution and integration**  

### 3. Bot Components
Located under `/botcomponents/`, includes:
- **Actions**  
  - `Output3Flow` → Handles agent output formatting and responses  
- **GPT Integration**  
  - `gpt.default` → Default GPT-powered reasoning and response generation  
- **Core Topics**  
  - `ConversationStart`, `StartOver`, `ResetConversation`  
  - `Greeting`, `Goodbye`, `ThankYou`  
  - `Escalate`, `Fallback`, `OnError`, `MultipleTopicsMatched`  
  - `EndOfConversation`, `Signin`, `Search`  

### 4. Bot Configuration
- `bots/cra6b_primovisAgentForEx3/configuration.json` → Bot settings  
- `bots/cra6b_primovisAgentForEx3/bot.xml` → Agent definition and metadata  

### 5. Assets
- `Assets/botcomponent_workflowset.xml` → Defines workflows linked with bot components  

---

## 🚀 Features

- **Agent-Oriented Design**: Orchestrates multiple workflows and tools  
- **Tool Execution**: Supports modular tool integration (e.g., data lookups, processing flows)  
- **AI Integration**: GPT-powered reasoning embedded in agent conversation  
- **Error Management**: Dedicated error-handling topics and escalation paths  
- **Reusability**: Modular bot components for different business scenarios  

---

## 🛠 Installation

1. Download the solution package (`PrimovisAgent_1_0_0_1.zip`).  
2. Open **Power Platform Admin Center** → **Solutions**.  
3. Select **Import Solution** and upload the `.zip` file.  
4. Publish all customizations after import.  

---

## 📖 Usage

1. Open **Copilot Studio / Power Virtual Agents**.  
2. Access the bot named **Primovis Agent**.  
3. Interact with the agent using natural language.  
4. The agent can:  
   - Trigger workflows (`CoAExample-3Agent`, `CoAExample-3Tool`)  
   - Route to tools and handle their outputs  
   - Manage conversations with fallback, escalation, and error recovery  

---

## ⚠️ Error Handling

The agent provides robust error handling via:
- `OnError` topic → Captures failures  
- `Fallback` topic → Handles unrecognized queries  
- `Escalate` topic → Transfers to a human agent or external process  

---

## ✅ Quality Standards

- **Reliability** → Ensures safe recovery from errors  
- **Reusability** → Modular bot components for extension  
- **Consistency** → Unified conversation patterns (Greeting → Task → Close)  
- **AI-Powered** → Uses GPT integration for unstructured input reasoning  

---

## 📜 License
This solution is distributed under your organization’s Microsoft Power Platform licensing terms.

---
