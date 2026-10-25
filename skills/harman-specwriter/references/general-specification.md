# General Specification

The document that gives everyone working on or with the project a common knowledge of it and of its
domain. It holds the components below, in this order. The shared sections of `SKILL.md` —
*Asking*, *Open questions*, *Shared checks* — apply throughout.

Interview in the same order, except for the Glossary: collect its terms as they come up — whenever
the Human uses a word with a project-specific meaning, confirm its definition. Propose terms one per
question, at most four per round, each with its whole row — definition and words to avoid — in the
question.

## Components

### Glossary
Domain- and project-specific terms, each with a one-line definition — not general vocabulary or
common technical terms. One name per concept and one meaning per name: when the Human uses several
words for one thing, agree on the term with them and list the others as words to avoid.
- A definition uses the Glossary's own terms, and never a word another row lists to avoid.
- A word several concepts share — loop, session, cycle — is never a term on its own: each concept
  gets a qualified name (learning loop, Build-Measure-Learn loop).
- A term goes in only when the document uses it. Rows are in alphabetical order.

### Vision
The vision in *The Lean Startup*'s sense: the startup's true north — the lasting change the project
wants to make in the world. Strategy may pivot and the product is tuned all the time; the vision
stays. A few sentences.
- If it names a feature, a channel, or a technology, it is strategy or product, not vision — ask
  what lies behind it.

### Problem
Who has the problem, what it is — how often it happens, what it costs them — and how they cope today:
competing products, workarounds, or nothing at all, and why that falls short. These ways of coping
are the alternatives *The wedge* is measured against.
- A claim the Human believes but has not observed is a leap-of-faith assumption: ask whether it
  belongs among the *Hypotheses*.
- *Today* is a table — the way of coping, its tools, why it falls short — with a *Nothing* row when
  people simply do without.

### The wedge
The project's edge over those alternatives: what it does that they can't or won't, which lets it
break into the market.
- Ask what exactly differs, and why the alternatives can't or won't match it — cost, technology,
  business model, access, insight. An edge anyone could copy tomorrow, such as "better UX" on its
  own, is a question, not a wedge.
- Write the edge as a short list of what the project does, then a table against the Problem's
  alternatives: a row per point of difference, and a row for why each alternative can't or won't
  match it.

### Build sequence
The phases that take the project from its first release toward the Vision, each with its goal and
the features it includes. Every feature sits in exactly one phase, and the first phase holds the
MVP.
- Phase 1's features are the MVP's: point to the MVP instead of repeating the list.
- A source's deferred or out-of-scope items go into the phase it names, or into a last phase,
  *Later*; ask only whether any of them is a non-goal instead.

### Hypotheses
The two leap-of-faith assumptions of *The Lean Startup*:
- **Value hypothesis** — whether the product really delivers value to customers once they use it.
- **Growth hypothesis** — how new customers will discover the product: its engine of growth, sticky
  (customers stay), viral (customers bring customers), or paid (acquiring a customer costs less
  than the customer brings in).

State each so that it can be proven wrong, with the signal that confirms or refutes it — a
measurable behaviour and its threshold. "Users like it" is not a signal: ask which behaviour would
show it. When the Human names a vanity metric (total sign-ups), propose an actionable one (cohort
retention, conversion) — the choice stays theirs.
- Under each hypothesis, list the leap-of-faith assumptions it rests on, riskiest first. A source's
  "riskiest assumptions" land here; one about reaching customers belongs to the growth hypothesis.
- A signal made of several gates is one table in reading order — `# | Gate | Measures | Passes when
  | Role | If it fails` — where *Passes when* holds only the threshold. The rules all gates share
  (when they are set, what a fail triggers, when a threshold may change, what is pooled) are a list
  above it, and each role (precondition, verdict, …) is defined in a line. A verdict read from two
  gates is a 2×2 table; a weighting by segment is a table of its own. Outcomes are *pass* and
  *fail*, and a failed gate need not be a kill: write what it triggers.
- A check the source leaves without a threshold, such as a comparison with the alternatives or
  willingness to pay, stays without one: write how it is checked and what its absence means.
- A growth hypothesis the source defers on purpose is written as deferred, with an open question
  for when it gets stated.

