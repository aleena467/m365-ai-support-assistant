# m365-ai-support-assistant
Microsoft 365 AI support dashboard with React, FastAPI, MSAL, Graph, OpenAI, and demo mode

# Microsoft 365 AI Support Assistant

A full-stack simulation of an internal Microsoft 365 IT support workspace built for identity management, collaboration services, and AI-powered troubleshooting.

## Overview

This project simulates an enterprise IT dashboard similar to what organizations like AIMCo would use for:

* Microsoft 365 user support
* Identity and group management
* Teams/SharePoint troubleshooting
* AI-powered IT assistance (Copilot-style support)

It includes a **mock Microsoft Graph layer** and a **FastAPI backend**, with a modern React dashboard frontend.

---

## Features

### 👤 Identity & Profile (Microsoft Graph Simulation)

* `/api/me` returns user profile (name, email, job title, location)
* Simulates Microsoft Graph `/me` endpoint

### 👥 Group Management

* `/api/groups` returns M365-style groups
* Simulates `/me/memberOf`
* Demonstrates role-based access concepts

### AI Support Assistant

* `/api/chat` provides AI-powered troubleshooting
* Supports Teams, SharePoint, OneDrive scenarios
* Can run in mock or OpenAI-powered mode

### Dashboard UI

* Clean IT workspace interface
* Profile + groups + AI assistant in one view
* Demo mode toggle for interview explanation

---

## Architecture

Frontend → React (Vite)
Backend → FastAPI
AI → OpenAI API (optional)
Identity → Mock Microsoft Graph (upgradeable to Entra ID)

---

## 🔁 Demo Mode

This project uses mock data to simulate Microsoft Graph because no test tenant was required.

To switch to real Microsoft identity:

* Set `VITE_USE_MOCK_AUTH=false`
* Add Azure App Registration credentials
* Enable MSAL authentication

---

## 🧠 Why this project matters

This project is designed specifically to match real-world responsibilities of:

* Microsoft 365 support roles
* Cloud workplace analysts
* IT automation and governance teams

It demonstrates:

* API integration
* Identity concepts (Entra ID)
* Enterprise SaaS understanding
* AI-assisted IT support workflows

---

## Tech Stack

* React (Vite)
* FastAPI
* Python
* OpenAI API
* Microsoft Graph (simulated)
* REST APIs

---

## Screenshots

<img width="1415" height="779" alt="Screenshot 2026-06-16 at 9 20 17 PM" src="https://github.com/user-attachments/assets/4a8fd8de-d00a-49aa-80c8-999d78915e3e" />


---

## How to run locally

### Backend

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

---

## Future improvements

* Replace mock Graph with real Microsoft Entra ID
* Add SharePoint integration
* Add Power Automate workflows
* Add Copilot Studio agent
