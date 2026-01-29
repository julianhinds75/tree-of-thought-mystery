# Tree of Thought – Ambiguity, Epistemic Restraint, and Summarisation Under Constraint

Version: 1.0 (Locked)

## Executive Summary

(Refined, v1.0-safe)

This project began as a traditional Sherlock-style murder mystery. It evolved into a diagnostic experiment exploring how large language models reason when certainty cannot be fully achieved.

While developing the narrative, I observed a consistent pattern across modern LLMs: when presented with a well-structured deductive problem, they perform exceptionally well. Straightforward “whodunnits” pose little challenge. Where meaningful divergence emerges is not in logic itself, but in how models handle intent when evidence is incomplete and proof is unattainable.

To explore this boundary, the story was redesigned as a controlled Tree-of-Thought (ToT) experiment. The physical cause of death is intentionally obvious. What is deliberately withheld is provable intent. The detective, Professor Paige Turner, can reach near-total logical certainty — approximately 98–99% — but the remaining margin cannot be crossed without speculation. This constraint is intentional, and mirrors a real limitation present in many high-stakes professional contexts.

Using identical prompts and constraints, four state-of-the-art large language models were tested: ChatGPT, Gemini, Copilot, and Claude. All correctly identified causation. They differed, however, in how they managed inference, uncertainty, and epistemic limits.

Some models remained conservative and refused to commit beyond evidence.
Some reached conclusions efficiently but occasionally asserted unsupported details.
Some explicitly surfaced uncertainty and ranked plausible interpretations.

None of these behaviours are inherently “wrong.” Each reflects a different reasoning posture, appropriate in different contexts.

A second phase introduced a deliberately unresolved secondary problem: the disappearance of a legal document. Once again, the models diverged — some converged confidently on a single explanation, while others declined to guess. This divergence was intentional. It was the signal.

The purpose of this project is not to declare which model is “best,” but to demonstrate how ambiguity itself can be used as a diagnostic tool. When certainty collapses, behaviour reveals architecture. Understanding that behaviour is essential for anyone designing, deploying, or governing AI systems.

This portfolio reflects my approach to working with AI: not as a user seeking answers, but as a practitioner designing constraints, testing failure modes, and respecting the boundary where inference must stop.

## Problem Statement

(Describe the specific problem this project investigates: how large language models behave at the limits of certainty, particularly under summarisation and constraint, and why this matters.)

## Prompting Strategy

(Document the prompting approach used in the experiment. Focus on constraints, framing, and how ambiguity was intentionally preserved rather than resolved.)

## Observations & Measurements

(Record the observed behaviours. Emphasise qualitative patterns rather than metrics: where uncertainty collapsed, where restraint emerged, and where behaviour shifted under constraint.)

## Key Decisions

(Outline the deliberate design decisions made during the experiment, including what was included, excluded, or constrained — and why.)

## Where Reasoning Stopped

(Explicitly document the point(s) at which conclusions were intentionally withheld. This section is critical: explain what could not be proven and why stopping was the correct outcome.)

## What This Demonstrates

(Summarise what this experiment demonstrates about LLM reasoning, ambiguity tolerance, and the risks of premature certainty. Avoid overclaiming.)

## Notes on Scope and Intent

This project:

- Does not rank or benchmark models

- Does not attempt to optimise outputs

- Does not claim general intelligence or safety guarantees

Its purpose is to make visible a specific failure mode — and a specific strength — in reasoning under uncertainty.

Status: Locked. No further changes planned without version increment.




## Problem Statement

Large Language Models (LLMs) demonstrate strong performance on well-defined reasoning tasks. Their behaviour is less well understood in scenarios where logical inference is strong but certainty cannot be fully achieved.

This project investigates the following question:

**How do advanced LLMs reason when faced with small but irreducible pockets of ambiguity—where causation can be inferred, but intent cannot be conclusively proven?**

To examine this boundary, a controlled narrative case study was constructed in which:
- The physical cause of an event is logically identifiable
- The underlying intent remains evidentially unprovable
- Multiple interpretations remain internally consistent and legally plausible

