---
name: local-first-ship
description: >-
  Run and prove the app locally (or with emulators) before cloud deploy; keep
  tests and CI green; deploy when asked. Use for local setup, CI, and release
  timing.
---

# Local first, then ship

## When to use

Scaffolding, “how do I run this?”, CI setup, or deployment requests.

## Order of operations

1. **Local / emulator path** documented and runnable (prefer one command).  
2. **Unit + integration tests** — one command, passing.  
3. **CI** runs tests on PR or main.  
4. **Deploy** only when the human asks or a checklist explicitly requires a public URL.  
5. Keep `.env` and keys out of git; document required variables.

## Verify

- A new contributor (or agent) can follow README to a working local session.  
- CI is green on the commit you claim is done.  
- Deployed URL (if any) matches the commit you documented.

## Do not

- Treat cloud Hosting as a substitute for a broken local path.  
- Commit production secrets or placeholder credentials that look real.  
- Skip CI when the project already has a test workflow.
