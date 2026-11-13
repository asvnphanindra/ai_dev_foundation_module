---
name: cert-or-checklist-ship
description: >-
  Ship against a rubric or certificate checklist: map criteria to artifacts,
  close pass-bar gaps first, keep a submit checklist. Use for courses, audits,
  or launch checklists.
---

# Checklist / rubric shipping

## When to use

Course projects, certification rubrics, or any scored launch checklist.

## Steps

1. **Inventory criteria** in a short table (criterion → max points / bar → artifact).  
2. **Map gaps** honestly (e.g. missing public URL, missing CD, missing tests).  
3. **Order work** by pass threshold first, then full marks.  
4. **Prove each bar** with a concrete artifact: README section, test command, CI run, live URL, Docker one-liner, obs UI, alert, on-call path.  
5. **Submit checklist**: repo URL, commit id, certificate/name fields, peer reviews if required, live URL if claimed.

## Typical full-stack bars (adapt to your rubric)

- Spec + public tracker with AC  
- Agent/process docs (`AGENTS.md`)  
- FE + BE + DB, one-command local  
- Unit + integration tests  
- Docker Compose one command  
- Deployed URL or deploy demo  
- CI tests + CD (manual prod gate OK if documented)  
- Observability + user-impact alert + on-call remediation  

## Do not

- Confuse “pass mark” with “expected score.”  
- Claim deploy points without a URL or recorded demo.  
- Skip mandatory peer reviews when the cert requires them.
