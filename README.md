<img src="assets/icon.svg" width="64" height="64" alt="">

# skill-playground

My personal collection of agent skills. Each skill is a folder with a `SKILL.md` that tells an AI coding agent how to do one job well.

## Skills

| Skill | What it does |
|-------|--------------|
| [dev-interview](skills/dev-interview/SKILL.md) | Runs a mock software developer interview with five configurable hint levels (0 none to 4 full walkthrough), then saves a session summary. |

## Layout

```
skills/
  <skill-name>/
    SKILL.md          # required: frontmatter + instructions
    *.md              # optional reference files, linked from SKILL.md
    scripts/          # optional helper scripts
template/
  SKILL.md            # starting point for a new skill
AGENTS.md             # entry point for tools without native skill support
.claude/skills        # symlink to ../skills, for Claude Code in this repo
```

## Using a skill

- **Claude Code, in this repo:** skills are available as slash commands through the `.claude/skills` symlink.
- **Claude Code, in another project:** copy or symlink a skill folder into that project's `.claude/skills/`, or into `~/.claude/skills/` for all projects.
- **Other tools:** the `SKILL.md` format is plain markdown with YAML frontmatter. Copy the folder to wherever your tool reads skills, or point it at `AGENTS.md`. Check your tool's docs for its skills path.

## Adding a skill

1. Copy `template/SKILL.md` to `skills/<new-name>/SKILL.md`.
2. Write a `description` that says what the skill does and starts its triggers with "Use when". It is the only thing the agent sees when deciding to load the skill.
3. Keep `SKILL.md` short and move detail into linked files.
4. Add the skill to the tables in this README and in `AGENTS.md`.

## Notes

- `dev-interview` writes its session summaries to `sessions/` in the project where it runs. That folder is gitignored here, so interview notes stay private.
- Windows checkouts may need symlinks enabled for `.claude/skills`.
