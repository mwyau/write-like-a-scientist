# Repository instructions

This repository contains one reusable writing skill. Keep it small enough to load routinely and keep conditional material out of the core context.

## Structure

- `skills/write-like-a-scientist/SKILL.md` contains the general writing rules and routes optional references.
- `skills/write-like-a-scientist/profiles/` describes the kind of text being written.
- `skills/write-like-a-scientist/domains/` contains field-specific terminology and writing conventions.
- `skills/write-like-a-scientist/LICENSE.txt` travels with the standalone skill directory.
- Project-specific facts, APIs, numerical settings, and local terminology belong in the project that uses the skill, not here.

Do not split profiles or domains into separate skills. The intended interface is one `write-like-a-scientist` skill that reads only the references needed for the current task.

## Editing the skill

This is the author's writing definition. Do not merge in generic academic-writing, humanizer, marketing-copy, or style-guide rules unless explicitly requested.

When adding guidance:

- Prefer a recurring writing principle over a long list of banned words.
- Treat warning words as context dependent. Keep them when they are the precise scientific or technical term.
- Keep examples generic when possible. Do not make a personal project, repository, package, paper, or version-specific implementation part of the reusable house style.
- Keep the core rules general. Move guidance that applies only to one writing context into a profile and guidance that applies only to one field into a domain.
- Do not turn a domain file into a textbook or glossary. Include terminology only when it changes how an agent should write.
- Keep the bundled license notice when copying or publishing the standalone skill directory.
- Do not add project-management machinery, installers, tests, or CI unless the repository develops a real need for them.

## Writing

The repository should follow its own skill. Use plain, direct English. Prefer a short common word when it says the same thing, but keep established scientific and technical terms. Do not make the documentation sound formal merely to sound polished.

## Git

Keep changes small and linear. Do not commit or push unless explicitly requested.
