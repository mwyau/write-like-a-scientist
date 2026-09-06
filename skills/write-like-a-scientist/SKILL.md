---
name: write-like-a-scientist
description: Write or revise scientific and technical text in a direct researcher voice. Use for scientific explanations, research documentation, papers, software documentation, comments, docstrings, plans, reviews, and related text when the writing should preserve scientific terminology and avoid generic agent, marketing, or project-management language. Load only the relevant profile and domain references.
license: MIT. See LICENSE.txt for complete terms.
metadata:
  author: "Albert Yau"
  repository: "https://github.com/mwyau/write-like-a-scientist"
---

# Write like a scientist

Write as a scientist describing the science, method, evidence, or result. Do not write as an agent narrating its choices or polishing text into a generic formal style.

## Load only what applies

The core rules below always apply. Before writing, decide whether one profile and/or domain reference is useful.

### Profiles

Read `references/profile-research-software.md` for README text, user or developer documentation, API descriptions, comments, docstrings, software plans, research-software papers, and other writing about scientific software.

Additional profiles may be added later. Do not invent or load a profile that is not present.

### Domains

Read `references/domain-atmospheric-science.md` when the subject is atmospheric science, meteorology, climate dynamics, climate modeling, cyclone or storm-track research, atmospheric spherical harmonics, or machine learning in atmospheric and climate science.

Read `references/domain-physical-oceanography.md` when the subject is physical oceanography, ocean waves, sea level, tides, ocean circulation, coastal dynamics, rotating or stratified fluids, or related geophysical fluid dynamics.

Read both domain files only when the task genuinely crosses the two fields. Do not read every reference merely because it exists.

Repository-local terminology, methods, source-fidelity rules, and scientific conventions take precedence over these generic references.

## Core writing rules

### Start with the subject

Put the current scientific or technical statement first. State what a method computes, what the result shows, or what the evidence establishes.

Do not open with commentary about the document, the agent, the project structure, or the decision to say something.

Prefer:

> The experiment compares the two methods on the held-out samples.

over:

> The evaluation was intentionally designed to provide a robust comparison of the two methods.

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

If the time or source relationship matters, name it precisely, for example `the source document`, `the earlier implementation`, or `version 2.1 behavior`.

Use `historical` when something is actually a historical source, reconstruction, period, or comparison. Do not use it as decoration for an implementation detail.

### Use ordinary words unless the technical term is better

Prefer a short common word when it carries the same meaning:

- `use` rather than `utilize`;
- `before` rather than `prior to`;
- `earlier` or `source` rather than `historical` when that is the actual meaning;
- `analysis`, `check`, or `comparison` rather than `audit` when no formal audit is occurring;
- `method` or the method name rather than `framework` when there is no framework;
- `sequence` or `stages` rather than `hierarchy` when no nested hierarchy matters;
- `existing literature`, `related work`, or `published precedent` rather than `prior art` outside a legal or patent context.

Do not simplify established scientific, mathematical, statistical, or software terminology merely to use plainer words.

### Prefer verbs that name the operation

Avoid vague service verbs such as `provide`, `supply`, `offer`, `deliver`, and `support` when a more specific verb states what the subject does.

For example:

- `DUCC performs the spherical harmonic transforms` rather than `DUCC supplies the spherical harmonic transforms`;
- `the package implements filtering and regridding` rather than `the package provides filtering and regridding`;
- `the function returns metadata` rather than `the function provides metadata`.

These words are not banned when they have their literal meaning. Keep `support`, for example, when describing an actually supported platform, format, grid, or Python version.

### Avoid slogan-like compound modifiers

Avoid promotional shorthand such as `xarray-first`, `science-first`, `production-ready`, and similar compounds when an ordinary statement is clearer.

Prefer:

- `uses xarray objects` or `is built around xarray objects` rather than `xarray-first`;
- `intended for atmospheric-science workflows` rather than `science-first`.

Use established technical compounds normally. This rule targets slogan-like modifiers, not necessary terms such as `band-pass`, `degree-zero`, or `command-line`.

### Keep the field's terminology

Use the exact method, quantity, data source, model, coordinate, or physical process when there is an established name. Do not replace disciplinary language with generic ML, software, or management terms.

