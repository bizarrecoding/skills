# Agent instructions

This repo is a collection of agent skills. See [README.md](README.md) for the layout and how to add a skill.

## Skills

Each skill is a folder in `skills/<name>/` with a `SKILL.md` (YAML frontmatter with `name` and `description`, then markdown instructions) and optional reference files next to it.

If your tool supports skills natively, it will pick them up. If not, read the `description` in each `SKILL.md` and, when the user's request matches, read that file in full and follow it.

| Skill | Use when |
|-------|----------|
| [dev-interview](skills/dev-interview/SKILL.md) | The user wants a mock developer interview, interview practice, or hints on how to answer an interview question. |

Files linked from a `SKILL.md` (such as `HINT-LEVELS.md`) are loaded only when the skill says to.

## Editing

- Edit skills only in `skills/`. `.claude/skills` is a symlink to it.
- Keep the table above in sync when adding or removing a skill.
- Start new skills from `template/SKILL.md`.
