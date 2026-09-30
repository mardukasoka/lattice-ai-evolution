# Lattice AI Evolution — Architecture

This repository implements the architecture independently audited during the Abacus review.

## Canonical control flow

```text
Human
  |
Council — deliberation / audit, not ordinary execution
  |
Sagent Supervisor — finite orchestration
  |\
  | Trackinizer — append-only evidence/provenance DAG
  |
  +-- TaskTicket --> Fractal Sandbox — untrusted bounded recursive execution
                         |
                      artifacts
                         |
                Deterministic Validation Gate
                         |
                    accept / reject
                         |
                     Trackinizer
```

## Invariants

1. Sagent is the root finite orchestrator.
2. Fractal is an untrusted batch execution substrate. It returns artifacts and never writes authoritative Atlas or Lattice state.
3. Trackinizer records evidence, experiments, failures, provenance and promoted artifacts.
4. Deterministic validation precedes promotion.
5. Council deliberates on ambiguity, conflict and promotion policy; it is not a workflow executor.
6. RRSI-style regularization governs recursive improvement experiments and held-out transfer evaluation.
7. PufferLib is used only where a genuine RL environment exists.
8. SOM is an analytics/relevance layer, never the supervisor.
9. Lattice ethics supplies questions, constraints and trajectory analysis, not autonomous normative authority.
10. Atlas/Uranometria are scientific environments and consumers of validated capabilities, not writable targets for experimental workers.

## Trust boundary

Fractal workers run in ephemeral isolated environments with bounded CPU, memory, time, descendants and cost. Production repositories, host credentials and unrestricted network access are outside the sandbox. A TaskTicket declares allowed tools and limits. Returned artifacts include provenance and test logs.

## Promotion rule

Experiment -> artifact -> deterministic checks -> held-out/transfer evaluation where applicable -> Council review when epistemically ambiguous -> Trackinizer record -> explicit promotion.

Rejected experiments remain evidence.
