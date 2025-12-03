# UCCE-Context-Engine
A framework for advanced, User-Centered Context Engineering (UCCE). Solves Context Bleeding by giving users Control and Transparency over AI memory management.
This is a comprehensive, well-structured `README.md` designed for a top-tier open-source project. It includes all necessary sections to attract users, document the architecture, and guide potential contributors.

# 🧠 UCCE-Context-Engine: User-Centered Context Engineering

**A principled framework for providing explicit user control and transparency over the AI's contextual memory, designed to prevent Context Bleeding and enhance trust.**

<p align="center">
  <a href="https://github.com/YourUsername/UCCE-Context-Engine/stargazers">
    <img src="https://img.shields.io/github/stars/YourUsername/UCCE-Context-Engine?style=flat-square&color=blue" alt="GitHub stars">
  </a>
  <a href="https://github.com/YourUsername/UCCE-Context-Engine/issues">
    <img src="https://img.shields.io/github/issues/YourUsername/UCCE-Context-Engine?style=flat-square&color=red" alt="GitHub issues">
  </a>
  <a href="https://github.com/YourUsername/UCCE-Context-Engine/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Python-3.9+-blue?style=flat-square" alt="Python Version">
  </a>
</p>

---

## 💡 The Problem: Context Bleeding

Modern AI systems are often "too smart" because they leverage irrelevant or outdated information from broader memory to answer a current query, leading to misaligned, frustrating, or incorrect outputs—a phenomenon known as **Context Bleeding**.

For example, asking for a chocolate cake recipe right after debugging a Python banking app can lead the AI to suggest a recipe formatted as a "secure, enterprise-grade chocolate cake class formatted in Python". This is a fundamental flaw impacting business outcomes and user trust.

## ✨ The Solution: UCCE-Context-Engine

The **UCCE-Context-Engine** addresses this by applying User-Centered Design (UCD) principles to context management. We aim to move AI from a black box to a transparent, controllable assistant.

Our framework provides the architectural components necessary to implement:

1.  **Transparency:** Making it clear what context the AI is considering.
2.  **Control:** Allowing users to define the boundaries of the AI's memory.
3.  **Scoped Context:** Enabling the AI to operate within specific, user-defined "memory zones" (Session, Project, Global).
4.  **Graceful Reset:** Providing easy ways to "clear" or "isolate" context without starting over.

## 🏗️ Architecture Overview

The UCCE-Context-Engine is structured into three main phases mirroring the flow of user interaction, with the new **Memory Manager** and **Control & Feedback** layers serving as the core innovation.

| Phase | Component Focus | Key Files/Modules | Solves | UCD Principle |
| :--- | :--- | :--- | :--- | :--- |
| **I. Context Gathering** | Data Definition & Storage | `context_models/`, `context_storage/` | Defines the structure of memory (context). | Foundation |
| **II. Dynamic Contextualization** | **UCCE Intelligence (Memory Manager)** | `memory_manager/` | **Context Bleeding** via isolation and pruning. | Reliability |
| **III. Personalized Response** | **User Control & Feedback** | `control_feedback/` | **Lack of Control** via explicit UI/API toggles. | Control & Transparency |

### Deep Dive into the Innovation Layers

#### 🧠 1. `/src/memory_manager` (UCCE Intelligence)
This layer is the gatekeeper of context, handling all logic to ensure only relevant information is passed to the LLM (Large Language Model).

| Module | Purpose | Solves the Problem of... |
| :--- | :--- | :--- |
| `agent_isolation.py` | Manages separate context windows for different Task IDs (e.g., Python Debugging vs. Recipe finding). | Context Bleeding |
| `pruning.py` | Implements strategic forgetting by removing outdated or low-relevance data segments. | Context Rot & Token Waste |
| `summarization.py` | Compresses long conversational history into concise, token-efficient summaries. | "Lost in the Middle" (Long Contexts) |
| `retriever.py` | Uses RAG/vector embeddings to fetch only the semantically most relevant context segments. | Efficiency & Accuracy |

#### 🗣️ 2. `/src/control_feedback` (User-Centered Layer)
This layer ensures the user has a view into, and control over, the memory system, implementing the "Context Scope Wireframe" principle.

| Module | Purpose | UCD Principle Implemented |
| :--- | :--- | :--- |
| `scope_toggles.py` | [cite_start]Defines and handles user commands for changing scope: `SESSION`, `PROJECT`, `GLOBAL`. | Control & Scoped Context |
| `context_inspector.py` | [cite_start]Packages the currently active context for visualization in a UI, acting as the "Active Memory Inspector". | Transparency |
| `override_handler.py` | [cite_start]Processes user commands to manually correct, inject, or reset context (e.g., "Ignore everything before 2pm"). | Graceful Reset |

---

## 💻 Getting Started

### Prerequisites

* Python 3.9+

### Installation (via pip)

*(Note: Once packaged, instructions will be updated. For now, use local setup.)*

```bash
# Clone the repository
git clone [https://github.com/YourUsername/UCCE-Context-Engine.git](https://github.com/YourUsername/UCCE-Context-Engine.git)
cd UCCE-Context-Engine

# Setup virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies (This is the basic setup)
pip install -r requirements.txt 
````

### Running the Demo

See the `examples/` directory for executable scripts that demonstrate the UCCE principles in action.

**Example: Context Bleeding Prevention**

```bash
python examples/demo_context_bleeding.py
```

This script will first simulate a long "Work Task" (Context Bleeding) and then show how a user-initiated **Scope Toggle** (Control) isolates the context to get a correct, non-technical answer.

-----

## 🤝 How to Contribute

This project is in its early stages and we warmly welcome contributions from developers, researchers, and UX designers\!

### High-Priority Contribution Areas:

1.  **`memory_manager` Implementation:** Implementing the core logic in `agent_isolation.py` and token-efficient `summarization.py`.
2.  **API Design:** Refining the interface between the `Context Engine` and the downstream `LLM` or `Decision Maker/Orchestrator` [see architecture image].
3.  **UI/UX Proof-of-Concept:** Creating a simple web or terminal interface (e.g., Streamlit, FastAPI/React) to demonstrate the **Active Memory Inspector** and **Scope Toggles** in action.

### Contribution Process

1.  Fork the repository.
2.  Create your feature branch (`git checkout -b feature/AmazingFeature`).
3.  Commit your changes (`git commit -m 'feat: Add AmazingFeature'`).
4.  Push to the branch (`git push origin feature/AmazingFeature`).
5.  Open a Pull Request.

Please refer to the `CONTRIBUTING.md` (To Be Added) for detailed guidelines.

-----

## 🗺️ Roadmap & Future Vision

The UCCE-Context-Engine is designed for growth, addressing advanced challenges in Context-Aware and Ubiquitous Computing.

  * **Multi-Modal Context:** Extend models to handle non-text inputs (images, audio snippets) as contextual data.
  * **Proactive/Calm Computing:** Implement logic for Non-Intrusive Adaptation, adhering to Mark Weiser's "Calm Technology" principle.
  * **Low-Code Customization:** Develop a simple Domain Specific Language (DSL) that allows non-developers to define high-level context rules (e.g., "IF I'm on my work Wi-Fi THEN set activity=Work").
  * **Federated Context:** Integrate secure, privacy-preserving methods for contextualizing across multiple user devices without centralizing all data.

-----

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

## 🧑‍💻 Contact

KALDJOB Guillaume Emmanuel / KGEmmanuel 

Project Link: [https://github.com/KGEmmanuel/UCCE-Context-Engine](https://www.google.com/search?q=https://github.com/KGEmmanuel/UCCE-Context-Engine)

```
```
