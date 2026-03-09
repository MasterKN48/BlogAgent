# Blog Creating Agent: Self-Hosted & Open Source Learning Project

This repository contains a comprehensive learning project plan to build an advanced AI agent system for blog creation. The system leverages a 100% free, open-source, and self-hostable technology stack.

## 🚀 Project Vision

An end-to-end platform using **Next.js**, **FastAPI**, and **LangGraph** to research, draft, and optimize blog content, featuring multimedia generation and mission-critical observability.

---

## 🛠 Self-Hosted Tech Stack

- **Frontend:** Next.js (React)
- **Backend:** FastAPI (Python)
- **Agent Orchestrator:** LangGraph
- **Database/Vector Store:** PostgreSQL with `pgvector`
- **Search Engine:** SearXNG
- **Observability:** Opik
- **LLM Inference:** Ollama / LM Studio (Local models like Llama 3, Qwen 2.5)
- **Audio/TTS:** Coqui XTTS v2 or Bark

---

## 📅 Roadmap & Phases

### Phase 1: Foundations & Orchestration

_Goal: Build a functional agent with self-hosted research and tracing._

- **Backend Setup:** Initialize FastAPI and PostgreSQL with `pgvector`.
- **Frontend Setup:** Create a Next.js multi-session chat interface.
- **LangGraph Integration:**
  - **Planner Node:** Generates outline from title.
  - **Research Node:** Fetches data via local **SearXNG**.
  - **Writer Node:** Drafts blog using local LLMs.
- **Observability:** Trace every agent step using a self-hosted **Opik** dashboard.

### Phase 2: Corrective RAG & Authentication

_Goal: Enhance reliability and add basic security._

- **User Authentication:** Simple JWT-based Login/Signup flow in Next.js and FastAPI.
- **Corrective/Self-RAG:**
  - **Grader Node:** LLM evaluates the relevance of research results.
  - **Fallback Loop:** Re-queries SearXNG or rewrites search terms if initial results are poor.
- **Semantic Caching:** Store research in `pgvector` to avoid redundant external searches.

### Phase 3: Human-in-the-Loop & Context

_Goal: Improve precision through user collaboration._

- **Human-in-the-Loop:** Implement LangGraph breakpoints for outline approval/editing before drafting.
- **Document Context:** Allow users to upload PDFs or Markdown files to guide the agent's research.
- **Evaluation Loop:** Use Opik logs to refine prompts based on real-world performance.

### Phase 4: Multimedia & Autonomous Agents

_Goal: Deep-level features for a complete content ecosystem._

- **Podcast Generation:** Integrated TTS (Coqui/Bark) to convert blogs into multi-speaker audio podcasts.
- **Autonomous SEO Agent:** A background worker tracking trends via SearXNG to suggest blog updates.
- **Social Media Distribution:** Automated generation of Twitter/LinkedIn threads from the main blog.

---

## 💡 Advanced Learning Suggestions

- **Multi-modal Agents:** Teach the agent to describe images within user documents to enhance content.
- **LoRA Fine-tuning:** Use Opik's refined datasets to fine-tune a small local model for a specific "voice."
- **Streaming UI:** Use Server-Sent Events (SSE) to show the agent's "chain of thought" in real-time.
