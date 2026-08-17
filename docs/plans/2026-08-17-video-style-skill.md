# Video Style Skill Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Build a public, reusable Codex project for defining and applying consistent video styles.

**Architecture:** Keep public project documentation outside the installable skill. Put the generic workflow, profile template, QA checklist, and example presets inside `video-style-skill/`; preserve the existing college style only as an example preset.

**Tech Stack:** Markdown, YAML, Codex Skills, optional HyperFrames, Git, GitHub

---

### Task 1: Create the distributable skill layout

**Files:**
- Create: `video-style-skill/SKILL.md`
- Create: `video-style-skill/agents/openai.yaml`
- Create: `video-style-skill/references/style-profile-template.md`
- Create: `video-style-skill/references/quality-checklist.md`

1. Create the new directory layout.
2. Write a renderer-neutral workflow with explicit priority and fallback rules.
3. Add a complete copyable style-profile template.
4. Add cross-renderer and HyperFrames-specific quality gates.
5. Validate the skill with `quick_validate.py`; expect `Skill is valid!`.

### Task 2: Convert the personal style into a preset

**Files:**
- Create: `video-style-skill/presets/college-social/profile.md`
- Move: `assets/approved-frame.md`
- Move: `assets/approved-reference-contact-sheet.jpg`
- Move: `assets/approved-template.html`

1. Rewrite the old specification as a profile that conforms to the generic template.
2. Move the existing visual reference and template into the preset.
3. Verify that all preset links resolve.

### Task 3: Write public project documentation

**Files:**
- Rewrite: `README.md`
- Remove: old root skill files after migration

1. Explain what the project is and what it is not while keeping it outside the nested installable Skill folder.
2. Document installation of the nested `video-style-skill/` folder.
3. Add profile and preset usage examples.
4. Show the final directory tree and customization workflow.

### Task 4: Verify and publish

**Files:**
- Verify: all project files

1. Run skill validation.
2. Run local link and path checks.
3. Commit the completed refactor.
4. Rename the GitHub repository to `video-style-skill`.
5. Upload the new tree and remove obsolete root files.
6. Compare the remote tree and file contents with the local commit.
