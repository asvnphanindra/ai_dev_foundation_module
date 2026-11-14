---
name: local-first-ship
description: >-
  Run and prove the app locally (or with emulators) before cloud deploy; keep
  tests and CI green; deploy to test then prod when asked. Use for local setup,
  CI, and release timing (test → prod).
---

# Local first, then ship

## When to use

Scaffolding, “how do I run this?”, CI setup, or deployment requests.

## Order of operations

1. **Local / emulator path** documented and runnable (prefer one command).  
2. **Unit + integration tests** — one command, passing.  
3. **CI** runs tests on PR or main.  
4. **Test / staging deploy** — separate project/env/config + secrets from prod; document the test URL and commit.  
5. **Verify on test** — smoke or checklist against the deployed test URL.  
6. **Prod deploy** only when the human asks or a rubric requires prod; use the same verified commit/artifact when possible.  
7. Keep `.env` and keys out of git; document required variables. Never use prod credentials or data stores for test deploys.

## Verify

- A new contributor (or agent) can follow README to a working local session.  
- CI is green on the commit you claim is done.  
- Name both test and prod URLs when they exist, and which commit each tracks.

## Do not

- Treat cloud Hosting as a substitute for a broken local path.  
- Commit production secrets or placeholder credentials that look real.  
- Skip CI when the project already has a test workflow.  
- Promote untested commits to prod.  
- Share env files across test and prod.  
- Treat the test URL as done when the ask was prod.
