# Progress import and diagnostic learning plans

Read this reference when a user wants an existing study record imported, a knowledge diagnostic before unit learning, or plans that exclude mastered topics.

## Preserve and merge records

- Inventory the backup schema and distinguish task completion, lesson self-rating, answers, test attempts, mock completion, stars, homework and schedule mappings. Do not silently treat a self-rating as diagnostic evidence.
- Validate known course, unit, task and question IDs. Migrate obsolete IDs explicitly; discard invalid date movement without discarding valid learning records. Do not infer assignment completion from a release date.
- Merge a supplied seed once per backup identity. Keep newer browser answers, choices and review states; combine historical attempts without duplicates. Retain existing timestamps and canonical question links. Reopening or resetting the site must not repeatedly reapply a seed.
- Export and import diagnostic answers, reports and history alongside prior progress. Recompute derived mastery from validated choices and the matching question bank; version or invalidate reports when that bank changes.
- Keep individual learner records out of reusable skills and GitHub packages. If the user specifically requests records embedded in their private site, that authorization does not make the records part of a reusable template.

## Whole-course reading and diagnostic entry

Provide one continuous textbook per subject, with a table of contents, all knowledge units, explanations, worked examples, source references, marked supplemental scope and offline printing. This is a compiled review textbook; do not claim it is the official assigned book. Preserve useful embedded figures and their labels.

Expose the textbook and diagnostic together in the subject entry and the diagnostic screen. A user should be able to read the subject as a whole before opening a unit. Existing unit pages and independent exercises can remain available.

Map diagnostic items to stable knowledge IDs. Use questions that distinguish comprehension and method selection, not repeated examples whose answers were just shown. Include “Not sure” rather than requiring guessing. Save draft answers, keep solutions closed until submission, and classify every covered unit; a high overall score must not hide a weak unit.

The motivating case uses two original English multiple-choice items per unit and an unchecked confirmation: “I can explain both answers and write the method without notes.” Both correct plus this confirmation means initial-screen mastery; correct choices alone do not. This number and criterion are a case implementation, not a universal requirement. For proof-heavy topics, retain a handwritten explanation or proof checkpoint and describe the limitation honestly.

## Plan from knowledge-level evidence

For unfinished teaching tasks, keep only weak or uncertain knowledge IDs. If every topic is mastered, skip the task without marking it complete. If a task contains several topics, reduce its workload and link to the first remaining topic. Retain completed historical tasks and answers.

Use diagnostic evidence ahead of older self-ratings after a complete diagnostic is submitted. Report the distinction visibly. On retest, update the current mastery assessment while preserving attempt history and wrong-answer history.

Retain independent practice, proof checkpoints, staged tests and the reserved full mocks needed to confirm learning beyond a short diagnostic. Replanning must preserve prerequisite order, protected rest days, phase constraints, fixed lecture reviews, exams and mock dates. Allocate repair work into available study budget; if the weak-topic list cannot fit, show the remaining queue and the reason. Do not silently declare those topics mastered or add unbounded catch-up work.

Route diagnostic mistakes back to the correct course panel and source knowledge unit. Correct retakes may change unresolved/reviewed state but must not erase earlier attempts. Include diagnostic mistakes in the existing sprint notebook and progress backup.

## Verify the behavior introduced

Exercise one merge, reload and export/import round trip. Check that newer browser answers survive, the supplied history remains, and the seed is applied once. Check an incomplete diagnostic, correct-but-unconfirmed answers, wrong/uncertain answers, a partially mastered multi-topic task and a fully skipped task. Verify the plan retains full mocks, workload constraints and protected dates; test textbook file links and diagnostic deep links. Stop once these concrete risks are verified.
