# Research software

Load this profile for README text, documentation, API descriptions, examples, comments, docstrings, design/plan documents, and software-paper text about research software.

Apply the core `write-like-a-scientist` rules first.

## Write for the researcher or user

Published documentation should read as scientific or technical documentation, not as instructions to an agent, a design review, a project-management brief, or a record of implementation decisions.

Start with what the software does, the scientific operation, the API, or the behavior the user needs.

Keep README text easy to scan. Put detailed methods and reference material in the appropriate documentation rather than turning the README into an architecture document.

## Describe current behavior directly

Prefer positive statements of supported behavior:

> The package supports global rectangular grids.

Mention unsupported behavior when it prevents a likely mistake or defines an important scientific boundary. Do not enumerate absent features merely to make the scope sound controlled.

Avoid phrases such as:

- `the initial package`;
- `the current phase`;
- `the API is designed to`;
- `this was intentionally kept small`;
- `accepted evolution`;
- `future architecture`.

Plans belong in plans. User documentation describes the software the user has.

## Name the API instead of narrating its organization

Use function, class, module, accessor, command, or file names when those are the useful facts.

Prefer:

> Operations are available through the accessor and as functions.

Do not add a paragraph explaining that one interface is primary, another is equivalent, both share a numerical path, or an accessor is thin unless that fact matters to use or interpretation.

Avoid meta-API terms such as `surface`, `promotion`, `importability`, or `compatibility surface` when ordinary API language works.

## Keep software abstractions tied to real objects

Terms such as `pipeline`, `framework`, `architecture`, `backend`, `protocol`, `layer`, and `hierarchy` are useful when they name a real software concept. Do not use them merely to make an implementation description sound systematic.

Prefer, when accurate:

- `data preparation` to `pipeline`;
- `training sequence` to `pipeline`;
- `analysis` or `check` to `audit`;
- `method` or the exact method name to `framework`;
- `implementation` to `execution layer`.

## Comments and docstrings

Comments should explain non-obvious current reasoning:

- numerical or scientific conventions;
- coordinate or sign conventions;
- units and normalization;
- constraints that are easy to violate;
- why an implementation step is required for the method.

Do not restate the code, preserve migration history, or explain obvious implementation structure.

Docstrings should state what an operation computes and the inputs, outputs, units, coordinates, assumptions, errors, or conventions a user needs. Do not fill them with architecture commentary.

## Scientific software claims

Distinguish:

- a formula from the literature;
- behavior copied or compared from another implementation;
- an analytic or numerical test;
- parity against an identified implementation;
- a benchmark;
- an external scientific validation.

`Tests pass` does not mean `scientifically validated`. A parity test does not make the comparison implementation scientific ground truth.

State the comparison and evidence for claims about parity, accuracy, speed, scalability, robustness, or correctness.

## Methods and references

Keep the exact scientific method name. Do not replace a cited method with an approximation while retaining the name.

When a software dependency supplies numerical machinery for a scientific operation, say so directly rather than implying that a wrapper implements the underlying numerical method itself.

Verify literature-derived formulas and terminology against primary scientific sources when practical. Verify bibliographic details against a publisher or another authoritative record.

## Plans and maintainer documents

Agent instructions and operational plans may use imperative language, repository paths, status markers, ownership/routing rules, and implementation vocabulary when those are genuinely useful. Do not copy that register into researcher-facing documentation.

A plan should still avoid filler and inflated wording. State the task, scientific constraint, evidence gate, or implementation step directly.

## Examples

Avoid:

> The accessor is the primary interface; each operation has an equivalent direct function.

Prefer:

> Operations are available through the accessor and as functions.

Avoid:

> The initial scope is deliberately limited to the supported grid types and does not reinterpret other grids.

Prefer, when sufficient:

> The package supports the listed grid types.

Add a restriction separately only where a user could otherwise supply invalid input.

Avoid:

> The package provides a robust, modern framework for high-performance scientific analysis.

Prefer naming the operations, data model, and measured performance that matter.
