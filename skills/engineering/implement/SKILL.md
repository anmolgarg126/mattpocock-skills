---
name: implement
description: "Implement a piece of work based on a spec or set of tickets."
disable-model-invocation: true
---

Implement the work described by the user in the spec or tickets.

Use /tdd where possible, at pre-agreed seams.

Run typechecking regularly, single test files regularly, and the full test suite once at the end.

Once done, use /review-since to review the work.

Never commit without explicit approval. Show the user the diff summary and the commit message you propose, then wait for them to say yes. Only then commit to the current branch. The same goes for any push, tag or branch creation.
