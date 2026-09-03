# HardPac

> Design studio & playground for the successor to **SoftPac** — a logistics software giant.

We do **not** have the SoftPac codebase. This repo is where we (re)discover what SoftPac does, model what the client actually needs, and explore rewrite options — architecture, stack, and scope — before committing to any implementation.

Development here is **fully agentic** and **client-collaborative**: requirements and domain knowledge are captured as structured notes in `docs/`, decisions are recorded as ADRs, and every exploration is reproducible.

## Status

| Phase | State |
|---|---|
| Discovery (what does SoftPac do, for whom, how) | 🔵 **Current** |
| Requirements & domain modeling | ⚪ not started |
| Architecture / stack options | ⚪ not started |
| Prototype / vertical slice | ⚪ not started |

## Repository structure

```
HardPac/
├── README.md            # this file — mission & status
├── docs/
│   ├── README.md        # documentation index
│   ├── softpac-discovery.md   # intel log: everything we learn about SoftPac
│   └── decisions/       # Architecture Decision Records (ADRs)
└── (future: prototypes/, specs/)
```

## Working agreement

- **Discovery first, code later.** Every stack/architecture decision must be
  traceable to a documented requirement or constraint.
- **One ADR per significant decision** (`docs/decisions/NNNN-title.md`).
- Anything learned from the client lands in `docs/softpac-discovery.md` with
  a source and date.
- Prototypes live in isolated subfolders so failed experiments don't pollute
  the main line.
