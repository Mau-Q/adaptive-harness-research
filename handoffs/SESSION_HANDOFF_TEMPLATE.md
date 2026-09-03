# Research Session Handoff Template

Use at the end of any substantial ChatGPT/Codex research or implementation session.

The purpose is to make future sessions recover **decision-relevant state**, not the full conversation.

---

## Session identity

Date:
Host:
Model:
Conversation/session reference:
Primary topic:

## Starting state

Current canonical project state used:
Relevant documents/commits:
Known uncertainties at start:

## Question actually investigated

...

## External prior art checked

- source:
- source:
- source:

If none:
`PRIOR_ART_NOT_CHECKED`

## Key findings

1.
2.
3.

## What changed

### Canonical understanding
...

### Architecture
...

### Implementation status
...

### Terminology
...

### Prior-art relationship
...

If nothing changed:
`NO_CANONICAL_CHANGE`

## What did NOT change

- ...
- ...

This section is mandatory when new evidence was interesting but did not justify reopening architecture.

## Superseded or weakened beliefs

- previous belief:
- new status:
- reason/evidence:

## Claims and evidence

| Claim | Evidence | Strength | Current status |
|---|---|---|---|
| ... | ... | low/medium/high | current/historical/proposal |

## Open questions

1.
2.
3.

## Next highest-value question

...

Why it can change a decision:
...

## Build/adopt decision

`ADOPT / EXTEND / COMPOSE / BUILD / DROP / RESEARCH_MORE / NONE`

Reason:
...

## Files that should be updated

- [ ] `00_CURRENT_STATE.md`
- [ ] `DESIGN_HISTORY.md`
- [ ] prior-art audit record
- [ ] implementation status matrix
- [ ] failure corpus
- [ ] experiment results
- [ ] none

## Authority boundary

This handoff is:
`RESEARCH_RESULT / PROPOSAL / IMPLEMENTATION_RESULT / VALIDATED_RESULT`

It does not silently authorize:
- architecture adoption;
- implementation;
- external calls;
- release;
- publication;
- repository mutation outside the authorized scope.
