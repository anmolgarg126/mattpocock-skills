# Domain Docs

How the engineering skills should consume this repo's domain documentation when exploring the codebase.

## Before exploring, read these

Domain docs live in `~/Developer/codebase/code-knowledge/<repo>/`, where `<repo>` is the repository folder name, never in the source repo itself.

- **`CONTEXT.md`** in that folder, or
- **`CONTEXT-MAP.md`** if it exists: it points at one `CONTEXT.md` per context. Read each one relevant to the topic.
- **`adr/`**: read ADRs that touch the area you're about to work in. In multi-context repos, also check `contexts/<context>/adr/` for context-scoped decisions.

If any of these files don't exist, **proceed silently**. Don't flag their absence; don't suggest creating them upfront. The `/domain-modeling` skill (reached via `/grill-with-docs` and `/improve-codebase-architecture`) creates them lazily when terms or decisions actually get resolved.

## File structure

Single-context repo (most repos):

```
~/Developer/codebase/code-knowledge/<repo>/
├── CONTEXT.md
└── adr/
    ├── 0001-event-sourced-orders.md
    └── 0002-postgres-for-write-model.md
```

Multi-context repo (presence of `CONTEXT-MAP.md`):

```
~/Developer/codebase/code-knowledge/<repo>/
├── CONTEXT-MAP.md
├── adr/                              ← system-wide decisions
└── contexts/
    ├── ordering/
    │   ├── CONTEXT.md
    │   └── adr/                      ← context-specific decisions
    └── billing/
        ├── CONTEXT.md
        └── adr/
```

## Use the glossary's vocabulary

When your output names a domain concept (in an issue title, a refactor proposal, a hypothesis, a test name), use the term as defined in `CONTEXT.md`. Don't drift to synonyms the glossary explicitly avoids.

If the concept you need isn't in the glossary yet, that's a signal: either you're inventing language the project doesn't use (reconsider) or there's a real gap (note it for `/domain-modeling`).

## Flag ADR conflicts

If your output contradicts an existing ADR, surface it explicitly rather than silently overriding:

> _Contradicts ADR-0007 (event-sourced orders), but worth reopening because…_
