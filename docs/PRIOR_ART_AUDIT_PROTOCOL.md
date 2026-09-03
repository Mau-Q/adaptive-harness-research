# Prior-Art Audit Protocol

Status: `ACTIVE RESEARCH PROTOCOL`

## Purpose

Prevent **prior-art blindness / reinvention failure**.

This protocol must run before a major Harness mechanism is treated as an original design direction or before a substantial new subsystem is built.

## Core rule

> Search before architecture.

Internal reasoning may formulate the problem, but it must not be treated as evidence that the problem is novel or unsolved.

## 1. Unit of audit

Audit one mechanism/problem at a time.

Current candidate topics include:

- state/control-oriented agent supervision
- runtime governance / path-dependent policy
- receding-horizon planning / bounded execution
- risk-proportional / right-sized assurance
- owner scope / claim ownership
- decision-value / information-value gating
- done-enough / stop conditions
- claim–argument–evidence–defeater structures
- verification and false completion
- control-consumption / runtime enforcement
- historical Finding / memory applicability
- context persistence / long-horizon state
- Maker/Checker independence
- runtime portability / host-neutral governance
- meta-harness / multi-runtime orchestration
- Harness self-evaluation / ablation / falsification
- long-horizon reward hacking
- adaptive simplification as models improve

Do not audit all topics superficially in one pass.

## 2. Required source classes

For each mechanism, inspect at least:

### Academic
- arXiv and relevant conference/workshop literature
- software engineering / dependable systems literature when applicable
- agent evaluation and long-horizon coding research

### Frontier labs
- OpenAI
- Anthropic
- Google / DeepMind
- Microsoft
- other directly relevant model/runtime teams

### Open source
- production coding-agent harnesses
- orchestration frameworks
- runtime governance systems
- benchmark/evaluation projects

### Industry / infrastructure
- runtime systems
- observability/evaluation vendors
- workflow/durable execution systems
- governance/security products

Prefer primary sources over summaries.

## 3. Audit questions

For every topic answer:

1. **Internal problem**
   - What exact failure or need did we observe?

2. **External terminology**
   - What does the research/industry call this problem?

3. **Existing work**
   - Which papers, systems, frameworks, products, or benchmarks address it?

4. **Maturity**
   - `MATURE`
   - `EMERGING`
   - `FRAGMENTED`
   - `OPEN`
   - `UNKNOWN`

5. **Existing implementation**
   - Is there production or open-source code?
   - Is it host-specific or general?

6. **Evidence quality**
   - conceptual only?
   - benchmark?
   - controlled ablation?
   - production evidence?
   - longitudinal evidence?

7. **Known limitations**
   - What failures are already documented?

8. **Internal relationship**
   - Are we:
     - `REDISCOVERING`
     - `ADOPTING`
     - `EXTENDING`
     - `COMPOSING`
     - `CONTRADICTING`
     - `POSSIBLY NOVEL`
     - `UNKNOWN`

9. **Action**
   - `ADOPT`
   - `EXTEND`
   - `COMPOSE`
   - `BUILD`
   - `DROP`
   - `RESEARCH_MORE`

10. **Falsifier**
    - What evidence would change this conclusion?

## 4. Required output format

Use one record per audited mechanism:

```text
TOPIC:
...

INTERNAL_PROBLEM:
...

EXTERNAL_TERMINOLOGY:
...

KEY_PRIOR_ART:
- ...
- ...

MATURITY:
...

WHAT_IS_ALREADY_SOLVED:
...

KNOWN_LIMITATIONS:
...

OUR_CURRENT_IDEA:
...

RELATION_TO_PRIOR_ART:
REDISCOVERING / ADOPTING / EXTENDING / COMPOSING /
CONTRADICTING / POSSIBLY_NOVEL / UNKNOWN

RECOMMENDED_ACTION:
ADOPT / EXTEND / COMPOSE / BUILD / DROP / RESEARCH_MORE

CONFIDENCE:
LOW / MEDIUM / HIGH

FALSIFIER:
...
```

## 5. Research discipline

### Do not
- call an idea “ours” before prior-art review;
- infer novelty from unfamiliarity;
- rely on model memory for a fast-moving field;
- treat one recent paper as field consensus;
- treat GitHub popularity as evidence of correctness;
- build because an implementation looks technically interesting;
- create a new subsystem merely to unify vocabulary.

### Do
- separate “independently rediscovered” from “novel”;
- preserve external names even if internal vocabulary differs;
- prefer existing mature primitives;
- explicitly record when an internal idea should be deleted;
- revisit conclusions as models/runtimes evolve.

## 6. Architecture gate

No major new implementation should pass this gate unless:

```text
PROBLEM_FORMULATED = YES
PRIOR_ART_SCANNED = YES
EXISTING_SOLUTIONS_COMPARED = YES
RESIDUAL_GAP_EXPLICIT = YES
BUILD_OR_EXTENSION_JUSTIFIED = YES
FALSIFIABLE_EXPERIMENT_DEFINED = YES
```

Otherwise:

```text
ARCHITECTURE_ACTION = DO_NOT_BUILD_YET
```
