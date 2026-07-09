# 💡 Ideas → Role Prompt Generator

Transform a single idea into a complete, structured software development system — with role-based prompts, a shared memory file, and a changelog with role accountability.

---

## What it does

Given any software idea you describe in plain text, the tool automatically generates:

| Output | Description |
|--------|-------------|
| **Idea Summary** | Explanation, target users, core features, technical scope |
| **Roles** | Relevant development roles with responsibilities and dependencies |
| **Role Prompts** | Structured, copy-ready prompts for each role |
| **MEMORY.md** | Shared context file used as single source of truth |
| **CHANGELOG.md** | Versioned log of changes with role ownership |
| **JSON export** | Full structured output for reuse in other tools or pipelines |

---

## Quick start

1. Open `index.html` directly in any modern browser — **no build step, no dependencies**.
2. Type (or paste) your idea into the text area.
3. Click **⚡ Generate System**.
4. Explore the generated sections, copy individual role prompts, or click **⬇ Download JSON** for the full export.

> **Tip:** Press `Ctrl+Enter` (Windows/Linux) or `Cmd+Enter` (Mac) to generate directly from the text area.

---

## Files

```
ideas_to_role_prompt/
├── index.html      # Complete single-file web application
├── MEMORY.md       # Template for the shared project context file
├── CHANGELOG.md    # Template/example changelog with role ownership
└── README.md       # This file
```

---

## Roles supported

The tool automatically selects relevant roles based on your idea's keywords:

| Role | Triggered by |
|------|-------------|
| Product Manager | Always included |
| System Architect | Always included |
| Backend Developer | API, server, database, auth, storage keywords |
| Frontend Developer | UI, web, app, dashboard, platform keywords |
| UI/UX Designer | Design, mobile, wireframe, layout keywords |
| QA Engineer | Test, quality, bug, validation keywords |
| DevOps Engineer | Deploy, hosting, Docker, CI/CD keywords |
| AI Engineer | AI, ML, LLM, GPT, recommend, predict keywords |

---

## JSON output structure

```json
{
  "idea_summary": {
    "title": "...",
    "explanation": "...",
    "targetUsers": "...",
    "coreFeatures": ["..."],
    "techScope": ["..."]
  },
  "roles": [
    {
      "name": "...",
      "icon": "...",
      "responsibility": "...",
      "scope": "...",
      "dependencies": ["..."]
    }
  ],
  "prompts": [
    {
      "role": "...",
      "prompt": "..."
    }
  ],
  "memory": {
    "projectSummary": "...",
    "architectureDecisions": ["..."],
    "techStack": ["..."],
    "currentProgress": ["..."],
    "keyConstraints": ["..."],
    "roleList": ["..."]
  },
  "changelog": [
    {
      "version": "0.1",
      "date": "YYYY-MM-DD",
      "entries": [
        {
          "change": "...",
          "role": "...",
          "reason": "..."
        }
      ]
    }
  ]
}
```

---

## Default tech stack

- **Frontend:** HTML5, CSS3, Vanilla JS (no framework, no build step)
- **Backend:** PHP or Node.js
- **Database:** SQLite or flat JSON files (MVP)
- **AI (optional):** OpenAI Chat Completions API

---

## System rules

- Keep everything **MVP-focused** — no over-engineering
- All roles share **MEMORY.md** as their single source of truth
- Every deliverable must produce a **CHANGELOG.md** entry with role accountability
- Prompts are **reusable** — copy them directly into any LLM chat
