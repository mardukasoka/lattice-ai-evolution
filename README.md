# lattice-ai-evolution

Experimental AI evolution laboratory for bounded recursive improvement, agent orchestration, validation, provenance and Lattice-informed trajectory research.

## Architecture

This repository implements the Abacus-audited core rather than introducing a second orchestration architecture:

**Council → Sagent Supervisor → bounded TaskTicket → sandboxed Fractal → artifacts → deterministic validation → Trackinizer.**

RRSI-style regularization surrounds recursive-improvement experiments. PufferLib is restricted to genuine RL environments. SOM is an analytical/relevance layer. The Lattice supplies an ethical/trajectory framework without executive authority.

See [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md).

## First acceptance milestone

Sagent issues a bounded TaskTicket; Fractal runs in an isolated sandbox and spawns two workers; the run returns artifacts, tests and provenance; deterministic validation accepts or rejects them; the outcome, including failures, is recorded without exposing host credentials.

No experimental worker writes authoritative Atlas or Lattice state.
