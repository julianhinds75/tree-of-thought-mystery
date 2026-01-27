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