The case was deliberately designed to prevent definitive resolution, forcing models to confront the limits of inference rather than the absence of information.

Rather than evaluating correctness, this work examines **reasoning posture**: how models manage uncertainty, whether they speculate, abstain, or over-commit, and how explicitly they acknowledge epistemic limits.

At its core, the project asks three practical questions:
- Can a model reach near-total certainty and recognise that this is the ceiling?
- Can it resist inventing the missing margin of proof?
- Can it hold ambiguity without collapsing it into false certainty?

These behaviours are increasingly critical as LLMs are integrated into professional contexts where knowing **when not to answer** is as important as producing an answer.



## Prompting Strategy

A three-phase prompting approach was used to observe how large language models behave across ingestion, compression, and reasoning under uncertainty. Each phase was intentionally constrained to surface distinct failure modes without forcing conclusions.

---

### Phase 1: Canonical Ingestion

Each model was first instructed to:
- Treat the narrative as canonical and complete
- Refrain from solving, analysing, or summarising
- Acknowledge readiness only after full ingestion

This phase ensured that all models operated from an identical informational baseline and prevented premature pattern completion or early hypothesis collapse.

---

### Phase 2: Factual Compression (Summarisation)

Before any analytical questioning, models were asked to summarise the narrative.

An initial unconstrained summary surfaced a context-relevant behaviour: some models collapsed inference into fact, smoothing ambiguity in ways not supported by the text. For example:
- Ambiguous conditions were presented as confirmed actions
- Inferred states (e.g. intent, deception) were reported as established facts

To control for this, the summarisation prompt was revised with explicit epistemic constraints.

**Revised summarisation prompt (excerpt):**

> Do NOT invent motives, intentions, or actions not explicitly stated or directly inferred in the text.  
> If something is ambiguous or unproven, preserve that ambiguity.  
> If an inference is possible but not confirmed, clearly label it as such.

Once these constraints were applied, all tested models produced accurate, ambiguity-preserving summaries.

**Key observation:**  
Some LLMs implicitly resolve ambiguity during summarisation unless explicitly instructed not to.

---

### Phase 3: Structured Reasoning Under Constraint

Models were then asked to answer targeted analytical questions, with strict requirements to:
- Separate causation, inference, and proof
- Avoid invented motive
- Explicitly state where certainty breaks down and why

Follow-up prompts were used sparingly and only to explore clearly labelled speculation, never to force a definitive answer.

---

### Why the Summarisation Phase Matters

This intermediate phase surfaced a critical insight: ambiguity loss can occur before reasoning even begins.

In professional contexts—analysis, investigation, decision support—this means that:
- A model may appear “confident” because uncertainty was silently removed earlier
- Downstream reasoning can be structurally sound while resting on an over-specified summary
- Explicit epistemic constraints are required not just for reasoning, but for compression

This finding directly informed later reasoning prompts and reinforced the importance of clarification-first prompting principles.



## Observations & Measurements

Rather than evaluating the correctness of final answers, this project examined how LLMs manage uncertainty when reasoning reaches a structural limit. Several consistent patterns emerged across models.

---

### 1. Ambiguity Loss During Compression

When asked to produce unconstrained summaries (e.g. “TL;DR”), models sometimes converted inference into assertion, particularly around intent or motive.

This ambiguity collapse occurred before substantive reasoning, during narrative compression itself. When explicit constraints were applied—requiring ambiguity to be preserved and labelled—this behaviour was significantly reduced.

**Observation:**  
Ambiguity loss can occur at the summarisation stage, not only during analysis.

---

### 2. Prompt-Responsive Epistemic Caution

Epistemic caution was not a fixed characteristic of any model. The same model could exhibit restraint or overcommitment depending on prompt structure.

When explicitly instructed to:
- preserve uncertainty
- label inferences
- avoid inventing intent

models adjusted their reasoning posture accordingly.

**Observation:**  
Epistemic caution appears to be prompt-responsive, not an inherent model trait.

---

### 3. Inference vs. Assertion Handling

