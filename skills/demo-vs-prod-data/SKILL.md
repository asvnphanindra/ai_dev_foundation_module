---
name: demo-vs-prod-data
description: >-
  Isolate demo/try-it data from real user data with separate store paths and
  strict security rules. Use when adding Try demo, seed data, or anonymous
  access.
---

# Demo vs production data

## When to use

“Try demo”, anonymous sign-in, seed data, or any shared sample environment.

## Rules of thumb

1. **Separate path** for demo data (collection, schema, or tenant)—not mixed into personal user trees.  
2. **Identities map cleanly**: demo/anonymous → demo path only; signed-in owners → their own path only.  
3. **No open world writes**. Deny cross-reads between demo and prod.  
4. Demo UX should **read and write the real backend** on the demo path—not a silent localStorage “success” that never persists.  
5. Seed fictional data only; no personal PII in seeds or telemetry.

## Verify

- Rules/tests prove demo cannot read `users/{other}` (or equivalent).  
- Try demo creates/updates only under the demo path.  
- README does not claim offline seed when Firestore/DB is required.

## Do not

- Reuse production user documents for demo.  
- Broaden security rules “temporarily” for demos.  
- Leave UI copy that says data was not written when the product expects persistence.
