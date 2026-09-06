# Atmospheric science

Load this domain for atmospheric science, meteorology, climate dynamics/modeling, cyclone and storm-track research, atmospheric spherical harmonics, and closely related climate-ML work.

Apply the core `write-like-a-scientist` rules first. Use project-local terminology when it is more specific.

## Use atmospheric terms, not generic substitutes

Keep established quantities and methods when they are what the work actually uses. Examples include:

- relative vorticity and divergence;
- streamfunction and velocity potential;
- geopotential height;
- storm-track activity and storm-track variability;
- weather impacts;
- reanalysis and observations;
- climate model or GCM;
- ensemble member;
- anomaly and climatology;
- spherical harmonic transform (SHT);
- spectral and triangular truncation;
- Gauss–Legendre (GL) and Clenshaw–Curtis (CC) grids;
- cyclic longitude;
- Eulerian and Lagrangian descriptions when that distinction is scientifically material.

Do not replace a standard atmospheric term with generic software, ML, or statistical wording merely to avoid repetition.

Prefer `climate model` or `GCM` to `simulator` in atmospheric prose unless simulation methodology itself is the subject.

## Preserve method names

When applicable to the Yau/Chang storm-track work, preserve:

- **Eulerian storm-track metrics/statistics** for gridded synoptic-eddy quantities such as EKE;
- **Lagrangian cyclone-track statistics** for quantities derived from tracked cyclones;
- **storm-track activity** and **storm-track variability**;
- **weather impacts** for associated precipitation and high-wind quantities;
- **EOF + MLR** when that is the fitted linear method;
- **CCA coupled patterns** and **canonical variates** for CCA results.

Do not call EOF + MLR or CCA `reduced-rank regression` unless reduced-rank regression is separately fitted and evaluated.

For cyclone tracking, use the terminology of the named tracking method when reproducing or comparing it. For Hodges/TRACK work, terms such as `objects`, `feature points`, `trajectories`, and the named adaptive constraints are preferable to invented generic labels when they refer to those specific concepts.

## Climate-model generalization

When these are the actual questions, prefer specific phrases such as:

- predictor climate fields;
- target anomaly field;
- cross-climate-model generalization;
- climate-model-to-observation generalization;
- held-out GCM or ensemble member.

Use ML terms such as `domain adaptation` or `domain generalization` when naming the actual ML method or literature. Do not let the abstraction replace the atmospheric description of which GCM, reanalysis, observation set, predictor field, or target field is being compared.

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

When comparing implementations, name the implementation and version or reference method. NCL, SPHEREPACK, TRACK, pyspharm, or another package can be a parity/reference implementation without being scientific ground truth.