### MVP
The smallest feature scope that tests both hypotheses — in *The Lean Startup*'s terms, the version of
the product that completes a full turn of the Build-Measure-Learn loop with the least effort. It
lists its features, all from the first phase, and how it produces each hypothesis' signal.
- A feature that serves neither hypothesis is a question: ask whether it belongs in the MVP.
- *Features* and *Tests* are lists. How the signals get produced — the experiment's rules and
  rollout, the instruments and diagnostic measures, the conversations and their calendar, any
  performance budget — goes in subsections under the MVP, as lists and tables.
- Name capabilities, not tools or vendors: those belong to a Technical Specification.

### Other components
Fit source material into the components above first; the table below says where common material
goes. Add another component — target customers, constraints, non-goals — only when the Human asks
for it or confirms your proposal of it, and only for material with no home above: never as a place
for leftovers. It goes after the MVP unless they want it elsewhere.

| Source material | Goes to |
| --- | --- |
| Competitors, workarounds, market notes | Problem → Today |
| Differentiation, a positioning sentence | The wedge |
| Deferred and out-of-scope items | Build sequence — the phase named, or Later |
| Riskiest assumptions | Hypotheses — under the hypothesis each belongs to |
| Metrics, gates, thresholds, how to read them | Hypotheses → Signal |
| Validation approach, experiment rules, rollout | MVP |
| Instrumentation, diagnostic measures, interviews | MVP |
| Performance or quality budgets | MVP |
| Reasons, history, status, change notes | Not carried |

## Checks

- The Vision names no feature, channel, or technology.
- The wedge is measured against the alternatives the Problem names.
- Every feature of the Build sequence sits in exactly one phase, and the phases lead toward the
  Vision.
- The MVP fits inside the first phase and produces both hypotheses' signals; each hypothesis can be
  refuted.
- No feature list appears twice: Phase 1 points to the MVP.
- Every *Passes when* holds a bare threshold.

## Template

````markdown
# General Specification: <project>

- **Updated**: <YYYY-MM-DD>

## Glossary

| Term | Definition |
| --- | --- |
| <Term> | <one-line definition; words to avoid, if any> |

## Vision
<a few sentences: the lasting change the project wants to make>

## Problem
- **Who**:
  - <the customers or users who have it>
- **Problem**:
  - <what goes wrong for them>
  - <how often it happens>
  - <what it costs them>
- **Today** — how they cope, and why it falls short:

| Way of coping | Tools | Why it falls short |
| --- | --- | --- |
| <way of coping> | <products, or —> | <why> |

## The wedge
**<the edge, in a few words>** — <what the customer hands over, and gets>:
- <what the project does that the alternatives don't>

| | <project> | <alternative> |
| --- | --- | --- |
| <point of difference> | <how the project does it> | <how the alternative does it> |
| Why it won't match | — | <cost, technology, business model, access, insight> |

## Build sequence

### Phase 1 — <name>
- **Goal**: <what the phase achieves>
- **Features**: the MVP's (see MVP).

### Phase 2 — <name>
- **Goal**: <what the phase achieves>
- **Features**:
  - <feature>

## Hypotheses

### Value hypothesis
- **Hypothesis**: <the falsifiable assumption>
- **Assumptions**, riskiest first:
  1. <assumption>
- **Signal**: <one behaviour and its threshold, or: the gates below>

#### Gates
- <a rule all gates share>

| # | Gate | Measures | Passes when | Role | If it fails |
| --- | --- | --- | --- | --- | --- |
| 1 | <gate> | <what it counts> | <threshold only> | <role> | <what a fail triggers> |

### Growth hypothesis
- **Hypothesis**: <how new customers find the product; its engine of growth — or: deferred>
- **Signal**: <the behaviour and threshold that confirm it; below the threshold it is refuted>

## MVP
- **Features** — all of Phase 1:
  - <feature>
- **Tests**:
  - value hypothesis — <how the MVP produces its signal>
  - growth hypothesis — <how>

### <how a signal gets produced: rollout, instruments, conversations, a budget>
<lists and tables>

## Open questions
- **Q1 — <component>**: <the question> — <the options discussed and your recommendation, if any>
<or: None.>
````
