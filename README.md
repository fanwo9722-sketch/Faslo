<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/platform-Windows%20%7C%20macOS-lightgrey?style=flat-square" />
  <img src="https://img.shields.io/badge/license-All%20Rights%20Reserved-green?style=flat-square" />
</p>

<h1 align="center">FASLO</h1>
<p align="center"><strong>I'm an AI-powered desktop coding agent for any codebase</strong></p>
<p align="center">Tell me what you want in plain English. I'll find the files, apply the fix, verify it, and push straight to GitHub — automatically.</p>

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

## What Am I?

I'm a desktop AI coding agent, and I work on your entire codebase — not just the frontend, not just the backend, all of it, in whatever language or framework you're actually using. Give me a task in plain English and I'll read your files, figure out exactly what needs to change, make the edit, verify it actually works, open or update a GitHub PR if that's what the job calls for, and tell you what I did. No terminal for you to touch, no manual setup beyond an API key. That's the whole point of me.

Flutter and FastAPI are the two stacks I cut my teeth on, but that's just where I started — I'm not limited to them.

I run as a native desktop app, so there's nothing to configure beyond entering an API key and pointing me at a project. Cloning, branching, committing, pushing, and opening PRs are all things I just handle myself — you never have to leave the app to do any of it.

---

## Where to Get Me

| Platform | File | Architecture | Size |
|---|---|---|---|
| 🪟 **Windows** | [FASLO.Setup.1.0.0.exe](https://github.com/fanwo9722-sketch/Faslo/releases/download/v1.0.0/FASLO.Setup.1.0.0.exe) | x64 | ~111 MB |
| 🍎 **macOS** | [FASLO-1.0.0-arm64.dmg](https://github.com/fanwo9722-sketch/Faslo/releases/download/v1.0.0/FASLO-1.0.0-arm64.dmg) | Apple Silicon (ARM64) | ~132 MB |
| 🐍 **macOS Agent** | [agent_server.app](https://github.com/fanwo9722-sketch/Faslo/actions/workflows/build-macos.yml) (CI artifact) | Apple Silicon | ~45 MB |

> **Note:** On macOS, you'll need both downloads running together — the desktop app alone won't have full functionality without its companion agent.

---

## How I Work

```text
   I'm told what to do, in plain English
                     |
                     v
        +-------------------------+
        |  I read your project    |
        |  — files, imports,      |
        |  and repo structure     |
        +-------------------------+
                     v
        +-------------------------+
        |  I generate a           |
        |  surgical patch — only  |
        |  the exact code that    |
        |  needs to change        |
        +-------------------------+
                     v
        +-------------------------+
        |  I apply the patch,     |
        |  auto-detect errors,    |
        |  and fix them before    |
        |  you ever see them      |
        +-------------------------+
                     v
        +-------------------------+
        |  I verify the result    |
        |  and report back live   |
        +-------------------------+
```

---

## What I Can Do

### 🧠 AI-Powered Code Understanding
I don't just skim your code — I read all of it. Every file, every class, every import, every dependency, before I touch a single line, so I actually understand how your project fits together before I try to change it. It doesn't matter what language or framework you're in, frontend or backend, I'll work through it. And I'm not locked to one model either — I can run on Claude, GPT-5.5, DeepSeek, or Mimo, whichever you've configured me to use.

### 🔧 Surgical Code Edits
When I make a change, I make exactly that change and nothing else. I work at the method, class, or file level, using a structured patch format so my edits are precise find-and-replace operations, not blind rewrites of things you didn't ask me to touch. For bigger changes, I can rewrite whole chunks — but I stay inside the lines you gave me.

### 🛡️ Automatic Error Recovery
After every edit, I run whatever linter, analyzer, or test suite fits your stack, and if something breaks, I catch it and fix it myself before I ever report back to you. If backend code changed, I'll go probe the actual endpoints to confirm the fix really works — not just that it compiles.

### 🐙 GitHub-Native Workflow
Point me at a repo URL and I'll clone it, branch off it, and get to work directly against your GitHub project. Give me an issue number and I'll go fix that specific issue, or turn me loose on your whole backlog. Once I've verified a fix, I commit it, push it, and open the pull request myself.

### 📡 Live Streaming UI
You can watch me work in real time — every file I read, every patch I apply, every check I run, streamed live as it happens. I run a multi-tab task runner, so I can take on several tasks at once. And I know when to ask and when to just tell you I'm done — if I need input, I'll ask; otherwise, I'll let you know the moment I've finished.

### 🔗 Task Chaining
The moment I finish one task, I'm ready for the next — queue it up instantly. I'll often suggest a natural follow-up based on what I just did, so we can build out entire features together, one conversational task at a time.

---

## Things You Can Ask Me

```text
"Fix issue #142 in this repo and open a PR"
"Clone this repo and resolve all failing tests"
"Add a like button to PostCard"
"Fix the login screen not redirecting after success"
"Add pagination to the feed endpoint"
"Create a new ProfileScreen with avatar and bio"
"Add error handling to the signup flow"
"Fix the 422 error on the register endpoint"
"Refactor the auth service to use proper token refresh"
"Add a search bar to the explore screen with debounced input"
"Review the open PRs and flag anything that looks broken"
```

---

## What I Need From You

| Requirement | Details |
|---|---|
| **A codebase** | Any local project folder, or a GitHub repo URL — any language or framework |
| **API key** | An API key for the model you want me to run on (entered once inside the app) |
| **GitHub access** *(optional)* | A personal access token, so I can clone private repos, push commits, and open PRs |

---

## Why I Exist

I got tired of watching the same loop play out: copy an error into a chat window, copy the fix back into the editor, run it, watch it break something else, repeat. So I close that loop myself. You describe the problem once, and I read, fix, verify, and report back — no round-tripping between you and a chat window required.

A few things I hold myself to along the way:

- 🎯 **I don't guess.** If I'm not confident about a change, I ask instead of shipping something half-right.
- 🔍 **I verify before I claim success.** "Fixed" means I checked — not that the patch compiled.
- 🧩 **I touch what you asked me to touch.** Nothing more.
- 🔄 **I keep momentum going.** One task well done should make the next one obvious.

---

## Models I Run On

| Model | Provider |
|---|---|
| Claude (Sonnet, Opus) | Anthropic |
| GPT-5.5 | OpenAI |
| DeepSeek | DeepSeek |
| Mimo | — |

---

## Status

🚀 I'm live at **v1.0.0**. Grab me from the downloads above.

---

## License

All Rights Reserved © FASLO
