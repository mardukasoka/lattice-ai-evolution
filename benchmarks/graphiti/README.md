# Graphiti temporal regression gate (not yet executed)

**Scope:** Indigo Atlas synthetic software-history episodes; no external API calls or live code execution.

## Preflight result
- Fork: `mardukasoka/graphiti`, version `graphiti-core==0.31.2` in inspected pyproject.
- Graphiti is not installed in the current execution environment; neither Neo4j nor FalkorDB is present. **No actual Graphiti run or benchmark pass is claimed.**
- Upstream README documents Neo4j/FalkorDB and default OpenAI-backed extraction/embedding. An offline run requires explicit mock LLM/embedder and isolated database or a local provider; no paid API should be called.
- Existing ClickUp task `14yr2e53890` records a reported Fractal/Sagent/Trackinizer P0 PASS, pending log verification; not evidence of Graphiti readiness.

## Fixture
See `graphiti-temporal-fixture.json`. Synthetic event chronology: unsupported -> supported -> regressed for Lua-to-Python switch, plus unrelated C-to-CSharp loop support. These are deliberately fictional test facts, NOT claims about actual Transpiler functionality.

## Execution gate
1. Install pinned `graphiti-core==0.31.2` in an isolated CI environment with ephemeral FalkorDB/FalkorDBLite (if compatible) or Neo4j. No secrets or network access to provider APIs.
2. Configure a deterministic fake extraction and embedding provider, or a verified local free provider. Record exact provider configuration; no LLM-generated answers in first gate.
3. Insert episodes with timestamps and unique source IDs; independently query temporal edges and source episode provenance at all four fixture dates.
4. Verify supersession does not delete historical claims, invalidate unrelated entities, or change earlier as-of answers. Restart database and repeat.
5. Report precision/recall on 4 dated queries, source-ID correctness, unrelated-fact false invalidations, persistence, elapsed time, memory, dependency and CI cost.
6. Repeat the same fixture through a timestamped Cognee baseline, preserving identical source IDs and evaluation rules. Do not claim a winner before both run.

## Pass criteria
- 4/4 as-of queries correct; 4/4 correct source IDs.
- Zero unrelated fact invalidations; all three historical Lua-to-Python claims retained.
- Persistence and restart verification passes.
- No paid external calls or secrets; full reproducible CI logs and artifacts.

## Security and cost
Fractal defaults to bypassing approval prompts and Sagent docs explicitly say it is NOT a sandbox. Do not combine either with this benchmark until isolated. Graphiti's default OpenAI configuration must not be used accidentally.

## ClickUp optimization review
Requested via comment on https://app.clickup.com/t/14yr2e53890 . Posting the comment does not mean ClickUp Brain has run an AI review.
