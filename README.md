# Write Like a Scientist

I got annoyed by agents constantly writing things like “historically,” “intentionally,” “deliberately,” “retained,” and “lineage.” This is my skill for making them write more like a scientist.

These are my writing rules, not a general academic-writing or “humanizer” guide.

## Structure

There is one skill:

```text
skills/write-like-a-scientist/
├── SKILL.md
├── LICENSE.txt
├── agents/
│   └── openai.yaml
└── references/
    ├── profile-linkedin-post.md
    ├── profile-research-software.md
    ├── domain-atmospheric-science.md
    └── domain-physical-oceanography.md
```

`SKILL.md` contains the rules that apply broadly. It loads a profile or domain reference only when the task needs it.

- A **profile** describes what is being written. `profile-research-software.md` covers README text, documentation, docstrings, comments, plans, and other research-software writing. `profile-linkedin-post.md` covers LinkedIn posts about scientific and technical work.
- A **domain** supplies field-specific terminology and writing conventions. The first two are atmospheric science and physical oceanography.

A scientific-software documentation task may use the core skill, the research-software profile, and one domain. A LinkedIn post may use the core skill, the LinkedIn profile, and a relevant domain. A general scientific explanation may need only the core skill. Unused files should stay out of context.

More profiles can be added later, for example `profile-scientific-paper.md`, without creating another skill.

`agents/openai.yaml` adds OpenAI-specific interface metadata. The skill itself remains based on `SKILL.md` and the Agent Skills directory format.

## Reuse

Copy or symlink the complete skill directory into a repository's skill location:

```bash
ln -s /path/to/write-like-a-scientist/skills/write-like-a-scientist \
  ./skills/write-like-a-scientist
```

A repository can then route writing tasks to `skills/write-like-a-scientist/SKILL.md`. Project-specific terminology and scientific rules remain in that repository and take precedence over the generic domain guidance.

The examples are warnings, not a word blacklist. `historical`, `intentionally`, `pipeline`, or `robust` can be the right word when they carry real scientific or technical meaning. The problem is using them as filler, narration, or decoration.

## License

MIT