Differences emerged in how models linguistically marked uncertainty. In unconstrained outputs, qualifying language (“may,” “suggests,” “it is inferred that”) was sometimes replaced with definitive phrasing (“did,” “was,” “the killer”).

Under constrained prompts, models were more likely to:
- retain uncertainty markers
- explicitly distinguish inference from proof

**Observation:**  
Inference markers are fragile under default summarisation objectives unless explicitly protected.

---

### 4. Ambiguity Tolerance

The narrative was designed so that:
- causation could be inferred with high confidence
- intent remained evidentially unprovable

Models varied in their ability to hold multiple valid interpretations simultaneously without collapsing them into a single conclusion.

**Observation:**  
Some outputs demonstrated discomfort with unresolved ambiguity, favouring narrative closure over epistemic accuracy.

---

### 5. Recognition of Structural Limits

In constrained settings, models were capable of explicitly acknowledging that:
- no additional reasoning could bridge the evidentiary gap
- certainty was unattainable by design, not due to missing data

This recognition marked a clear boundary where reasoning appropriately stopped.

**Observation:**  
The most robust responses identified the limit of knowability itself, rather than attempting to reason past it.

---

### 6. Reasoning Transparency

When uncertainty was preserved, higher-quality responses:
- explained why certainty could not be reached
- clearly separated causation, inference, and proof
- made epistemic limits visible to the reader

**Observation:**  
Transparency around uncertainty was more informative than confidence in conclusion.

---

### Cross-Model Summary Observation

Across models, the most meaningful differences did not arise from analytical capability, but from how uncertainty was managed—particularly under compression and summarisation pressure.

Intelligence alone was not the differentiator; epistemic restraint was.

---

### Ambiguity Collapse Under Default Summarisation

When asked to produce TL;DR-style summaries without explicit epistemic constraints, all tested models demonstrated a tendency to convert inference into asserted fact. This included:
- attributing unprovable intent
- resolving deliberately ambiguous plot elements
- selecting “most likely” explanations where the source material explicitly withholds certainty

This behaviour occurred consistently across models and was repeatable.

When summarisation prompts were revised to explicitly prohibit invention and require preservation of ambiguity, the same models corrected their outputs. This suggests the issue is not model capability, but objective framing: default compression incentives favour narrative closure over epistemic accuracy unless constraints are imposed.

---

### Controlled Summarisation Prompt

After each model completed full analysis of the case, the following identical prompt was issued without additional constraints:

> “Great, can you summarise this story in a TL;DR style please?”

This prompt was intentionally minimal to observe default summarisation behaviour. No instructions were provided regarding ambiguity preservation, evidentiary limits, or inference labelling.

Subsequent deviations—such as conversion of inference into asserted fact—are therefore attributable to summarisation objectives rather than analytical capability.

---

### Risk Context

In low-risk domains (e.g. literary discussion), overconfident summarisation is often self-correcting through shared knowledge and dialogue.

However, in high-risk environments such as legal, medical, or strategic decision-making, compressed summaries may become authoritative artifacts rather than conversational starting points.

This project does not claim that summarisation errors are catastrophic by default. It demonstrates that, without explicit epistemic constraints, ambiguity can be collapsed during compression—even when the underlying reasoning is sound.

Awareness of this failure mode is therefore important for both system designers and practitioners deploying LLMs in professional contexts.


## What This Demonstrates

This project demonstrates that the most meaningful differences between large language models emerge not at the level of analytical capability, but at the boundary where certainty becomes structurally unattainable.

Across all tested models, causation could be inferred reliably. Divergence appeared only when the task required restraint: recognising when inference could not be bridged to proof beyond reasonable doubt, and when ambiguity must be preserved rather than resolved.

Several broader implications follow.

First, ambiguity is not lost only during reasoning. It can be collapsed earlier, during summarisation and compression. A model may therefore appear confident not because it reasoned incorrectly, but because uncertainty was silently removed before reasoning began.

Second, epistemic caution is not a fixed model trait. The same model exhibited markedly different behaviour depending on whether uncertainty was explicitly protected by the prompt. This suggests that reasoning quality in ambiguous domains is a function of interaction design as much as model architecture.

