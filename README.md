# 🚀 AI Agent Framework 

## 📌 Introduction

This repository contains an **AI Agent Framework** designed to demonstrate **agentic AI principles** such as reasoning, policy-based decision-making, skill execution, and lifecycle management using **Large Language Models (LLMs)**.

The framework emphasizes **clarity, modularity, and extensibility**, making it suitable for:

- Learning agentic AI concepts  
- Building enterprise AI agents  
- Integrating with workflow engines like **n8n**  
- Extending into multi-agent systems  

---

## 🎯 Objectives

- Build a **true AI agent**, not just a chatbot  
- Separate **decision-making** from **execution**  
- Enforce **policy-driven control**  
- Provide a clean foundation for future extensions such as memory, tools, and governance  

---

## 🧠 What Is an AI Agent in This Framework?

An AI agent in this framework:

- Receives a goal (context)  
- Evaluates the goal using policies  
- Selects an appropriate skill  
- Executes the skill using an LLM  
- Returns a controlled and validated output  

---

## 📂 Project Structure

```bash
ai-agent-framework/
├── agent.py          # Agent orchestrator
├── states.py         # Agent state definitions
├── policies.py       # Decision & governance logic
├── skills.py         # Agent capabilities (tools)
├── llm_client.py     # LLM abstraction & retries
├── main.py           # Entry point
├── test_memory.py    # Repeated execution demo
└── list_models.py    # Model inspection utility


🧱 Core Components Explained
1️⃣ Agent Orchestrator (agent.py)
Central controller of the agent

Manages execution flow

Applies policies and invokes skills

Key Responsibility:

Coordinate reasoning and action safely.

2️⃣ State Management (states.py)
Defines agent lifecycle states

Currently supports:

idle

active

Why it matters:
States enable future features such as pausing, retries, and multi-step workflows.

3️⃣ Policy Engine (policies.py)
Decides what the agent is allowed to do

Acts as a governance layer

Prevents uncontrolled or unsafe execution

Enterprise Value:
Policies ensure predictable and auditable AI behavior.

4️⃣ Skills (skills.py)
Represent agent actions (tools)

Encapsulate business logic

Easily extendable

Example Skills:

Content generation

API invocation

Database queries (future)

5️⃣ LLM Client (llm_client.py)
Abstracts LLM interaction

Handles retries and failures

Decouples agent logic from model providers

Supports easy replacement with:

OpenAI

Azure OpenAI

Local models

6️⃣ Entry Point (main.py)
Demonstrates how to run the agent

Serves as a CLI or integration example

🔁 Execution Flow
Input context is received

Agent state is initialized

Policy engine evaluates the request

Skill is selected

LLM is invoked

Output is returned

🔐 Safety & Control
Skills execute only via policy approval

LLM access is isolated

Clear control boundaries are enforced

Ready for enterprise governance extensions

🚀 Future Enhancements
Memory (vector databases)

Tool orchestration

Multi-agent collaboration

Workflow integration (n8n)

Observability and logging

📝 One-Line Summary
This AI Agent Framework demonstrates how to build policy-controlled, modular, and extensible agentic AI systems using LLMs.
