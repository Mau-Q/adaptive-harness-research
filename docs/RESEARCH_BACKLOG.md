# Research Backlog

Status: `ACTIVE`
Rule: prioritize by **decision value**, not by conceptual attractiveness.

## P0 — Reconstruct current truth

### R0.1 Historical design reconstruction
Goal:
- produce a reliable timeline from early Codex Harness work to the current Adaptive Engineering Control framing.

Inputs:
- ChatGPT conversation exports
- Codex session/rollout summaries
- current policies
- implementation plans
- repository state
- Pi/OpenCode/DSH experiments

Output:
- `DESIGN_HISTORY.md`
- major supersession relationships
- current vs historical vs experimental separation

Done when:
- major architecture phases can be recovered without rereading all raw chats;
- each major phase has provenance;
- current completion state is explicit.

### R0.2 Completion-state reconstruction
Goal:
- determine what was only discussed, what was implemented, what was tested, what was adopted, and what was later externalized/deprecated.

Output:
- capability/status matrix:
  `DESIGNED / IMPLEMENTED / VALIDATED / ADOPTED / EXTERNALIZED / SUPERSEDED / UNKNOWN`

## P0 — External prior-art alignment

Run the Prior-Art Audit Protocol on the following first:

### R1. Runtime governance / path-dependent control
Decision question:
- Is our state/control framing already covered by existing runtime-governance work?

### R2. Harness evaluation / ablation
Decision question:
- What is the best existing methodology for measuring Harness value and overhead?

### R3. Long-horizon context/state continuity
Decision question:
- Is a custom Context Compiler necessary, or can existing model/runtime/project primitives solve most of the problem?

### R4. Verification / false completion / reward hacking
Decision question:
- Which verification problems are already well-defined and benchmarked?

### R5. Adaptive/right-sized engineering assurance
Decision question:
- Which parts are existing risk-tiering practice, and what remains coding-agent-specific?

## P1 — Reclassify internal concepts

After R1–R5, classify:

| Internal concept | Status to decide |
|---|---|
| State/Control-centered Harness | ADOPT / EXTEND / COMPOSE / BUILD / DROP |
| Receding-horizon execution | ... |
| Owner-actionability | ... |
| Decision-value gate | ... |
| Done Enough | ... |
| Execution Findings | ... |
| Control Consumption | ... |
| Runtime Admission | ... |
| Maker/Checker | ... |
| Thin Governance | ... |
| Context Compiler | ... |
| Meta-governance | ... |
| Adaptive Engineering Control | ... |

## P1 — Find residual gaps

Only after the mapping, identify 1–3 gaps that satisfy all:

- materially important for AI software development;
- not already adequately solved by model/runtime/framework;
- observable in real tasks;
- measurable;
- small enough for a bounded experiment;
- likely to remain relevant across model upgrades.

## P2 — Minimal experiments

For each residual gap:

```text
same model
same repo
same starting state
same task
```

Compare:

- baseline
- existing mature solution (if available)
- minimal internal extension

Measure at least:

- task success
- false completion
- wrong-trajectory persistence
- scope creep
- unnecessary intervention
- Human rescue
- regression
- cost/token/runtime overhead
- time to correct solution

## P2 — Decide repository identity

Only after the first prior-art reconstruction decide whether the public GitHub repository should primarily be:

- a new Harness;
- an adaptive control extension;
- a benchmark/evaluation suite;
- a research/knowledge repository;
- a reference implementation;
- a set of plugins/skills for existing hosts;
- or some combination.

Do not lock the repository identity before this decision.

## Explicit non-goals for now

- no full framework rewrite;
- no custom agent runtime;
- no new event-store platform;
- no generic plugin ecosystem;
- no large vector database / GraphRAG system merely for project memory;
- no public novelty claims;
- no broad promotion before reproducible evidence exists.
