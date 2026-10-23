# Verification plan

Status: draft; no test or build result should be implied by this plan.

## Baseline setup checks

1. Record the upstream revision and read applicable repository instructions.
2. Check package manager and runtime declarations.
3. Install dependencies using the committed lockfile.
4. Build the application without changing application logic.
5. Serve the built application locally and verify the editor loads, creates a drawing, and can export it.
6. Record exact outcomes and any limitations in SETUP.md and HANDOFF.md.

## Proposed compatibility journeys

- Load an existing drawing, edit, save, and reopen while preserving content.
- Exercise shape movements, labels, and undo/redo.
- Export existing drawings to SVG and PNG.
- Preserve browser storage across a version transition.

Check semantic drawing data as well as visible output. Fix browser/font conditions before using image comparisons.

## Proposed agent evaluation

- Passing candidate proceeds without unnecessary repair.
- A controlled regression produces useful evidence and a verified fix.
- An unresolved regression stops after the configured attempt limit.
- Changes to mandatory checks or expected results block unattended release.
- New source changes invalidate evidence for an older candidate.
- Production promotion requires human action.

Select a small, meaningful subset after inspecting upstream tests. Do not claim arbitrary bug repair or production safety beyond measured scenarios.
