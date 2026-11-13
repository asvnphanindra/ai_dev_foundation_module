---
name: agent-collaboration
description: >-
  How humans and coding agents should collaborate: one clarifying question at a
  time, short kickoffs, regular commits, one focused change set. Use when
  coordinating agents or writing kickoff prompts.
---

# Agent collaboration

## When to use

Planning work for agents, writing kickoffs, or resolving ambiguity with the human.

## Practices

1. **One clarifying question at a time**  
   If blocked, ask a single short question; number it when a short series is needed (e.g. Q1/3).

2. **Short kickoffs**  
   Instructions + paths to docs/code. Do not paste large file contents when a path will do.

3. **Commit and push regularly**  
   Land working slices on the remote often so review and recovery stay cheap.

4. **One focused worker per change set**  
   Avoid parallel agents editing the same files unless the human explicitly wants fan-out.

5. **Document the team**  
   `AGENTS.md` (or equivalent) names roles and handoffs; link modular process docs.

## Do not

- Ask multi-part clarification dumps in one message when one answer unblocks.  
- Leave secrets in chat, commits, or logs.  
- Start cloud deploy or destructive ops without explicit human ask.
