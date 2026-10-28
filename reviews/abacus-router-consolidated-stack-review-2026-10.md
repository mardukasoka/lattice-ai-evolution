# Indigo Atlas — Abacus Router Consolidated Cognitive / RSI Stack Review
Date: 2026-10-29
Status: REVIEW REQUEST — read-only; no deployment or self-modification authorized.

## Objective
Review and consolidate existing Indigo Coding Council, cognitive memory, recursive agent orchestration, and universal transpiler resources. Recommend an evidence-based, mobile-first, low-cost-first integration with Beam as a prospective coding model and eventual fine-tuning target. Do not duplicate existing systems.

## Confirmed GitHub inventory
- https://github.com/mardukasoka/fractal — recursive worktree agent orchestration
- https://github.com/mardukasoka/sagent — agent execution candidate
- https://github.com/mardukasoka/trackinizer — experiment and provenance candidate
- https://github.com/mardukasoka/letta — persistent agent memory candidate (MemGPT lineage)
- https://github.com/mardukasoka/graphiti — temporal knowledge graph candidate; **NO GRAPHITI TESTS YET**
- https://github.com/mardukasoka/cognee — ingestion/knowledge retrieval candidate; prior small Cognee smoke test in chess-atlas
- https://github.com/mardukasoka/chess-atlas — benchmark harness; branch indigo/knowledge-memory-benchmark; Cognee and LightRAG probes; do not infer production readiness
- https://github.com/mardukasoka/transpiler — existing universal source-to-source compiler, limited language subsets; correctness not guaranteed
- https://github.com/mardukasoka/lattice-ai-evolution — bounded recursive improvement laboratory
- https://github.com/mardukasoka/webllm — existing browser Council/model-routing candidate
- https://github.com/mardukasoka/harness2 — existing agent tooling / schema candidate
- https://github.com/mardukasoka/openrig — previously assessed orchestration candidate
External candidates: Beam (verify model identity, license, availability, inference API, VRAM/compute, adapter training); Abacus Router (verify actual available access and billing). LightRAG may be an installed dependency in chess-atlas, not a canonical independent fork.

## Current evidence and cautions
- Cognee smoke: 3/3 retrieval contexts contained expected tokens; does NOT prove per-source attribution or generated-answer correctness.
- LightRAG deterministic local probe: 4/4 documents ingested, expected source labels present for 2/3 answerable questions; non-semantic hashed embeddings, stub extraction, no graph/answer accuracy. Its no-context sentinel was misclassified as nonempty; native reference IDs were blank.
- Graphiti: **untested**. Letta: **untested**. Fractal–Sagent–Trackinizer integration: historical compatibility discussion is not current deployment proof.
- Fractal upstream README warns its seeded agents bypass approval prompts and worktrees do not isolate credentials, filesystem or network. Do not run unattended with production secrets.
- Cognee is a knowledge/memory layer, NOT Beam inference hosting; verify inference deployment separately.
- The Coding Council already exists: discover and preserve its implementation rather than designing another council.

## Review workstreams (READ ONLY)
1. Inventory exact repositories, default branches, commits, languages, dependencies, licenses, maintenance status, test workflows, permissions and security risks. Locate actual Coding Council and Abacus Router integration, distinguishing confirmed files from assumptions.
2. Trace Fractal -> Sagent -> Trackinizer interfaces. Assess integration tests, run isolation, cost/time/depth limits, replayability, artifacts and provenance. Compare existing orchestration alternatives; avoid duplicate daemons.
3. Compare Letta, Graphiti, Cognee and LightRAG by responsibilities: persistent per-agent memory, temporal graph, scientific provenance, ingestion/retrieval. Design one canonical Atlas knowledge schema and adapter interfaces, not four competing truth stores. Give Graphiti a minimal independent smoke test plan, with source IDs, temporal updates, persistence, retrieval, and abstention.
4. Evaluate Beam inference feasibility and model/provider specifics using authoritative primary documentation. Separate inference, RAG, agent learning, supervised fine-tuning/LoRA and RL. Estimate hardware, GPU hours, model licensing, storage and data governance. No unapproved spending.
5. Audit transpiler supported languages and versions, architecture, parsers, generators, tests, security, and feasibility of typed intermediate representation. Keep code transpilation separate from documents/media/CAD format conversion; preserve round-trip fidelity and semantic equivalence as applicable.
6. Specify one narrow improvement experiment: baseline supported conversion; one missing feature; independently verified compile/run/property tests; isolated feature branch; Council review; Trackinizer artifact lineage; optional Beam training example only after independent validation. Use held-out tests and report regressions.
7. Examine WebMCP as optional browser tool interface, not replacement for model hosting or backend MCP; progressive enhancement for mobile GitHub Pages.
8. Cost, threat and failure analysis: prompt injection from retrieved docs, malicious code execution, credential isolation, sandboxing, package supply chain, data poisoning, training contamination, runaway recursive tasks, regression masking.

## Required deliverables
- Evidence matrix per repo: confirmed / tested / inferred / unknown with file paths and commit hashes.
- One dependency and dataflow diagram showing existing Council, Beam inference, Fractal/Sagent/Trackinizer, Letta/Graphiti/Cognee/LightRAG, Atlas KG, transpiler and evaluation gate.
- Decision table: adopt / adapt / defer / reject, rationale, overlap, estimated compute/cost, risks.
- Concrete Graphiti smoke test plan and baseline parity evaluation against Cognee and LightRAG.
- Beam inference and fine-tuning readiness gate with explicitly sourced model claims and hardware requirements.
- Three-phase implementation plan (read-only audit -> isolated test -> supervised PR), with acceptance criteria, rollback and estimated time/cost.
- List blockers and questions requiring explicit human authorization.

## Hard constraints
Read-only investigation. Do not merge, deploy, spend money, trigger unattended loops, fine-tune, rotate credentials, or write to production systems. No claims of successful tests without actual logs and artifacts. Keep the existing Council and repositories; propose minimal adapters and branch-only changes for later authorization.