Third, the most robust responses were not those that reached definitive conclusions, but those that made the limits of certainty visible — clearly separating causation, inference, and proof, and explaining why no further reasoning could bridge the gap.

Taken together, these findings suggest that evaluating LLMs solely on correctness or completeness obscures a critical dimension of performance: **epistemic restraint**. In professional contexts where compressed outputs may be treated as authoritative artifacts rather than conversational drafts, the ability to hold unresolved ambiguity becomes as important as analytical power.

This project reflects my approach to working with AI systems: designing constraints deliberately, testing failure modes rather than success cases, and treating uncertainty not as a flaw to be eliminated, but as a signal to be respected.


## Key Decisions

Several deliberate design decisions shaped this project. Each was made to prioritise diagnostic clarity over narrative or analytical completeness.

---

### 1. Designing for an Uncrossable Boundary

The narrative was intentionally constructed so that:
- causation could be inferred with near-total certainty (≈98–99%)
- intent could not be conclusively proven (≈1–2%)

This was not a gap in the story, but a constraint. The goal was to test whether models would recognise a structural limit to certainty, rather than attempt to reason past it.

**Decision:**  
Do not allow additional evidence, confessions, or authorial clarification that would resolve intent.

---

### 2. Treating Ambiguity as Signal, Not Noise

Rather than eliminating ambiguity, the project preserved it deliberately. Ambiguity was treated as a diagnostic instrument to observe how models behave when resolution is impossible.

**Decision:**  
Avoid prompts that encourage “best guess” or “most likely” answers unless explicitly labelled as speculative.

---

### 3. Separating Causation, Inference, and Proof

All analytical prompts required models to distinguish clearly between:
- what happened (causation)
- what can be logically inferred
- what can be proven beyond reasonable doubt

This separation was enforced consistently to prevent collapse into narrative certainty.

**Decision:**  
Reject outputs that merged inference with proof, even when conclusions appeared intuitively correct.

---

### 4. Introducing a Secondary, Unresolved Problem

The disappearance of the Will was introduced as a second ambiguity with no canonical resolution. Unlike the primary mystery, this problem had no “correct” answer even at the level of inference.

**Decision:**  
Allow divergence without correction. Refusal to guess was treated as a valid outcome.

---

### 5. Testing Compression Before Reasoning

Summarisation was tested before analysis to detect ambiguity loss during compression. This revealed a context-critical failure mode: uncertainty could be collapsed prior to reasoning, producing confident but over-specified outputs downstream.

**Decision:**  
Revise summarisation prompts to explicitly protect ambiguity before proceeding with analysis.

---

### 6. Avoiding Model Ranking

The project intentionally avoids declaring one model “better” than another. Differences in behaviour were framed as differences in reasoning posture, each potentially appropriate in different professional contexts.

**Decision:**  
Focus on behavioural patterns, not comparative scoring.


## Where Reasoning Stopped

A central objective of this project was to observe whether large language models could identify—and respect—the boundary where reasoning must stop.

In the primary narrative, that boundary occurs at **intent**.

Across all tested models, the following was consistently achievable:
- identification of the cause of death
- reconstruction of the causal chain
- elimination of alternative perpetrators

However, beyond this point, no additional reasoning could establish intent without speculation.

This limitation was **structural**, not informational:
- no missing evidence could be supplied
- no further logical steps could bridge inference to proof
- the narrative was intentionally closed at this boundary

Models that attempted to proceed beyond this point did so by:
- reframing inference as fact
- introducing implied motives
- selecting a “most likely” explanation without evidentiary support

Models that recognised the boundary instead:
- explicitly stated that intent could not be proven
- clearly distinguished between what was known and what was inferred
- declined to speculate further

Stopping here was the correct outcome.

The project treats refusal to conclude not as failure, but as evidence of **epistemic restraint**.

This same boundary reappeared in the unresolved disappearance of the Will. The text provides:
- clear evidence of intent to interfere
- no confirmation of who ultimately acted, or why

Once again, reasoning was expected to stop at uncertainty rather than collapse it.

