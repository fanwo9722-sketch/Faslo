<![CDATA[<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/platform-Windows%20%7C%20macOS-lightgrey?style=flat-square" />
  <img src="https://img.shields.io/badge/license-All%20Rights%20Reserved-green?style=flat-square" />
</p>

<h1 align="center">FASLO</h1>
<p align="center"><strong>AI-powered desktop coding agent for Flutter & FastAPI</strong></p>
<p align="center">Describe what you want in plain English. FASLO finds the files, applies the fix, and verifies it — automatically.</p>

<p align="center">
  <a href="https://github.com/fanwo9722-sketch/Faslo/releases/download/v1.0.0/FASLO.Setup.1.0.0.exe">
    <img src="https://img.shields.io/badge/%E2%96%BA_Download-Windows.exe-blue?style=for-the-badge&logo=windows&logoColor=white" />
  </a>
  &nbsp;
  <a href="https://github.com/fanwo9722-sketch/Faslo/releases/download/v1.0.0/FASLO-1.0.0-arm64.dmg">
    <img src="https://img.shields.io/badge/%E2%96%BA_Download-macOS.dmg-black?style=for-the-badge&logo=apple&logoColor=white" />
  </a>
  &nbsp;
  <a href="https://github.com/fanwo9722-sketch/Faslo/actions/workflows/build-macos.yml">
    <img src="https://img.shields.io/badge/%E2%96%BA_Download-macOS_Agent_(.app)-orange?style=for-the-badge&logo=python&logoColor=white" />
  </a>
</p>

---

## What is FASLO?

FASLO is a desktop AI coding agent that understands your entire codebase — frontend **and** backend. You describe a task in plain English, and FASLO reads your files, identifies what to change, applies surgical edits, verifies the result, and reports back. **No terminal. No manual setup. Just results.**

It is built with a **multi-layer architecture** that combines:

| Layer | What it does |
|---|---|
| **Flutter Frontend** | Real-time task UI with live streaming, multi-tab task runner, and live terminal output |
| **Electron Desktop Shell** | Wraps the Flutter web app into a native desktop experience for Windows and macOS |
| **Python AI Agent** | The brain — reads your codebase, applies patches, runs checks, verifies endpoints, and chains tasks |
| **FastAPI Backend Server** | Handles agent logic, file I/O, patch application, and error recovery with full CRUD operations |
| **Firebase Integration** | User authentication, data persistence, and cloud sync |

---

## Downloads

| Platform | File | Architecture | Size |
|---|---|---|---|
| 🪟 **Windows** | [FASLO.Setup.1.0.0.exe](https://github.com/fanwo9722-sketch/Faslo/releases/download/v1.0.0/FASLO.Setup.1.0.0.exe) | x64 | ~111 MB |
| 🍎 **macOS** | [FASLO-1.0.0-arm64.dmg](https://github.com/fanwo9722-sketch/Faslo/releases/download/v1.0.0/FASLO-1.0.0-arm64.dmg) | Apple Silicon (ARM64) | ~132 MB |
| 🐍 **macOS Agent** | [agent_server.app](https://github.com/fanwo9722-sketch/Faslo/actions/workflows/build-macos.yml) (CI artifact) | Apple Silicon | ~45 MB |

> **Note:** The macOS Electron app (.dmg) requires the Python agent server (.app) to be running alongside it. Download both for full macOS support.

---

## How It Works

```
   You type a task in plain English
                    |
                    v
        +----------------------+
        |  FASLO reads your    |
        |  lib/ folder and     |
        |  understands your    |
        |  widget tree         |
        +----------+-----------+
                   v
        +----------------------+
        |  AI generates a      |
        |  surgical patch -    |
        |  only the exact code |
        |  that needs to change|
        +----------+-----------+
                   v
        +----------------------+
        |  Patch applied ->    |
        |  auto-detects errors |
        |  -> fixes them before|
        |  you ever see them   |
        +----------+-----------+
                   v
        +----------------------+
        |  Verifies endpoints  |
        |  (if backend code    |
        |  changed) and reports|
        |  results live        |
        +----------------------+
```

---

## Features

### 🧠 AI-Powered Code Understanding
- Reads your **entire** Flutter widget tree, Dart classes, and Python/FastAPI endpoints
- Understands file relationships, imports, and dependencies before making changes
- Supports **Claude**, **GPT-5.5**, **DeepSeek**, and **Mimo** models via OpenRouter

### 🔧 Surgical Code Edits
- Applies fixes at the **method**, **class**, or **file** level — never touches unrelated code
- Uses structured patch format with exact find/replace for reliable edits
- Supports chunk rewrites for larger changes

### 🛡️ Automatic Error Recovery
- Runs `dart analyze` and Python checks after every edit
- Catches and fixes errors automatically before reporting back
- Probes FastAPI endpoints to verify backend changes actually work

### 📡 Live Streaming UI
- Watch every step in real time — file reads, patches, checks, and results
- Multi-tab task runner — run several tasks in parallel
- Ask/Done prompts — the agent asks when it needs input, tells you when it's done

### 🔗 Task Chaining
- When a task finishes, queue the next one instantly
- Agent suggests follow-up tasks based on what it just did
- Build entire features through a conversation

---

## Example Tasks

```
"Add a like button to PostCard"
"Fix the login screen not redirecting after success"
"Add pagination to the feed endpoint"
"Create a new ProfileScreen with avatar and bio"
"Add error handling to the signup flow"
"Fix the 422 error on the register endpoint"
"Refactor the auth service to use proper token refresh"
"Add a search bar to the explore screen with debounced input"
```

---

## Requirements

| Requirement | Details |
|---|---|
| **Flutter project** | Must have a `lib/` folder with Dart source files |
| **Python backend** | FastAPI with `main.py` or equivalent entry point |
| **API key** | OpenRouter API key (entered once inside the app) |
| **Node.js 18+** | For the Electron desktop shell |

---

## Tech Stack

| Component | Technology |
|---|---|
| Desktop Shell | **Electron** (Windows + macOS native apps) |
| Frontend UI | **Flutter Web** (compiled, embedded in Electron) |
| AI Agent | **Python 3.11** (code reading, patching, verification) |
| Backend API | **FastAPI** (agent server, file operations, endpoint probing) |
| Authentication | **Firebase Auth** + Google OAuth |
| Database | **Cloud Firestore** |
| AI Models | **OpenRouter** (Claude, GPT-5.5, DeepSeek, Mimo) |
| Payments | **Paystack** integration |
| Build System | **GitHub Actions** (auto-build on push) |
| Packaging | **PyInstaller** (agent) · **electron-builder** (desktop app) |

---

## Architecture

```
+-------------------------------------------------+
|              Electron Desktop App                |
|  +-------------------------------------------+  |
|  |          Flutter Web App (UI)             |  |
|  |  - Task input     - Live streaming        |  |
|  |  - Multi-tabs     - Terminal output       |  |
|  +-------------------+-----------------------+  |
|                      | IPC / WebSockets          |
|  +-------------------v-----------------------+  |
|  |          Electron Main Process            |  |
|  |  - preload.js    - main.js                |  |
|  |  - Google OAuth   - Paystack payments     |  |
|  +-------------------+-----------------------+  |
+----------------------|--------------------------+
                       | HTTP / WebSocket
+----------------------v--------------------------+
|           Python Agent Server                    |
|  - Reads codebase with AST + glob scanning      |
|  - Applies patches (find/replace + chunks)      |
|  - Runs dart analyze, python checks             |
|  - Probes FastAPI endpoints for verification     |
|  - Chains follow-up tasks automatically          |
|  - Firebase integration for user data            |
+--------------------------------------------------+
```

---

## Supported Models

| Model | Provider |
|---|---|
| Claude (Sonnet, Opus) | Anthropic via OpenRouter |
| GPT-5.5 | OpenAI via OpenRouter |
| DeepSeek | DeepSeek via OpenRouter |
| Mimo | via OpenRouter |

---

## Status

🚀 **FASLO v1.0.0** is live. Downloads are available above.

---

## License

All Rights Reserved © FASLO]]>