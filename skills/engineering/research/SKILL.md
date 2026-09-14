---
name: research
description: Investigate a question against high-trust primary sources and capture the findings as a Markdown file under ~/Developer/codebase/brainstorming. Use when the user wants a topic researched, docs or API facts gathered, or reading legwork delegated to a background agent.
---

Spin up a **background agent** to do the research, so you keep working while it reads.

Its job:

1. Investigate the question against **primary sources** (official docs, source code, specs, first-party APIs), not a secondary write-up of them. Follow every claim back to the source that owns it.
2. Write the findings to a single Markdown file, citing each claim's source.
3. Save it to `~/Developer/codebase/brainstorming/<feature>/research/<question-slug>.md` (the feature folder this question belongs to; for research not tied to a feature, use `~/Developer/codebase/brainstorming/<topic-slug>/research.md`), never in the source repo. Report the path.
