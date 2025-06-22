# 🤖 Multi-AI Agent System with YouTube Channel Tool (CrewAI)

A modular, agent-based system that automates YouTube content analysis and blog generation using **CrewAI** and **LLMs**. This project uses a custom YouTube tool to fetch transcripts from a channel and deploys multiple autonomous agents to handle research, writing, and editing — **without storing any data**.

---

##  Overview

This project demonstrates how **autonomous AI agents** can collaborate using tools, tasks, and roles to generate high-quality content from YouTube video transcripts. It leverages:

-  **CrewAI** for agent orchestration  
-  **YouTube Transcript API** for transcript retrieval  
-  **OpenAI GPT** for reasoning and writing tasks  
-  No persistent storage (no vector DB, no local cache)

---

##  Core Features

| Feature                | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| 🎥 YouTube Tool        | Fetches transcripts from latest videos in a channel                         |
| 👥 CrewAI Agents       | Multi-agent setup with research, writing, and editing roles                 |
| 📄 Blog Generation     | Automatically creates a blog post based on video content                    |
| 🧰 Task Delegation     | Each agent has its own tool, task, and independent reasoning                |
| ⚡ Lightweight          | Stateless & memory-free — perfect for quick, throwaway RAG-style runs       |

---

## 🏗️ System Architecture

```mermaid
flowchart TD
    A[YouTube Channel URL] --> B[Transcript Extraction Tool]
    B --> C[Research Agent]
    C --> D[Writer Agent]
    D --> E[Editor Agent]
    E --> F[Final Blog Output]

