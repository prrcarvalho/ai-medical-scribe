# Domain docs

This repository uses a single-context domain-document layout.

## Before exploring

- Read `CONTEXT.md` at the repository root when it exists.
- Read relevant decisions under `docs/adr/` when that directory exists.
- If either is absent, proceed silently. Create them lazily through domain-modeling when terminology or an architectural decision is actually resolved.

## Layout

```text
/
├── CONTEXT.md
├── docs/
│   └── adr/
└── src/
```

## `CONTEXT.md`

Use `CONTEXT.md` only as the project's domain glossary:

- Use its canonical terms in issues, specifications, tests, and code.
- Challenge ambiguous or conflicting terminology.
- Do not store implementation details or general planning notes in it.

## Architectural decision records

Create an ADR only when a decision is hard to reverse, surprising without context, and the result of a genuine trade-off. Surface conflicts with existing ADRs rather than silently overriding them.
