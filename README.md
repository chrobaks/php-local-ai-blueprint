# php-local-ai-blueprint
Open-source collaboration blueprint for a local PHP/Symfony AI analyzer. Looking for Python &amp; Symfony enthusiasts!

# 🛡️ On-Premise PHP AI Analyzer (Project Conceptual Blueprint)

Welcome! This is a **public discussion and architecture repository** for an upcoming, fully local, and data-sovereign AI code intelligence platform. 

> ⚠️ **Note:** The core Symfony/EasyAdmin application code is kept in a **private repository** to protect the architecture and prevent generic commercial exploitation. This repository serves as the public entry point for community discussion, architecture feedback, and co-founder/contributor matching.

---

## 🎯 The Vision

Modern AI coding assistants (like Copilot or Cloud APIs) are powerful but pose a massive **data privacy risk** for businesses in the DACH region. Proprietary source code is a company's core intellectual property. Many development teams are legally or strategically prohibited from uploading their repositories to external cloud servers.

**Our Goal:** Build a 100% On-Premise tool that combines classic static code analysis with local Large Language Models (LLMs via Ollama) running entirely on internal company hardware. 

---

## 🏗️ Technical Architecture & Stack

The system is designed as a decoupled, high-performance microservice pipeline:

1. **Frontend / Core (PHP):** Built with **Symfony 8.0** and **EasyAdmin 5** (Private Repo). This handles multi-tenancy, repository management, and the async job dashboard.
2. **Static Analysis (PHP):** Automatically extracts hard metrics and structures (via PHPStan) into a local PostgreSQL database.
3. **AI Pipeline (Python):** An independent background service that ingests the pre-structured PHPStan data, runs a local RAG (Retrieval-Augmented Generation) loop, and queries an offline **Ollama** server (`llama3.1`) to generate context-aware refactoring and security recommendations.

---

## 📊 Data Interface Specification (PHP ➔ Python)

To allow contributors to work completely independent of the private Symfony codebase, the data contract between PHP and Python is fully specified via JSON. 

You can view the compact data payload structure here:
👉 **[Click here to view the JSON Specification Blueprint](interface_spec.json)**

---

## 🤝 Join the Project (Munich-based or Remote)

This project is driven by pure passion for Open Source, data sovereignty, and local AI architecture. There is **no commercial pressure** and no corporate overhead. It’s about building a robust tool for the PHP community and geeking out over local LLMs.

### Who we are looking for:
- 🐘 **Symfony Developers:** To help optimize the async Messenger queues, DB migrations, and EasyAdmin UI workflows.
- 🐍 **Python & AI Enthusiasts:** To build out the local RAG pipelines, chunking strategies, and vector embeddings (ChromaDB).
- 💡 **Munich Locals:** The project is rooted in Munich. If you are around, let's meet up for a Spezi/Beer to spin some ideas!

---

## 💬 How to Connect & Contribute

Since the code is private, **the best way to get involved is through GitHub Discussions:**

1. Click on the **[Discussions](../../discussions)** tab at the top of this repository.
2. Introduce yourself or share your thoughts on the JSON spec.
3. If we are on the same wavelength, we can set up a quick call or meet up in Munich, and I'll grant you access to isolated development tasks.

*This concept blueprint is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)** to protect the community's collective ideas.*
