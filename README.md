# ⚖️ Legal Management Platform - Wills Module (Enterprise Showcase)

> **🔒 Proprietary & Confidential:** This is a commercial, enterprise-grade platform built for a legal firm. To protect client data and comply with POPIA, the source code is strictly private. This repository serves as a technical case study of the platform's architecture, the automated Wills workflow, and the cloud deployment strategy.

## 📌 Executive Summary
This platform is designed as a modular, scalable **Legal Practice Management System**. While the initial Phase 1 deployment is focused specifically on automating the Will drafting and approval process, the underlying architecture is built to scale and support future legal functions (such as Trust Fund management). 

**The Business Problem:** The firm relied on a manual, paper-based workflow. Agents manually retyped client data into legal templates, causing high human error, slow turnaround times, and data security risks.
**The Solution:** A secure, automated digital workflow from Agent to Attorney, eliminating manual typing and providing a POPIA-compliant audit trail.

## 🔄 The Automated Workflow (Phase 1: Wills)
1. **Agent Initiation:** Agents log in and either send a secure, time-sensitive link to the client for self-service, or capture the client's data directly on the dashboard.
2. **Agent QA:** The submission returns to the Agent Dashboard for review, editing, and validation before submission.
3. **Attorney Review:** Attorneys see a clean list of pending Wills, where they can approve (triggering auto-generation of the document) or request changes.
4. **Client Action:** The client receives an email, downloads the final Will, signs it, and uploads the signed PDF back to the secure portal.
5. **Archiving:** The system permanently stores the signed document and logs a full audit trail (Date, Agent, Attorney).

## 🏗️ Cloud Infrastructure & Deployment
I designed the hosting architecture to be enterprise-grade, isolating the firm's data from shared hosting environments.
- **Dedicated VPS:** Deployed on a high-speed AMD EPYC server (4 vCPU, 8GB RAM, 200GB NVMe).
- **Operating System:** Ubuntu Linux (Enterprise-grade stability).
- **Security:** Off-site encrypted nightly backups for POPIA compliance.
- **Scalability:** The infrastructure is durable enough to host future modules (e.g., Trust Funds) and the firm's public-facing corporate website, saving them additional hosting costs.

## 🧠 System Architecture & Future-Proofing
- **Modular Design:** The database and backend logic were built with future expansion in mind. Adding new legal modules (like Trust Funds or Estate Administration) will be a seamless integration rather than a full rebuild.
- **Document Automation:** Bypassed heavy PDF rendering engines by utilizing `python-docx` to dynamically inject JSON data into predefined XML templates, reducing document generation time by ~80%.
- **Security First:** Implemented Role-Based Access Control (RBAC) and token-based, time-sensitive URLs for clients to upload signed documents without requiring a full account, balancing user experience with POPIA compliance.

## 💻 Tech Stack
- **Backend:** Python (Flask), SQLAlchemy ORM
- **Frontend:** HTML, CSS, JavaScript (Jinja2 templating)
- **Database:** SQLite (development) with a clear PostgreSQL migration path
- **Document Generation:** `python-docx`
- **Security:** Werkzeug password hashing, secure session management

## 👨‍💻 My Role (Developer & Cloud Specialist)
- **Full-Stack Development:** Designed and built the entire backend logic, database schema, and frontend UI.
- **Infrastructure Management:** Responsible for server uptime, firewall management, and automated off-site backups.
- **Business Analysis:** Authored the full technical proposal, pricing model, and hosting strategy for the client.

## 📸 System Interface (Anonymized)
*(Drag and drop 3 screenshots of the UI here. Make sure to use fake data like "John Doe")*
