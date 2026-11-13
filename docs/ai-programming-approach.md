# Programming approach with AI tools

A practical loop for building an application with coding agents. Process-first; stack-agnostic.

## 1. Frame the product before code

- Write a short problem statement: who, pain, expected behavior.
- Keep a living product spec and a **public** task tracker (issues) with acceptance criteria.
- Prefer one end-to-end app over disconnected demos.

## 2. Groom → AC → implement → verify

For each slice of work:

1. **Groom** the ask into a small, testable outcome.  
2. Write **acceptance criteria** (observable pass/fail).  
3. **Implement** only that slice.  
4. **Verify** (tests, manual path, or both) before the next slice.  

Do not skip AC when agents implement: criteria are the contract.

## 3. Collaborate with agents deliberately

- Ask **one clarifying question at a time** when blocked; keep questions short.  
- Prefer **short kickoffs** and links to docs over dumping large context.  
- **Commit and push regularly** so progress is recoverable and reviewable.  
- Prefer **one focused worker** on a change set to avoid conflicting edits.  
- Document agent roles and how they hand off (`AGENTS.md` + modular docs).

## 4. Local first, ship when asked

1. One-command (or clearly documented) **local** run—emulators or local services before cloud.  
2. **Unit + integration** tests runnable in one command; keep them green.  
3. **CI** on pull requests (or main) for tests.  
4. **Deploy** (Hosting, containers, etc.) when the human asks or the checklist requires it—not as a substitute for a working local path.  
5. Never commit secrets (`.env`, keys); document required env vars instead.

## 5. Demo vs production data

- Demo/try-it paths must not leak into personal production data.  
- Prefer a **separate store path** (collection/schema/tenant) for demo.  
- Security rules: demo identities only access demo data; real users only their own.  
- Avoid “offline fake success” that hides that the backend was never written.

## 6. Checklist / rubric shipping

When a course, cert, or launch rubric exists:

- Map each criterion to a concrete artifact (README section, test command, URL, CI badge).  
- Close gaps in priority order (pass bar first, then full marks).  
- Keep a submit checklist: repo URL, commit id, live URL, peer reviews if required.

## 7. Observability and ops (when in scope)

- Shared **trace id** across logs, metrics, and traces; viewable in a UI.  
- At least one **user-impact** alert.  
- An on-call path (human or agent) that can remediate from the alert.

## 8. Context management

- Root `AGENTS.md` indexes process docs and skills.  
- Modular docs for architecture, product, and process—agents read what the task needs.  
- This module is meant to be a **git submodule** so every new project starts from the same foundations.
