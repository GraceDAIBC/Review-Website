# bilingual-exam-review-site

A reusable Codex skill for building offline HTML exam-review portals from course materials: beginner explanations, continuous textbooks, English practice, knowledge diagnostics, preserved progress, adaptive daily plans, full mocks and sprint notebooks.

## Repository layout

```text
skills/bilingual-exam-review-site/
  SKILL.md
  agents/openai.yaml
  references/
    user-prompts.md
    skills-used.md
    progress-and-diagnostics.md
```

`user-prompts.md` archives the motivating user's requests and their latest effective scope. Its dates and personal planning preferences are examples, not defaults for another student. The package contains no course PDFs, passwords, site credentials or personal progress backup.

## Use in Codex

Copy `skills/bilingual-exam-review-site` into your Codex skills directory (normally `~/.codex/skills/`). If a skill with this name already exists, review and replace it with this version.

Example request:

> Use $bilingual-exam-review-site to build or update my HTML review portal. Import my existing progress, give each course a complete textbook and knowledge diagnostic, and plan from the topics I still need to learn.

## Upload to GitHub

Use the contents of this directory as a repository's files, preserving the `skills/bilingual-exam-review-site` hierarchy. The ZIP delivered with this version is a portable copy of the same directory. Uploading this package does not publish any study website or learner data.

## Provenance

This skill was authored from the study-website workflow and the user's requests. References record the skills actually consulted. `find-skills` was installed separately from the official Vercel Labs repository; its implementation is not included here. Bundled OpenAI/plugin skills were used in place, not copied into this repository.
