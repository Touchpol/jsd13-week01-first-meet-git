prd_content = """# Product Requirement Document (PRD)

## 1. Document Control & Metadata
* **Product Name:** ProjectPulse AI (Intelligent Project Management & Automation Platform)
* **Document Version:** v1.0.0
* **Date:** July 1, 2026
* **Author:** Product Management Team
* **Status:** Draft / Under Review
* **Target Release:** Q3 2026

---

## 2. Executive Summary & Objective
ProjectPulse AI aims to solve the problem of fragmented workflows and administrative overhead in project management. Current tools act as passive data repositories, requiring manual status updates, task creation, and timeline adjustments. 

This platform introduces an active, AI-assisted layer that automatically synthesizes meeting notes, tracks real-time progress against milestones, predicts delivery bottlenecks, and drafts subtasks based on high-level goal descriptions. The core objective is to reduce time spent on project administration by 40% for engineering and product teams.

---

## 3. Problem Statement & User Personas

### 3.1 Problem Statement
Modern product and engineering teams waste excessive hours keeping project tracking software updated. Information is scattered across communication tools (Slack/Teams), documentation platforms (Notion/Confluence), and issue trackers (Jira/Linear). This siloed data leads to misaligned priorities, unexpected blockers, and delayed releases due to human oversights in project tracking.

### 3.2 User Personas
* **Persona A: The Product Manager (Sarah)**
    * *Needs:* Needs high-level roadmap tracking, automatic sync between team updates and timeline projections, and instant status summary generation for executive leadership.
    * *Pain Points:* Spends Fridays chasing developers for status updates and manually rewriting sprint progress into stakeholder reports.
* **Persona B: The Engineering Team Lead (Alex)**
    * *Needs:* Clean task breakdowns, minimal distraction from coding, automated ticket transition rules, and early warning signs for technical dependencies.
    * *Pain Points:* Hates manual logging, ticket updates, and constantly updating estimated completion dates.

---

## 4. Scope & Feature Requirements

The initial release (MVP) focuses on Core Task Management augmented by a centralized AI Assistant Engine.

### 4.1 Epics & Functional Requirements

| ID | Feature / Epic | Description | Priority |
| :--- | :--- | :--- | :--- |
| **FR-01** | Interactive Kanban Board | Drag-and-drop workflow status columns with custom field mapping and filtering capabilities. | P0 (Critical) |
| **FR-02** | AI-Powered Task Generation | Users can input a single paragraph description; the system automatically breaks it into a primary task with estimated story points and nested checkboxes. | P0 (Critical) |
| **FR-03** | Auto-Meeting Digest Sync | Upload or link audio/transcript files from Zoom/Meet; AI extracts action items and links or auto-generates tickets directly. | P1 (High) |
| **FR-04** | Predictive Bottleneck Alerts | Dashboard view showing dependencies that are at risk based on historic developer velocity and overlapping blockers. | P1 (High) |
| **FR-05** | Real-Time Multi-User Editing | Collaborative concurrent updates to descriptions, comments, and statuses without manual refreshes. | P0 (Critical) |

---

## 5. Non-Functional Requirements (NFRs)

### 5.1 Performance & Scalability
* **Latency:** Task status transitions and database commits must resolve within <200ms globally.
* **AI Engine Response:** AI text generation / task parsing must return a streaming or structured response within 3.5 seconds.
* **Concurrency:** Support up to 50,000 active concurrent WebSocket connections without performance degradation.

### 5.2 Security & Compliance
* **Authentication:** Multi-factor authentication (MFA) and Single Sign-On (SSO) integration via SAML 2.0 / OIDC.
* **Data Encryption:** TLS 1.3 for all data in transit, and AES-256 for data at rest.
* **Compliance:** Compliance alignment with SOC 2 Type II and GDPR framework standards.

---

## 6. User Experience (UX) & Flow
* **Navigation Hierarchy:** Left-collapsed persistent navigation panel (Dashboard, Projects, Boards, Settings).
* **Command Palette:** Global quick action menu invoked via `Ctrl + K` or `Cmd + K` allowing users to execute tasks, assign owners, or call the AI parser from anywhere in the interface.
* **Dark Mode Compatibility:** Universal toggle shifting system UI variables seamlessly between light theme and charcoal/slate theme arrays.

---

## 7. Key Performance Indicators (KPIs) & Success Metrics
* **Activation Rate:** % of new workspaces that generate at least 5 AI-assisted tasks within the first 7 days > 65%.
* **Retention Rate:** 30-day user retention benchmarking at 45% or higher for engineering organizations.
* **Efficiency Metric:** Average time saved per sprint cycle on manual status updates (targeted at >3 hours per user/month).

---

## 8. Open Questions & Future Considerations
1.  *AI Context Windows:* How should we handle historical task references when generating new sprints without hitting API context tokens limits?
2.  *Integration Strategy:* Should the initial launch include native Slack sync, or rely on a generic webhook mechanism? (Deferred to Phase 2 review).
"""

with open("prd.md", "w", encoding="utf-8") as f:
    f.write(prd_content)

print("File prd.md successfully generated.")