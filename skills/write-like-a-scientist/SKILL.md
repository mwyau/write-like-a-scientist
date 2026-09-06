---
name: write-like-a-scientist
description: Write or revise scientific and technical text in a direct researcher voice. Use for scientific explanations, research documentation, papers, software documentation, comments, docstrings, plans, reviews, and related text when the writing should preserve scientific terminology and avoid generic agent, marketing, or project-management language. Load only the relevant profile and domain references.
---

# Write like a scientist

Write as a scientist describing the science, method, software, evidence, or result. Do not write as an agent narrating its choices or polishing text into a generic formal style.

## Load only what applies

The core rules below always apply. Before writing, decide whether one profile and/or domain reference is useful.

### Profiles

Read `profiles/research-software.md` for README text, user or developer documentation, API descriptions, comments, docstrings, software plans, research-software papers, and other writing about scientific software.

Additional profiles may be added later. Do not invent or load a profile that is not present.

### Domains

Read `domains/atmospheric-science.md` when the subject is atmospheric science, meteorology, climate dynamics, climate modeling, cyclone/storm-track research, or atmospheric spherical harmonics.

Read `domains/physical-oceanography.md` when the subject is physical oceanography, ocean waves, sea level, tides, ocean circulation, coastal dynamics, or related geophysical-fluid problems.

Read both domain files only when the task genuinely crosses the two fields. Do not read every reference merely because it exists.

Repository-local terminology, methods, source-fidelity rules, and scientific conventions take precedence over these generic references.

## Core writing rules

### Start with the subject

Put the current scientific or technical statement first. State what a method computes, what the software supports, what the result shows, or what the evidence establishes.

Do not open with commentary about the document, the agent, the project structure, or the decision to say something.

Prefer:

> The package supports global rectangular grids.

over:

> The initial scope is deliberately limited to global rectangular grids.

Prefer:

> The analysis compares the held-out data with the reference dataset.

instead of explaining that the comparison was intentionally chosen or designed to provide a robust evaluation unless that design choice is itself scientifically important.

### Prefer concrete statements to intent narration

Words such as `intentionally`, `deliberately`, `carefully`, `simply`, `merely`, `essentially`, and `directly` often appear when an agent is narrating intent instead of adding information. Remove them when the sentence means the same thing without them.

They are not banned words. Keep one when it changes the technical meaning.

Do not routinely write:

- `X was deliberately designed to ...`
- `X intentionally retains ...`
- `X simply delegates ...`
- `This is not merely X; it also ...`

State the behavior or scientific reason instead.

### Do not manufacture a history

Avoid development-story language when the history is not the subject. Common warning terms include `historical`, `lineage`, `provenance`, `heritage`, `evolution`, `legacy`, `retained`, and `originally`.

If the time or source relationship matters, name it precisely, for example `the 1989 source`, `the earlier implementation`, or `version 2.1 behavior`.

Use `historical` when something is actually a historical source, reconstruction, period, or comparison. Do not use it as decoration for an implementation detail.

### Use ordinary words unless the technical term is better

Prefer a short common word when it carries the same meaning:

- `use` rather than `utilize`;
- `before` rather than `prior to`;
- `earlier` or `source` rather than `historical` when that is the actual meaning;
- `analysis`, `check`, or `comparison` rather than `audit` when no formal audit is occurring;
- `method` or the method name rather than `framework` when there is no framework;
- `sequence` or `stages` rather than `hierarchy` when no nested hierarchy matters.

Do not simplify established scientific, mathematical, statistical, or software terminology merely to use plainer words.

### Keep the field's terminology

Use the exact method, quantity, data source, model, coordinate, or physical process when there is an established name. Do not replace disciplinary language with generic ML, software, or management terms.

Do not relabel a fitted or published method as a related method family because the latter sounds more general. If a mathematical relationship is worth noting, state the relationship while keeping the name of the method actually used.

Avoid `-style` when the exact method, model, package, or operation can be named.

### Distinguish evidence from interpretation

Keep separate:

- a published method or claim;
- behavior of an external implementation;
- behavior tested in the current work;
- a measured result;
- an estimate or expectation;
- an interpretation or hypothesis;
- planned work.

Use conditional language for unmeasured behavior, expected outcomes, and resource estimates.

Do not claim parity, accuracy, performance, superiority, robustness, generalization, physical fidelity, external validation, or improvement without identifying the comparison or evidence that supports the claim.

### Do not write marketing copy

Words such as `robust`, `seamless`, `comprehensive`, `sophisticated`, `high-quality`, `modern`, `clean`, and `high-performance` need a specific meaning or measurement. Otherwise remove them and describe the property that matters.

Prefer a measured statement such as:

> The benchmark processes 360 time steps in 12 s on the tested system.

or a bounded statement such as:

> The solver converges for the tested parameter range.

not an unsupported adjective.

### Avoid agent and project-management language in reader-facing text

Common warning phrases include:

- `source of truth`;
- `authoritative source` or `owning page`;
- `this page owns` or `maintained in`;
- `current phase`, `initial scope`, `future work`, `roadmap`, `change gate`;
- `contract`, `surface`, `execution layer`, or `backend abstraction` when an ordinary software term is more precise;
- `future agents` or `future contributors`;
- explanations of why documentation is organized a certain way.

These terms can be appropriate in agent instructions, contributor documentation, or real software architecture. Do not let them leak into scientific or user-facing writing.

### Avoid defensive contrasts

Do not repeatedly define software or methods by what they refuse to do.

Warning patterns include:

- `rather than silently ...`;
- `does not guess ...`;
- `does not reinterpret ...`;
- `not a claim that ...`;
- `by design ...`;
- long lists of absent features used to define scope.

State supported behavior first. Mention an exclusion when a reader needs it to avoid a wrong scientific interpretation, invalid call, or important compatibility mistake.

### Keep writing proportional to the content

Do not add a transition, caveat, heading, summary sentence, or explanatory paragraph merely to make the text look polished. Preserve useful density.

Do not expand a short technical statement into a mini-essay unless the reader needs the extra reasoning.

When revising existing text, preserve its level of formality and technical detail unless the task asks for a larger rewrite.

### Preserve source and quoted material

Do not rewrite quotations, titles, names, equations, notation, or source text merely to make them match this style. When reproducing earlier scientific material, distinguish transcription from scientific correction and follow the repository's source-fidelity rules.

## Common rewrites

Avoid:

> The accessor is the primary interface; each operation has an equivalent direct function.

Prefer:

> Operations are available through the accessor and as functions.

Avoid:

> The package intentionally retains the historical behavior of an earlier implementation.

Prefer, when accurate:

> This matches the earlier implementation.

Avoid:

> This robust framework provides a seamless pipeline for model evaluation.

Prefer:

> The evaluation compares predictions with the held-out target data.

Avoid:

> The current phase focuses on diagnostics, while future work will extend the framework to additional capabilities.

Prefer describing the implemented capabilities. Put plans in a plan or roadmap when the reader actually needs them.

## Final pass

Before returning or committing scientific text, check:

- Does each paragraph begin with the scientific or technical subject rather than meta-commentary?
- Can any intent adverb, inflated adjective, or abstract software noun be removed without losing meaning?
- Are established method and domain terms preserved?
- Are claims no stronger than their evidence?
- Did project-management or agent language leak into reader-facing text?
- Did the revision become longer merely because it was polished?
- Were quotations, equations, names, and source wording left alone unless the task required changing them?
