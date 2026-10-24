# General Specification

The document that gives everyone working on or with the project a common knowledge of it and of its
domain. It holds the components below, in this order. The shared sections of `SKILL.md` —
*Asking*, *Open questions*, *Shared checks* — apply throughout.

Interview in the same order, except for the Glossary: collect its terms as they come up — whenever
the Human uses a word with a project-specific meaning, confirm its definition.

## Components

### Glossary
Domain- and project-specific terms, each with a one-line definition — not general vocabulary or
common technical terms. One name per concept and one meaning per name: when the Human uses several
words for one thing, agree on the term with them and list the others as words to avoid.

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

### The wedge
The project's edge over those alternatives: what it does that they can't or won't, which lets it
break into the market.
- Ask what exactly differs, and why the alternatives can't or won't match it — cost, technology,
  business model, access, insight. An edge anyone could copy tomorrow, such as "better UX" on its
  own, is a question, not a wedge.

### Build sequence
The phases that take the project from its first release toward the Vision, each with its goal and
the features it includes. Every feature sits in exactly one phase, and the first phase holds the
MVP.

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

### MVP
The smallest feature scope that tests both hypotheses — in *The Lean Startup*'s terms, the version of
the product that completes a full turn of the Build-Measure-Learn loop with the least effort. It
lists its features, all from the first phase, and how it produces each hypothesis' signal.
- A feature that serves neither hypothesis is a question: ask whether it belongs in the MVP.

### Other components
Add one — target customers, competitors, constraints, non-goals, risks — only when the Human asks
for it or confirms your proposal of it. It goes after the MVP unless they want it elsewhere.

## Checks

- The Vision names no feature, channel, or technology.
- The wedge is measured against the alternatives the Problem names.
- Every feature of the Build sequence sits in exactly one phase, and the phases lead toward the
  Vision.
- The MVP fits inside the first phase and produces both hypotheses' signals; each hypothesis can be
  refuted.

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
- **Who**: <the customers or users who have it>
- **Problem**: <what goes wrong for them, how often, what it costs>
- **Today**: <how they cope now, and why that falls short>

## The wedge
<the edge over the alternatives: what the project does that they can't or won't, and why that lets
it break into the market>

## Build sequence

### Phase 1 — <name>
- **Goal**: <what the phase achieves>
- **Features**: <feature>, <feature>

### Phase 2 — <name>
...

## Hypotheses

### Value hypothesis
- **Hypothesis**: <the falsifiable assumption>
- **Signal**: <the behaviour and threshold that confirm it; below the threshold it is refuted>

### Growth hypothesis
- **Hypothesis**: <how new customers find the product; its engine of growth>
- **Signal**: <the behaviour and threshold that confirm it; below the threshold it is refuted>

## MVP
- **Features**: <features, all from Phase 1>
- **Tests**: value hypothesis — <how the MVP produces its signal>; growth hypothesis — <how>

## Open questions
- **Q1 — <component>**: <the question> — <the options discussed and your recommendation, if any>
<or: None.>
````
