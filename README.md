# ai_dev_foundation_module

Reusable **process** foundations for building apps with AI coding agents (Cursor). Stack-agnostic: no app templates—skills and a short playbook only.

## Add as a submodule

```bash
git submodule add https://github.com/asvnphanindra/ai_dev_foundation_module.git ai_dev_foundation_module
git submodule update --init --recursive
```

In the consuming app’s `AGENTS.md`, point agents at:

- `ai_dev_foundation_module/docs/ai-programming-approach.md`
- `ai_dev_foundation_module/skills/*/SKILL.md`

## Layout

| Path | Role |
|------|------|
| `docs/ai-programming-approach.md` | Narrative playbook |
| `AGENTS.md` | Skill index for agents |
| `skills/*/SKILL.md` | Cursor skills (read when relevant) |

## Skills (v1)

1. **groom-ac-implement** — groom → acceptance criteria → implement → verify  
2. **agent-collaboration** — clarifying questions, short kickoffs, commit cadence  
3. **local-first-ship** — local/emulators → tests/CI → deploy when asked  
4. **demo-vs-prod-data** — isolated demo data + security boundaries  
5. **cert-or-checklist-ship** — rubric/checklist driven delivery  

Update this module in one place; pull submodule updates into each project.
