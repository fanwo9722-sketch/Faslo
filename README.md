# FASLO 🔥

> **AI-powered coding agent for Flutter/Dart & Python/FastAPI projects — packaged as a desktop app.**

Named after the people who matter most — **F**rancisca, **A**jibola, **S**halom, **L**oveth, **O**luwadamilare.

---

## What is FASLO?

FASLO is a desktop application that acts as your AI coding agent. Open it, type a task in plain English, and watch it read your codebase, apply the fix, detect errors, and heal itself — all without you touching a single file.

No terminal. No config. No setup headaches. Just download, install, and start building.

---

## Download

| Platform | Download |
|---|---|
| 🪟 Windows | [Download for Windows (.exe)](https://github.com/fanwo9722-sketch/FasloEngine/actions/runs/26492638970/artifacts/7232596064) |
| 🍎 macOS | [Download for macOS (.dmg)](https://github.com/fanwo9722-sketch/FasloEngine/actions/runs/26492638970/artifacts/7232604458) |

---

## Features

- 🧠 **AI Agent** — powered by an LLM that thinks, searches, and patches your code iteratively
- 🔍 **Smart Code Search** — searches across your entire Flutter and FastAPI project instantly
- 🔧 **Surgical Patching** — replaces a single method, a full class, or creates new files without touching anything else
- 🩹 **Smart Find-Replace** — handles indentation, whitespace, and encoding mismatches automatically
- 🔄 **Self-Healing** — runs Dart analyzer and Python syntax checks after every patch and fixes errors automatically
- 📡 **Live API Probing** — calls your backend endpoints directly to verify responses before writing fixes
- 🌐 **Browser Verification** — opens a real browser to confirm your UI works after a fix
- 💬 **Live Streaming UI** — watch the agent think, search, and write code in real time
- 🗂️ **Full Project Awareness** — indexes every `.dart` and `.py` file in your project automatically
- ✅ **Works on Windows & macOS**

---

## How It Works

```
You type a task (e.g. "Add a like button to PostCard")
        ↓
FASLO scans and indexes your entire project
        ↓
The AI agent searches your code, finds the right files,
and applies the fix surgically
        ↓
Dart analyzer + Python checker run automatically
        ↓
Any errors are fed back to the agent and fixed (up to 3 rounds)
        ↓
✓ Done — clean, working code
```

---

## Example Tasks You Can Give FASLO

```
"Add a reply button to CommentCard"
"Fix the login screen not redirecting after success"
"Add pagination to the feed endpoint"
"Change the primary color to blue across all screens"
"Add error handling to the signup flow"
"Create a new ProfileScreen with avatar and bio"
"Add a loading spinner to the checkout button"
"Fix the 422 error on the register endpoint"
```

---

## Demo

![FASLO Demo](https://i.imgur.com/RfafchZ.gif)

---

## Built With

| Layer | Technology |
|---|---|
| Desktop App | Electron (Windows & macOS) |
| Frontend Projects | Flutter / Dart |
| Backend Projects | Python / FastAPI |
| AI Agent | OpenRouter LLM (tool-calling) |
| Code Indexing | Custom AST-based indexer |

---

## Requirements

- Your Flutter project (with a `lib/` folder)
- Your FastAPI backend (`main.py`)
- An OpenRouter API key (entered once inside the app)

That's it. FASLO handles everything else.

---

## License

MIT License — free to use, modify, and build on.

---

## Acknowledgements

Built with love and named after family. 🙏

*Francisca · Ajibola · Shalom · Loveth · Oluwadamilare*
