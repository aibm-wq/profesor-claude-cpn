# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this project is

A **Claude Skill** — a packaged instruction set that turns Claude into a personal tutor for the Anthropic Claude Partner Network (CPN) certification program. It runs inside **Cowork** (Claude Code on the web) and is deployed as a `.skill` ZIP file that users install directly.

All content and all user interactions are in **Spanish**.

## Repository structure

```
SKILL.md                    # The skill definition (YAML frontmatter + instruction body)
README.md                   # User-facing installation and usage guide
profesor-claude-cpn.skill   # Deployable ZIP archive (the actual install artifact)
references/
  c1_claude_code.md         # Teaching content for C1: Claude Code in Action
  c2_agent_skills.md        # Teaching content for C2: Introduction to Agent Skills
  c3_mcp.md                 # Teaching content for C3: Introduction to MCP
  c4_claude_api.md          # Teaching content for C4: Building with the Claude API
```

## Architecture

The skill has two layers:

**1. `SKILL.md` — behavioral instructions**
Contains the YAML frontmatter with activation triggers (e.g., `buen día profe`, `quiz`, `save`) and the full behavioral spec: session flow, teaching methodology, progress tracking, command responses, and quiz format. This is what Claude reads to know *how to behave*.

**2. `references/` — course content**
One file per course. Each file contains concept explanations, analogies, concrete examples, and the 3 quiz-evaluated key points per module. The skill reads only the active course's reference file per session. This is what Claude reads to know *what to teach*.

## Deployment workflow

The `.skill` file is a ZIP archive of `SKILL.md` + `README.md` + `references/`. After editing any of those files, repackage it:

```bash
zip -r profesor-claude-cpn.skill SKILL.md README.md references/
```

Users install by downloading `profesor-claude-cpn.skill` and clicking "Save skill" in Cowork. Changes are live only after the user reinstalls the updated `.skill` file.

## Skill behavior conventions

These rules are defined in `SKILL.md` and must be preserved when editing:

- **Strict module order** — modules are prerequisites; no skipping, even if the student requests it.
- **Verification before progression** — the tutor asks one comprehension question and waits for confirmation before marking a module complete and moving on.
- **Progress file** — session state is persisted to `PROGRESO_CPN.md` in the user's connected folder, not in the conversation. `save`/`hasta mañana` writes it; `clear` reads it to resume.
- **Quiz mode** — 5 multiple-choice questions (A/B/C/D), one at a time, with score and explanation of wrong answers at the end. Minimum passing score: 70%.
- **Session start flow** — every session: read `PROGRESO_CPN.md` → show progress dashboard → ask available time.

## Editing guidelines

- **Teaching content changes** (analogies, examples, quiz points): edit the relevant `references/cN_*.md` file.
- **Behavioral changes** (commands, session flow, teaching methodology): edit `SKILL.md`.
- **User-facing docs** (installation steps, command table): edit `README.md`.
- After any edit, repackage the `.skill` file (see above) and commit both the source files and the updated `.skill`.
