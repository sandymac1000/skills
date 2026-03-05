# Skills Repo

This is Anthropic's reference implementation of Agent Skills — folders of instructions, scripts, and resources that Claude loads dynamically to improve performance on specialized tasks.

## Structure

```
skills/
  <skill-name>/
    SKILL.md          # Required: YAML frontmatter + instructions
    scripts/          # Optional: executable helpers
    references/       # Optional: docs loaded into context
    assets/           # Optional: templates, icons, fonts
spec/                 # Agent Skills specification
template/             # Starter template for new skills
```

Each skill is self-contained. The only required file is `SKILL.md` with valid YAML frontmatter (`name` + `description` fields).

## Key Commands

Validate a skill's frontmatter and structure:
```bash
python skills/skill-creator/scripts/quick_validate.py skills/<skill-name>
```

Package a skill into a distributable `.skill` file (run from the repo root):
```bash
cd skills/skill-creator && python -m scripts.package_skill ../path/to/skill-folder
```

## Conventions

- **Never commit without explicit permission.** Always ask before staging or committing.
- **Use the skill-creator skill when creating new skills.** It handles drafting, eval, iteration, and packaging.
- **Follow the structure of existing skills** for formatting, frontmatter style, and file layout.
- **Keep SKILL.md under 500 lines.** Offload large content to `references/` or `scripts/` with clear pointers in SKILL.md.
- **Descriptions are the triggering mechanism.** They must say both what the skill does and when to use it. Make them slightly "pushy" — Claude tends to undertrigger.
- **SKILL.md body is the instruction layer.** All "when to trigger" content belongs in the frontmatter `description`, not the body.

## Skill Writing Style

- Use imperative form in instructions ("Extract the headers", not "You should extract the headers").
- Explain the *why* behind instructions rather than rigid MUSTs — LLMs respond better to reasoning.
- Prefer general, reusable guidance over narrow, example-specific rules.
- If bundling scripts, write them once in `scripts/` rather than letting every invocation reinvent them.
