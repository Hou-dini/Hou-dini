# Hi, I'm Eli 👋

**Applied AI Engineer** focused on building production-oriented AI systems that automate real-world workflows.

I design and deploy multi-agent systems that move beyond prototypes into **reliable, task-oriented tools**.

---

## 🚀 Featured Project: Project Mirror

**Project Mirror** is a multi-agent AI system designed to act as a professional assistant—handling tasks like information retrieval, scheduling, and technical reasoning through coordinated agent workflows.

👉 It demonstrates how AI systems can operate in **real environments**, where outputs directly influence decisions and actions.

### 🎬 Demo

<p align="center">
   <img src="https://raw.githubusercontent.com/Hou-dini/project-mirror-overview/main/agentic_portfolio_demo.gif?raw=true" width="750" alt="Project Mirror"/>
</p>

*Short walkthrough demonstrating multi-agent coordination, task execution, and real workflow automation.*

### 🔑 Key Capabilities
- Multi-agent orchestration for complex task execution  
- Retrieval-augmented reasoning (RAG) with strict context isolation  
- Real-world tool integration (e.g., scheduling via APIs)  
- Structured outputs and validation for reliability  
- Observability into system behavior and failure modes  

### 🧠 Why it matters
Most AI projects demonstrate isolated capabilities.  
Project Mirror focuses on **system reliability, coordination, and real usability**.

---

## 🏗️ Architecture

Project Mirror employs a hierarchical orchestration pattern where a high-reasoning "Nexus" agent manages a fleet of specialized sub-agents.

```mermaid
graph TD
    User([User]) <--> Frontend[Next.js 16 / Tailwind CSS 4]
    Frontend <--> API[FastAPI Backend]
    
    subgraph "MAS Orchestration (Google ADK)"
        API <--> Nexus{Nexus Orchestrator<br/>Gemini 3.1 Flash-lite}
        Nexus -- "Delegation / Handoff" --> Researcher[Researcher Agent<br/>Llama 3.3 70B]
        Nexus -- "Delegation" --> TechLead[Technical Lead Agent<br/>Gemini 3 Flash]
        Nexus -- "Delegation" --> DemoSpec[Demo Specialist<br/>Scenario Runner]
        Nexus -- "Tool Call (MCP)" --> Scheduler[Scheduler Agent<br/>Google Calendar]
    end

    subgraph "Knowledge & Tools"
        Researcher <--> VectorDB[(Weaviate Vector DB)]
        Researcher <--> Search[Google Search API]
        DemoSpec <--> MockData[(Isolated Demo Contexts)]
        Scheduler <--> Calendar[(Google Calendar API)]
    end

    subgraph "Reliability Layer"
        Nexus -.-> RedTeam[Adversarial Red-Team]
        RedTeam -.-> Guardrails[Pydantic Validation]
        Guardrails -.-> Nexus
    end
```
---
## Repository

Project overview and supporting documentation:
[https://github.com/Hou-dini/project-mirror-overview](https://github.com/Hou-dini/project-mirror-overview)

---

## 🧪 Additional Project: Kognia AI

**Kognia AI** is a hierarchical multi-agent system for autonomous research synthesis and structured reasoning.

<p align="center">
   <img src="https://raw.githubusercontent.com/Hou-dini/Hou-dini/main/kognia demo.gif?raw=true" width="750" />
</p>

- Automated research workflows using agent coordination  
- Real-time orchestration visibility and logging  
- Structured reasoning pipelines for consistency  

➡️ [Source Code](https://github.com/Hou-dini/kognia_backend)

---

## ⚙️ What I Focus On

- Designing **multi-agent systems** that handle real tasks  
- Improving **LLM reliability** through validation and grounding  
- Building systems that balance **latency, cost, and accuracy**  
- Turning complex workflows into **usable AI tools**  

---

## 🛠️ Tech Stack

**AI / Systems**
- Multi-agent orchestration (Google ADK, MCP)  
- RAG systems (Weaviate, structured outputs)  
- Model routing and evaluation  

**Backend**
- Python (FastAPI, asyncio)  
- REST APIs, microservices  

**Data**
- PostgreSQL, MongoDB  
- Vector databases (Weaviate)  

**Infra**
- Docker, CI/CD (GitHub Actions)  
- Cloud deployment (GCP, Vercel)  

---

## 📫 Contact

- Email: elikplimkudowor@gmail.com  
- LinkedIn: https://linkedin.com/in/elikplim-kudowor  

---
