# Atmospheric science

Load this domain for atmospheric science, meteorology, climate dynamics/modeling, cyclone and storm-track research, atmospheric spherical harmonics, and closely related climate-ML work.

Apply the core `write-like-a-scientist` rules first. Use project-local terminology when it is more specific.

## Use atmospheric terms, not generic substitutes

Keep established quantities and methods when they are what the work actually uses. Examples include:

- relative vorticity and divergence;
- streamfunction and velocity potential;
- geopotential and geopotential height;
- potential vorticity;
- eddy kinetic energy;
- storm-track activity and storm-track variability;
- weather impacts;
- reanalysis and observations;
- climate model or GCM;
- ensemble member;
- anomaly and climatology;
- spherical harmonic transform (SHT);
- spectral and triangular truncation;
- cyclic longitude;
- Eulerian and Lagrangian descriptions when that distinction is scientifically material.

Do not replace a standard atmospheric term with generic software, ML, or statistical wording merely to avoid repetition.

Name the actual atmospheric quantity when it is known: temperature, precipitation, pressure, wind, geopotential height, vorticity, or another field is usually more informative than `feature`, `signal`, `channel`, or `component` in scientific prose. Those generic terms remain appropriate when they refer to real model features, channels, or mathematical components.

Prefer `climate model` or `GCM` to `simulator` in atmospheric prose unless simulation methodology itself is the subject.

## Preserve method names

Use the terminology of the method or literature actually being discussed. Do not replace an established analysis with a broader or mathematically related label because the broader term sounds more general.

For cyclone tracking, use the terminology of the named tracking method when reproducing or comparing it rather than inventing generic labels for method-specific quantities.

For statistical or machine-learning analyses, keep the name of the method actually fitted or evaluated. If a relationship to another method family matters, explain the relationship without renaming the method.

## Climate-model generalization

Name the actual comparison when possible: a climate model, ensemble member, reanalysis, observation set, predictor field, target field, region, or time period.

Use ML terms such as `domain adaptation` or `domain generalization` when naming the actual ML method or literature. Do not let the abstraction replace the atmospheric description of the data being compared.

## Interpretation

Keep distinct:

- predictive skill;
- attribution or saliency;
- probe/decodability results;
- representation similarity;
- intervention, perturbation, or removal tests.

Do not turn predictive association or a diagnostic into a physical or mechanistic causal claim without the evidence needed for that claim.

## Numerical and coordinate wording

State sign, radius, normalization, coordinate, latitude-order, longitude, spectral-range, and zero-mode conventions when they are needed to interpret a result. Do not hide them behind phrases such as `standard convention` when multiple atmospheric conventions exist.

When comparing implementations, identify the implementation or reference method precisely enough that the comparison is reproducible. A reference implementation is not automatically scientific ground truth.
