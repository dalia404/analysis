# Autonomous Gold Market Intelligence Agent

An agentic AI system designed to analyze gold-market signals by combining external search, Google Sheets context, memory, and automated n8n workflows.

---

## Overview

The system operates as an automated n8n agentic workflow that receives user requests via a Webhook, processes them through an AI Agent powered by the Google Gemini Chat Model, dynamically executes attached tools, and returns a structured response back to the user interface.

---

## Architecture Diagram

```text
Webhook (User Request Input)
     ↓
AI Agent
     ├── Model: Google Gemini Chat Model
     ├── Memory: Simple Memory
     └── Tools:
           ├── Search google in SearchApi
           ├── Get row(s) in sheet in Google Sheets
           └── Call n8n Workflow Tool
     ↓
Respond to Webhook1 (Response Output)