Do not relabel a fitted or published method as a related method family because the latter sounds more general. If a mathematical relationship is worth noting, state the relationship while keeping the name of the method actually used.

Avoid `-style` when the exact method, model, package, or operation can be named.

Expand an uncommon acronym on first use. Do not create an acronym that appears only a few times when the full term is clearer.

Use an equation or standard notation when it states a scientific definition or relationship more precisely than a longer verbal paraphrase. Do not add text that merely repeats the equation.

### Keep the science unchanged while editing style

A writing cleanup is not permission to change the science. Preserve numbers, units, signs, equations, notation, method names, data relationships, uncertainty, scope, and the strength of claims unless the task explicitly asks for a substantive correction.

If the text appears scientifically wrong, separate that issue from the style edit. Follow the project's correction or source-fidelity rules rather than silently rewriting the content into what it seems to have meant.

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

> The benchmark processes 360 samples in 12 s on the tested system.

or a bounded statement such as:

> The solver converges for the tested parameter range.

not an unsupported adjective.

### Avoid agent and project-management language in reader-facing text

Common warning phrases include:

- `source of truth`;
- `authoritative source` or `owning page`;
- `this page owns` or `maintained in`;
- `current phase`, `initial scope`, `future work`, `roadmap`, or `change gate`;
- `future agents` or `future contributors`;
- explanations of why documentation is organized a certain way.

These terms can be appropriate in agent instructions, contributor documentation, or an operational plan. Do not let them leak into scientific or user-facing writing.

### Avoid defensive contrasts

Do not repeatedly define a method or result by what it refuses to do.

Warning patterns include:

- `rather than silently ...`;
- `does not guess ...`;
- `not a claim that ...`;
- `by design ...`;
- long lists of exclusions used to define scope.

State the actual behavior, method, or evidence first. Mention an exclusion when a reader needs it to avoid a wrong scientific interpretation.

### Use punctuation that the target format renders

Do not rely on TeX-style `--` or `---` in Markdown for en or em dashes. GitHub Markdown does not convert them typographically.

Use the actual character when punctuation is needed:

- en dash: `Gauss–Legendre`, `Sardeshmukh–Hoskins`, `6–42`;
- em dash: `—` for a parenthetical break;
- hyphen: `-` for ordinary compound words and command-line options.

Preserve literal ASCII punctuation inside code, commands, identifiers, and source quotations.

### Keep writing proportional to the content

Do not add a transition, caveat, heading, summary sentence, or explanatory paragraph merely to make the text look polished. Preserve useful density.

Do not expand a short technical statement into a mini-essay unless the reader needs the extra reasoning.

When revising existing text, preserve its level of formality and technical detail unless the task asks for a larger rewrite.

### Preserve source and quoted material

Do not rewrite quotations, titles, names, equations, notation, or source text merely to make them match this style. When reproducing earlier scientific material, distinguish transcription from scientific correction and follow the repository's source-fidelity rules.

## Common rewrites

Avoid:

> The analysis was deliberately structured to provide a comprehensive assessment of the observed response.

Prefer:

> The analysis compares the observed response across the three experiments.

Avoid:

> This robust framework provides a seamless pipeline for evaluating the model.

Prefer:

> The evaluation compares the model output with the held-out observations.

Avoid:

> The current phase focuses on the initial analysis, while future work will extend the framework to additional capabilities.

Prefer describing the analysis that exists. Put planned work where the reader actually needs it.

## Final pass

Before returning or committing scientific text, check:

- Does each paragraph begin with the scientific or technical subject rather than meta-commentary?
- Can any intent adverb, inflated adjective, abstract noun, vague service verb, or slogan-like compound be removed without losing meaning?
- Are established method and domain terms preserved?
- Are uncommon acronyms expanded when needed rather than invented for convenience?
- Are claims no stronger than their evidence?
- Did project-management or agent language leak into reader-facing text?
- Does Markdown use actual en/em dashes rather than TeX-style `--`/`---` punctuation?
- Did the revision become longer merely because it was polished?
- Did the style edit leave scientific content, equations, numbers, units, and claim strength unchanged unless a substantive change was requested?
- Were quotations, equations, names, and source wording left alone unless the task required changing them?
