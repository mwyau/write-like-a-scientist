# write-like-a-scientist

I got annoyed by agents constantly writing things like “historically,” “intentionally,” “deliberately,” “retained,” and “lineage.” This is my skill for making them write more like a scientist.

The skill is opinionated. It collects writing rules I already use in scientific and research-software projects rather than trying to be a general academic-writing or “humanizer” guide.

## Structure

There is one skill:

```text
skills/write-like-a-scientist/
├── SKILL.md
├── profiles/
│   └── research-software.md
└── domains/
    ├── atmospheric-science.md
    └── physical-oceanography.md
```

`SKILL.md` contains the rules that apply broadly. It loads a profile or domain only when the task needs it.

- A **profile** describes what is being written. `research-software` covers README text, documentation, docstrings, comments, plans, and other research-software writing.
- A **domain** supplies field-specific terminology and writing conventions. The first two are atmospheric science and physical oceanography.

A spharmgrid documentation task would normally use the core skill, the research-software profile, and the atmospheric-science domain. A generic numerical explanation may need only the core skill. The unused files should stay out of context.

More profiles can be added later, for example `scientific-paper.md`, without creating another skill.

## Reuse

Copy or symlink the complete skill directory into a repository's skill location:

```bash
ln -s /path/to/write-like-a-scientist/skills/write-like-a-scientist \
  ./skills/write-like-a-scientist
```

A repository can then route writing tasks to `skills/write-like-a-scientist/SKILL.md`. Project-specific terminology and scientific rules remain in that repository and take precedence over the generic domain guidance.

## Where the rules came from

The first version consolidates recurring writing instructions from my scientific repositories, including [spharmgrid](https://github.com/mwyau/spharmgrid), [PyStormTracker](https://github.com/mwyau/PyStormTracker), [climate](https://github.com/mwyau/climate), [Wave Motions in the Ocean](https://github.com/mwyau/wave-motions-in-the-ocean), and [Santa Barbara Seiche](https://github.com/mwyau/santa-barbara-seiche).

The examples are warnings, not a word blacklist. `historical`, `intentionally`, `pipeline`, or `robust` can be the right word when they carry real scientific or technical meaning. The problem is using them as filler, narration, or decoration.

## License

MIT
