---
name: groom-ac-implement
description: >-
  Groom a feature or issue into acceptance criteria, implement only that slice,
  then verify. Use when starting a GitHub issue, user story, or unclear feature
  request with AI agents.
---

# Groom → AC → implement → verify

## When to use

New feature, bug with unclear scope, or any issue an agent will implement.

## Steps

1. **Groom**  
   Restate the outcome in one sentence. Cut out-of-scope work. Name the user-visible change.

2. **Acceptance criteria**  
   List 2–6 observable checks (Given/When/Then or bullet pass/fail). No AC → do not implement yet.

3. **Implement**  
   Smallest change that meets AC. Prefer existing patterns in the repo. Commit with a message that references the issue/outcome.

4. **Verify**  
   Run the project’s test command and any manual path named in AC. Fix failures before the next slice.

## Do not

- Implement while “figuring out” requirements in the same pass without writing AC.  
- Bundle unrelated refactors with the slice.  
- Mark done without verification evidence.
