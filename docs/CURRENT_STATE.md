# Adaptive Harness Research — Current State

Status: `RESEARCH / PRE-IMPLEMENTATION`
Last updated: 2026-09-03

## 1. Current problem statement

The project is **not yet defined as a new Harness framework**.

The current research question is:

> In AI software development, what engineering-control responsibilities still need to exist outside the model, which should be delegated to the runtime/host, which belong to ordinary software engineering, and which require Human authority?

A more implementation-oriented wording is:

> How should a coding-agent system adapt its engineering controls according to live state, evidence, uncertainty, authority, risk, and task horizon—without collapsing into a fixed workflow or an ever-growing policy stack?

## 2. Current conceptual direction

The strongest internal direction so far is:

- move from **Prompt/Workflow-centered** thinking toward **State/Control-centered** thinking;
- keep the planner/model capable and flexible;
- keep governance thin and focused on stable semantic/normative boundaries;
- let runtime/host primitives own commodity execution machinery where possible;
- treat workflow as a possible output of control decisions, not necessarily the primary abstraction;
- prefer bounded/receding-horizon execution over long fixed trajectories;
- vary assurance rigor according to project context, risk, claim strength, and lifecycle;
- distinguish the existence of a rule from proof that the rule was actually consumed at the relevant execution boundary;
- preserve Human authority and avoid silently converting qualification, evidence, or historical experience into authorization;
- treat Harness mechanisms themselves as falsifiable and removable.

## 3. Important historical evolution

The design did **not** begin here. It passed through several forms:

1. Codex-oriented prompt/policy workflow.
2. Strategy / Prompt / Finding split with D0/D1/D2 routing.
3. Repository Harness + task-level Harness.
4. Runtime Admission and control-consumption enforcement.
5. Harness VNext and state/control-oriented reasoning.
6. Pi / OpenCode / DeepSeek Harness portability research.
7. Thin Governance + Host/Runtime-owned execution plumbing.
8. Dynamic Harness discussions.
9. Adaptive Engineering Control framing.
10. Current realization: before further design or implementation, the whole history must be aligned against external prior art.

This chronology is provisional until the historical reconstruction is complete.

## 4. What is already relatively clear

### Stable candidate principles

These appear repeatedly across the historical work and should be treated as **research hypotheses**, not unquestionable truth:

- `qualification != authorization`
- no silent authorization expansion
- stale authority cannot silently become current authority
- Human-required authority cannot be inferred from convenience
- restrictive historical findings may constrain but must not create new authority
- test/evaluate system invariants rather than demand one fixed trajectory
- evidence strength should bound decision/claim strength
- historical knowledge needs applicability + provenance + lifecycle
- `STOP`, `ASK`, `PIVOT`, `DO_NOTHING`, read-only, and dry-run can be legitimate control actions
- “done enough” should be scoped to the current owner/claim/lifecycle, not maximal imaginable completeness
- a mechanism should only remain if its value can be demonstrated or its risk-control role is justified

### Important implementation-boundary hypothesis

Likely split:

- **Model / Planner:** reasoning, proposing actions, implementation choices
- **Runtime / Host:** agent loop, sessions, tools, sandbox, execution plumbing, retry, extension lifecycle
- **Engineering Control / Governance:** stable boundaries, authority, evidence requirements, control decisions
- **Software Engineering:** architecture, requirements, tests, review, CI, observability, repository contracts
- **Human:** goals, value judgments, material authority, adoption, unresolved semantic/product decisions

This split is not frozen.

## 5. What is NOT yet proven

Do not claim any of the following without new evidence:

- that “Adaptive Engineering Control” is a novel research contribution;
- that a new standalone Harness product/framework is needed;
- that the current design improves coding-agent performance;
- that the current design is better than existing open-source or commercial harnesses;
- that the current set of failure modes is complete;
- that a context compiler or meta-harness needs to be built from scratch;
- that all earlier internal mechanisms should remain;
- that Runtime Admission, Finding Recall, Maker/Checker, Context Compiler, or other mechanisms belong in the final architecture;
- that the current vocabulary matches the vocabulary used by the research community.

## 6. Current highest-priority next step

`PRIOR_ART_RECONSTRUCTION`

Before new architecture or implementation work:

1. reconstruct the major historical internal concepts;
2. map each concept to current external terminology and prior art;
3. identify mature existing solutions;
4. classify internal ideas as:
   - `ADOPT`
   - `EXTEND`
   - `COMPOSE`
   - `BUILD`
   - `DROP`
   - `UNKNOWN`
5. identify what remains genuinely unresolved and worth experimenting on.

## 7. Stop rule

Do **not** create a new large Harness architecture, runtime, event store, scheduler, meta-harness, context platform, or plugin framework merely because a plausible gap is discovered.

A new implementation direction requires:

- a clearly formulated gap;
- external prior-art review;
- evidence that existing capabilities are insufficient for the intended use;
- a bounded experiment or reference implementation;
- a falsifiable success criterion.
