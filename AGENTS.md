# Workspace continuity

Before working in this workspace, read PROJECT_CONTEXT.md, SETUP.md, and HANDOFF.md. Use DECISIONS.md to distinguish accepted decisions from proposals. Read the relevant architecture, requirements, or test-plan file for the task.

The source checkout is a pinned Git submodule in `excalidraw/`; follow its own AGENTS.md as well when working there. Workspace documentation is tracked in the parent GitHub repository. Initialize the submodule after cloning. Before making application changes, decide where to publish the source fork: do not point the parent repository at a source commit that exists only on one machine.

Keep observed setup results in SETUP.md and current handoff status in HANDOFF.md. Record confirmed architectural decisions in DECISIONS.md. Never record credentials or mark an account request, build, test, or deployment successful without evidence.

The user requested setup in the current chat and architecture refinement in a separate chat. Follow the current user's task scope and avoid concurrent edits to files owned by another active chat.
