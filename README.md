# SmartFlow AI: Smart Automation & Resource Intelligence Platform

[![Node.js Version](https://img.shields.io/badge/node-%3E%3D20.0.0-brightgreen.svg)](https://nodejs.org/)
[![React Version](https://img.shields.io/badge/react-18.3.1-blue.svg)](https://react.dev/)
[![Vite Version](https://img.shields.io/badge/vite-6.0.7-purple.svg)](https://vitejs.dev/)
[![License](https://img.shields.io/badge/license-MIT-cyan.svg)](LICENSE)

**SmartFlow AI** is a next-generation, AI-driven automation and resource intelligence platform engineered specifically for students, researchers, academic labs, and institutions. It bridges high-throughput workflow automation, real-time resource telemetry (time, energy, study hours, GPU compute, cloud storage), predictive machine learning heuristics, and multi-source data exploration into a single executive dashboard.

---

## 1. Problem Statement

> **Student Innovation – Smart Automation:**  
> Student innovation focuses on the intelligent use of resources for transforming and advancing technology by combining Artificial Intelligence to explore various sources, automate repetitive activities, analyze information, and generate valuable insights.

Traditional task managers and static dashboards lack adaptive intelligence—they require constant manual updating, do not detect workload or resource bottlenecks, fail to predict delivery risks, and cannot execute automated rules based on live telemetry.

---

## 2. Project Objective

Build a working full-stack software application that:
1. **Automates Repetitive Activities**: Visual WHEN-IF-THEN rule engine and recurring task auto-renewal.
2. **Optimizes Resource Allocation**: Monitors energy, compute clusters, study hours, and digital bandwidth, computing wasted capacity and providing 1-click optimization.
3. **Synthesizes Multi-Source Intelligence**: Parses CSV/JSON datasets, computes statistical anomalies/outliers, and visualizes distributions without paid third-party APIs.
4. **Predicts Hazards & Simulates Decisions**: Features an **AI Priority Predictor** and interactive **What-If Scenario Simulator** to evaluate milestone delays before committing changes.
5. **Provides Zero-Friction Setup**: Seamlessly operates in dual-mode (MongoDB database with automatic fallback to high-fidelity in-memory persistence).

---

## 3. Uses and Benefits

### Core Uses
* **Automate Repetitive Tasks**: Deploy reactive event triggers on approaching deadlines, file uploads, and resource spikes.
* **Intelligent Resource Management**: Real-time tracking of focused study hours, GPU clusters, lab hardware, and network usage.
* **Data Exploration**: Ingest CSV/JSON datasets, auto-detect columns, identify statistical outliers, and chart trends.
* **Predictive Sequencing**: Automatically sort tasks by AI priority trajectory rather than static due dates.
* **Decision Stress-Testing**: Simulate "what happens if a project slips by 3 days" to project risk scores and conflicts.

### Key Benefits
* **Saves 5–8 Hours Weekly**: Eliminates manual logging and repetitive status updates.
* **Prevents Milestone Burnout**: Warns users before project timelines breach cognitive or hardware limits.
* **Zero Configuration**: Ready to demo immediately with pre-loaded realistic data.

---

## 4. Key Features & Modules

```
----------------------------------------------------------------------
| SmartFlow AI |  Search Tasks & Resources  | Notifications | Profile |
----------------------------------------------------------------------
| Sidebar      | Dashboard (KPIs, Trends, AI Daily Plan, Insights)    |
|              | Resources (Capacity, Wasted Units, 1-Click Optimize) |
|              | Automation (WHEN-IF-THEN Visual Engine, Test Runs)   |
|              | AI Insights (Recommendation Center, Anomaly Sweeps)  |
|              | Tasks (Predictive Priority Scoring, Templates)       |
|              | Analytics & Reports (Export CSV, Printable PDF)      |
|              | Activity Timeline (Chronological Audit Logs)          |
|              | AI Assistant (Natural-Language Command Action Hub)   |
|              | Data Explorer (Multi-source CSV/JSON Analytics)      |
|              | What-If Simulator (Interactive Stress-Testing)       |
|              | Settings (Profile, Dark/Light Themes, AI Sensitivity)|
----------------------------------------------------------------------
```

### Module Breakdown:
1. **Dashboard**: Live KPIs (Resource Efficiency %, Automation Score, Productivity Score, Overdue Tasks), Productivity Trend Area Chart, Priority Donut Chart, Resource Utilization Bars, and AI Daily Plan schedule.
2. **Resources Hub**: Tracks Time, Energy, Study Hours, Projects, Equipment, Digital Resources, and Network Usage. Features a 1-click **Optimize** action that reclaims wasted overhead.
3. **Automation Workflow Engine**: Visual builder for `[WHEN Event] → [IF Condition] → [THEN Actions]`. Includes a live **Test Workflow** trigger with millisecond execution profiling.
4. **AI Insights & Recommendation Center**: Actionable recommendations (e.g. *Expedite Overdue Research Paper*, *Batch GPU Training Overnight*, *Combine Code Reviews*) with direct 1-click execution.
5. **Smart Tasks**: Automated priority calculation (0–100) using deadline proximity, duration load, and text sentiment. Features pre-built templates (*Academic Research*, *Hardware Prototype*, *Hackathon Sprint*).
6. **Multi-Source Data Explorer**: Ingests files or pre-loaded datasets (`academic_workload.csv`, `energy_consumption.json`), calculating mean, min, max, std-dev, outlier detection, and interactive line charts.
7. **What-If Simulator**: Interactive sliders for milestone shifts, capacity changes, and unplanned workload spikes, outputting live risk levels and conflict warnings.
8. **Reports & Analytics**: Full intelligence briefs with 1-click **Export to CSV** and **Printable PDF**.
9. **Activity Timeline**: Complete chronological audit trail of all automated events, task completions, and resource adjustments.
10. **Smart Alert Center**: Categorized notifications with in-app toasts and browser push notification support.
11. **Settings**: Profile identity, Dark/Light mode switcher, database storage mode display, and heuristic sensitivity sliders.

---

## 5. Technology Stack

| Layer | Technologies Used | Purpose |
| :--- | :--- | :--- |
| **Frontend** | React 18, Vite 6, React Router 6 | High-speed SPA rendering with component modularity |
| **Icons & UI** | Lucide React, Glassmorphism Tokens | Futuristic, responsive cyberpunk-dark and executive-light design |
| **Charts** | Recharts, Canvas-Confetti | Responsive area charts, bar graphs, and completion animations |
| **Backend** | Node.js, Express.js | High-throughput REST API with middleware architecture |
| **AI Layer** | SmartFlow Heuristic & NLP Service | Natural-language intent parser, priority scorer, and scenario simulator |
| **Persistence** | Mongoose (MongoDB) + StorageAdapter | Transparent dual-mode: connects to Mongo or falls back to in-memory store |
| **Data Engine** | PapaParse, Multer | Streaming CSV/JSON parsing and statistical computation |

---

## 6. System Architecture

```mermaid
graph TD
    Client[React + Vite Frontend (Port 5173)] -->|JWT REST API| ExpressServer[Node.js Express Server (Port 5000)]
    ExpressServer --> AIService[AI Engine: NLP & Priority Scorer]
    ExpressServer --> WorkflowEngine[Automation Workflow Engine]
    ExpressServer --> Storage[Dual Storage Adapter: MongoDB or In-Memory]
    ExpressServer --> DataAnalyzer[Data Analysis & Outlier Engine]
    Client --> Simulator[What-If Scenario Simulator]
    Client --> ExportEngine[CSV / PDF Report Generator]
```

---

## 7. Installation & Quickstart

### Prerequisites
* **Node.js**: v18+ or v20+ installed
* **npm**: v9+ installed
* *(Optional)* MongoDB running locally or via MongoDB Atlas (Application operates out-of-the-box in Demo Mode if MongoDB is not present).

### Step 1: Clone or Navigate to Directory
```bash
cd c:\Users\juver\OneDrive\Desktop\Hackathon
```

### Step 2: Install Dependencies
```bash
# Install root dependencies
npm install

# Install server dependencies
cd server
npm install

# Install client dependencies
cd ../client
npm install
cd ..
```

### Step 3: Run the Application (Concurrent Mode)
Launch both the backend API and frontend dev server with a single command:
```bash
npm run dev
```

The system will start:
* **Backend API**: `http://localhost:5000` (Health Check: `http://localhost:5000/api/health`)
* **Frontend Web App**: `http://localhost:5173`

---

## 8. Demo Credentials & 1-Click Access

When opening `http://localhost:5173`, click the **"Quick Demo Login (1-Click)"** button to bypass authentication and instantly load the fully populated workspace.

Alternatively, use standard demo credentials:
* **Email**: `demo@smartautomation.ai`
* **Password**: `demo123`

---

## 9. Environment Variables (`.env`)

A default `.env` file is included in the project root:

```ini
# Server Configuration
PORT=5000
NODE_ENV=development

# Database Configuration (Optional - in-memory fallback is active if MongoDB is not reachable)
MONGODB_URI=mongodb://localhost:27017/smart_automation_db
DEMO_MODE=true

# JWT Secret for Authentication
JWT_SECRET=super_secret_ai_automation_jwt_key_2026

# Optional External AI API (Google Gemini / OpenAI)
EXTERNAL_AI_API_KEY=
EXTERNAL_AI_PROVIDER=none
```

---

## 10. API Documentation (Key Endpoints)

| Endpoint | Method | Description |
| :--- | :--- | :--- |
| `/api/health` | `GET` | Platform status, timestamp, and active database mode |
| `/api/auth/demo-login` | `POST` | Generates 1-click JWT demo token |
| `/api/tasks` | `GET`, `POST` | List filtered tasks or create task with AI priority score |
| `/api/tasks/ai-suggest-order`| `POST` | Reorders tasks based on optimal AI trajectory |
| `/api/resources` | `GET`, `POST` | Fetch all resource streams or register a new monitor |
| `/api/resources/:id/optimize`| `POST` | Trims wasted units and load-balances capacity |
| `/api/automations` | `GET`, `POST` | View or create visual WHEN-IF-THEN automation rules |
| `/api/automations/:id/test` | `POST` | Simulates execution of a workflow rule in real-time |
| `/api/ai/assistant` | `POST` | Processes natural language prompt into executable actions |
| `/api/ai/insights` | `GET` | Computes system scores, trends, and recommendations |
| `/api/ai/what-if` | `POST` | Calculates conflicts and risk scores for hypothetical delays |
| `/api/data/upload` | `POST` | Ingests and analyzes CSV/JSON files |
| `/api/data/sample/:name` | `GET` | Loads sample academic or energy datasets |
| `/api/reports/summary` | `GET` | Aggregated metrics for PDF and executive briefs |
| `/api/reports/export-csv` | `GET` | Downloads task and resource telemetry in CSV format |

---

## 11. Verification & Testing

1. **Backend Route Verification**:
   ```powershell
   Invoke-RestMethod -Uri http://localhost:5000/api/health
   ```
2. **Frontend Build Verification**:
   ```powershell
   cd client
   npm run build
   ```
3. **Workflow Rule Test**:
   ```powershell
   Invoke-RestMethod -Uri http://localhost:5000/api/automations/wf-01/test -Method Post
   ```

---

## 12. Future Enhancements

* **IoT Sensor Integration**: MQTT bridges to connect hardware lab sensors (temperature, wattage, ambient noise).
* **Voice-Activated Commands**: Web Speech API integration for hands-free workflow triggers.
* **Multi-User Collaborative Workspaces**: Real-time WebSockets synchronization between project team members.
* **Autonomous LLM Agents**: LangChain/AutoGen style self-correcting agents that resolve task bottlenecks autonomously.

---

## 13. License

Distributed under the MIT License. Built for the Student Innovation Hackathon Demonstration.
