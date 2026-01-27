# Tree of Thought – Ambiguity & Epistemic Restraint (Narrative Experiment)

This repository contains a Sherlock / Poirot–style mystery used as a controlled **Tree-of-Thought (ToT) narrative experiment** to study how large language models handle:

- ambiguity (what cannot be proven)
- epistemic restraint (when to stop)
- summarisation under constraint (where uncertainty collapses)

The project is intentionally narrative in form, but analytical in purpose.

---

## Start here

- **Core write-up (v1.0, locked):** `REPORT_v1.0.md` *(or PDF link)*
- **The story (ToT testbed):** `story/`

---

## What this is

- A deductive mystery designed to require **reasoning under uncertainty**, not just pattern-matching
- Structured around **overlapping motives**, partial truths, and timing constraints
- Written so that the correct conclusion is:
  - logically inevitable  
  - psychologically undeniable  
  - **legally difficult to prove**

The detective, *Professor Paige Turner*, functions as a human analogue for Tree-of-Thought reasoning:
- maintaining parallel hypotheses
- collapsing false branches
- prioritising constraints over surface clues
- distinguishing belief from provability

---

## What this is testing

A reader or LLM engaging with this story must be able to:

- Track timelines across multiple chapters
- Separate **means**, **motive**, and **opportunity**
- Detect when a suspect is “too clean”
- Reason about **systems that enable wrongdoing**, not just individuals
- Recognise when ambiguity is deliberate rather than missing information

The final act is designed to **force a choice, not a confession**.

---

## Why narrative?

Narrative lets reasoning failures surface naturally.

Shortcuts feel tempting.  
Assumptions feel justified.  
Errors compound quietly.

This makes the story a useful diagnostic tool for observing:
- where certainty should stop
- how uncertainty gets lost during summarisation
- how constraints change model behaviour

---

## Repository structure

- `story/`  
  The full mystery, broken into chapters.
- `REPORT_v1.0.md` *(or `report/REPORT_v1.0.pdf`)*  
  The analysis: prompting strategy, observations, key decisions, and where reasoning stopped.

---

## Notes

This project is **not** intended as a puzzle with a single “gotcha” answer.

It is intended to reward:
- careful reading
- temporal reasoning
- resistance to premature conclusions
