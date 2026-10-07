# Skills and tooling actually used in the motivating task

The initial website was built with existing installed skills; GitHub/OpenAI catalogue discovery did not itself install a skill. After the user explicitly requested `find-skills`, it was installed from the official Vercel Labs repository and its local SKILL.md was read. This later installation supports future discovery; it was not the tool that authored the initial website.

| Skill | Actual role | Source in this session |
|---|---|---|
| `sites:sites-building` | Website structure and static implementation workflow | Existing Sites plugin, version 0.1.75 |
| `sites:sites-hosting` | Site identity, source workflow, private deployment and status | Existing Sites plugin, version 0.1.75 |
| `pdf:pdf` | Course/PDF reading, extraction, question-only paper preparation and visual verification | Existing primary-runtime PDF plugin |
| `skill-installer` | Discover options and install the explicitly requested find-skills | Existing system skill |
| `find-skills` | Installed and read following the user’s request; supports subsequent skill discovery | [vercel-labs/skills](https://github.com/vercel-labs/skills/tree/main/skills/find-skills) |
| `visualize:visualize` | Consulted for visual composition; final diagrams use self-contained SVG in HTML, not hosted inline widgets | Existing bundled visualization skill |
| `skill-creator` | Create and validate this reusable skill and its references | Existing system skill |

The OpenAI maintained public skills catalogue is [openai/skills](https://github.com/openai/skills). This is a catalogue reference, not evidence that any specific repository revision was installed. The system skills above were used from their already available local copies; plugin skill paths belong to the session's local plugin installation. On another machine, discover available skill names and paths instead of assuming those paths or versions.

## Implementation evidence

- Source: `content.py`, `tests.py`, `build.py`, `app.js`, `adaptive.js`.
- Bilingual teaching and practice: `english_content.py`, `calculus_details.py`.
- Embedded offline diagrams: `visuals.py`, `visuals.js`.
- Original complete mocks and separate solutions: `mock_papers.py`, `mock_english.py`.
- Course-paper preparation: `prepare_papers.py`.
- Meaningful local checks used a browser to exercise the workflow, native PDF rendering for extracted paper layout, and independent rational row reduction to verify supplied matrix RREFs, exceptional ranks and inverse products.

- Complete per-subject reading and diagnostic bank: `diagnostic_build.py`, `diagnostic_bank.py`; continuous textbook HTMLs and mapped English screening items.
- Imported progress and adaptive diagnosis: `diagnostics.js`, `progress_seed.json` in the private project, plus changes to `app.js`, `adaptive.js`, `mistakes.js`; the personal seed is not shipped in this skill package.
- Assignment reminders: `homework.js`; exact known due times, editable verification and separate release-date notes.
- Sprint notebook: `mistakes.js`, `stars.js`; wrong-answer history, review state, lesson stars and combined offline HTML export.

Do not inherit personal local file paths, site IDs, login details, or the failed publication state into another project. Reuse the workflow decisions, not the old project's identity. Never store credentials in a skill.

## Subsequent update

The latest progress-and-diagnostic update consulted the existing `bilingual-exam-review-site` and `sites:sites-hosting` skills; the prompt archive and reusable instructions were then updated with `skill-creator`. No additional GitHub skill was installed for that update. The GitHub-ready package contains this authored skill and provenance links, not copies of other skill distributions or the learner's progress JSON.
