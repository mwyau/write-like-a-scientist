# Physical oceanography

Load this domain for physical oceanography, ocean and coastal waves, sea level, tides, circulation, rotating/stratified fluids, and related geophysical-fluid problems.

Apply the core `write-like-a-scientist` rules first. Use project-local notation and terminology when it is more specific.

## Keep the physical terms

Use the quantity or process that the analysis actually describes. Examples include:

- sea level and sea-level anomaly;
- tide or tidal signal;
- current and velocity;
- seiche;
- surface, internal, barotropic, and baroclinic modes/waves when those distinctions apply;
- rotation and stratification;
- frequency and wavenumber;
- phase velocity and group velocity;
- equivalent depth;
- boundary and matching conditions;
- mode and eigenvalue;
- limiting case and asymptotic behavior;
- pressure, density, and free-surface displacement with their stated conventions.

Do not replace these with generic phrases such as `ocean signal`, `feature`, `component`, or `framework` when the physical quantity is known.

## Make conventions explicit when they matter

Ocean-wave and coastal calculations often depend on sign and coordinate choices. State the relevant convention rather than implying that there is only one standard choice:

- coordinate orientation;
- Fourier/sign convention;
- positive frequency or wavenumber convention;
- phase and propagation direction;
- vertical coordinate;
- rotation and stratification parameters;
- boundary condition;
- mode normalization.

Keep equations and nearby prose consistent with the same symbols and conventions.

## Separate source reproduction from scientific interpretation

When reconstructing or checking older physical-oceanography material, preserve the source wording, notation, equations, and figure labels unless the task explicitly authorizes an editorial or scientific correction.

A transcription statement answers what the source says. A scientific check answers whether the mathematics or physics is consistent. Do not silently reconcile those two questions.

If an earlier source, code path, and modern analysis differ, name them separately rather than rewriting the earlier method into modern terminology.

Use `historical` when the work actually concerns historical evidence or reproduction. Otherwise prefer the specific source, date, version, or `earlier` when that is what is meant.

## Data limitations

Do not invent units, time zones, station metadata, calibration, forcing, or physical amplitudes that the source data do not establish. State what is unknown and keep diagnostic quantities separate from physically interpreted quantities until the required metadata are known.

## Evidence and physical claims

Keep separate:

- a reproduced source calculation;
- an independently checked equation;
- an observed spectral or modal feature;
- a fitted model result;
- a dynamical interpretation;
- a causal or forcing claim.

A spectral peak, CEOF mode, phase relationship, or spatial pattern does not by itself prove a dynamical mechanism. Match the strength of the wording to the physical evidence.
