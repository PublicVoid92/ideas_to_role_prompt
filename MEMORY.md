# MEMORY.md — Shared Project Context

> **PURPOSE:** This file is the single source of truth for all roles.
> Every role must read this file before starting their work and update it when making architectural decisions.

---

## Project Summary

<!-- Filled in by the Product Manager after idea capture -->

_Replace this with a 2–3 sentence summary of the product, its target users, and its core purpose._

---

## Architecture Decisions

| Decision | Rationale | Date | Decided By |
|----------|-----------|------|-----------|
| Single-page application | Faster MVP delivery, no build step required | TBD | System Architect |
| RESTful API over GraphQL | Simpler implementation for MVP scope | TBD | System Architect |
| Vanilla JS (no framework) | Zero build tooling, runs directly in browser | TBD | System Architect |

---

## Tech Stack

| Layer | Technology | Notes |
|-------|-----------|-------|
| Frontend | HTML5, CSS3, Vanilla JS | No framework, no build step |
| Backend | PHP or Node.js | Choose based on hosting |
| Database | SQLite or flat JSON files | MVP only — migrate later if needed |
| AI (if applicable) | OpenAI API | Chat Completions endpoint |
| Hosting | VPS / free tier (Vercel, Railway) | Budget-conscious |

---

## Current Progress

- [ ] Idea defined
- [ ] Roles assigned
- [ ] Architecture designed
- [ ] Backend API implemented
- [ ] Frontend UI implemented
- [ ] AI integration (if applicable)
- [ ] QA tested
- [ ] Deployed

---

## Key Constraints

1. **MVP only** — no feature creep; build the simplest thing that works
2. **No heavy frameworks** — keep dependencies minimal
3. **All roles share this file** — update it when decisions change
4. **Changelog required** — every deliverable must have a CHANGELOG.md entry
5. **Vanilla JS preferred** — unless complexity clearly justifies a framework

---

## Open Questions / Blockers

| # | Question | Owner | Status |
|---|---------|-------|--------|
| 1 | _Add open questions here_ | — | Open |

---

## Notes

_Add any cross-cutting concerns, external dependencies, or important context here._
