# Adaptive Harness Research

Status: `RESEARCH / PRE-IMPLEMENTATION`

Repository identity: `PROVISIONAL`

Current highest-priority action: `PRIOR_ART_RECONSTRUCTION`

## What this repository is

This is a research-oriented engineering repository for curating the current
state, historical decisions, prior-art reviews, experiments, failures, and
open questions around Coding Agent systems. The working research name is
`Adaptive Harness Research`; it is not a commitment to a final product name,
architecture, or originality claim.

The research scope includes:

- Harness Engineering;
- Runtime Governance;
- Adaptive Engineering Control;
- long-horizon software-engineering agents;
- verification and assurance;
- state and context continuity;
- authority, evidence, and control;
- Harness evaluation and prior-art reconstruction.

The repository is intended to become curated canonical research knowledge for
future Human, ChatGPT, and Codex work. Raw ChatGPT/Codex history remains
private/raw research evidence and is not automatically current truth.

## What this repository is not

It is not:

- a mature Harness Framework;
- a new general-purpose Agent Runtime;
- a claim that the current concepts are original;
- a claim that the current architecture is better than Codex, Claude Code,
  Pi, OpenCode, or another existing Harness;
- a plan to reimplement commodity capabilities already supplied by a mature
  Runtime or Host;
- an automatic import of private ChatGPT/Codex conversations, local Memory,
  or Codex session data.

No framework implementation has started in this repository.

## Current research questions

> In AI software development, what engineering-control responsibilities still
> need to exist outside the model, which should be delegated to the
> runtime/host, which belong to ordinary software engineering, and which
> require Human authority?

> How should a coding-agent system adapt its engineering controls according to
> live state, evidence, uncertainty, authority, risk, and task horizon without
> collapsing into a fixed workflow or an ever-growing policy stack?

## Current priority

`PRIOR_ART_RECONSTRUCTION`, not Framework implementation.

The next research stage is to reconstruct the internal design history and
implementation/completion state, align each major concept with external
terminology and prior art, and identify any residual gap worth a bounded,
falsifiable experiment. That work is not started automatically by this
bootstrap.

## Research discipline

> Search before architecture.

An important mechanism must receive a prior-art review before it is treated as
an original direction or used to justify a substantial new subsystem. Internal
discussion can formulate a problem, but it is not evidence that the problem is
novel or unsolved.

## Source-of-truth and status discipline

The repository keeps these statuses distinct:

| Status | Meaning |
|---|---|
| `CURRENT` | Current accepted project understanding or authority |
| `HISTORICAL` | A prior state or past decision |
| `PROPOSAL` | A suggested direction not yet adopted |
| `RESEARCH_RESULT` | A bounded research conclusion |
| `IMPLEMENTED` | Implemented in a named codebase or artifact |
| `VALIDATED` | Supported by the stated validation evidence |
| `ADOPTED` | Explicitly accepted for ongoing use |
| `SUPERSEDED` | Replaced or weakened by later evidence/decision |
| `UNKNOWN` | Not established by the available evidence |

These labels must not be collapsed into one another. In particular,
discussion is not implementation, implementation is not adoption, and a test
or report is not automatically useful real-world effect.

## Repository map

- [Current State](docs/CURRENT_STATE.md) — current research framing and stop
  rule.
- [Prior-Art Audit Protocol](docs/PRIOR_ART_AUDIT_PROTOCOL.md) — required
  audit questions and architecture gate.
- [Research Backlog](docs/RESEARCH_BACKLOG.md) — decision-value-ordered
  questions and future bounded experiments.
- [Design History](docs/DESIGN_HISTORY.md) — provisional phases awaiting
  reconstruction.
- [Terminology](docs/TERMINOLOGY.md) — provisional internal working terms.
- [Open Questions](docs/OPEN_QUESTIONS.md) — unresolved research questions,
  not feature commitments.
- [Prior-Art Audits](prior-art/audits/README.md) — one record per audited
  mechanism.
- [Experiments](experiments/README.md) — experiment principles; no benchmark
  was started in this bootstrap.
- [Failures](failures/README.md) — future curated and anonymized failure
  patterns.
- [Session Handoff Template](handoffs/SESSION_HANDOFF_TEMPLATE.md) — concise
  provenance-bearing continuity between research sessions.

## Bootstrap provenance and boundary

The four initial research documents were recovered from the local archive
`adaptive-harness-research-pack.zip` and migrated without changing their
research semantics. The archive itself is not committed.

This bootstrap does not import private conversations, personal Memory,
Codex JSONL, or complete transcripts. It does not call a model/API, run a
benchmark, create a runtime, create a database or platform, or make a public
novelty claim.
