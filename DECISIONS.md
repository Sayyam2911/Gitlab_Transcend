# Decision log

Use IDs to preserve the reasoning across chats. Mark a decision Accepted only when confirmed; do not silently turn a proposal into a requirement.

## D-001: Build on Excalidraw

- Date: 2026-10-23
- Status: Accepted
- Decision: Use the MIT-licensed Excalidraw repository for Path B.
- Reason: Mature standalone end-user product, strong visual demonstration, manageable basic editor hosting.
- Alternatives discussed: Memos, Reactive Resume, Actual Budget, Ghost, NextChat, and supporting tools.
- Consequence: Inspect the upstream build and preserve attribution; collaboration is a separate scope question.

## D-002: Supervised autonomy

- Status: Accepted
- Decision: Automate intermediate workflow steps and let the participant approve the release outcome.
- Reason: User prefers reviewing the result rather than approving each operation.

## D-003: Establish setup before finalizing architecture

- Date: 2026-10-23
- Status: Accepted
- Decision: Prioritize organizer access, accounts, Git clone, and baseline build; finalize architecture in another chat using these documents.

## D-004: Preserve existing drawings across releases

- Status: Proposed direction, endorsed in discussion; detailed scope pending
- Proposal: Demonstrate compatibility checks, agent-assisted repair, and supervised release against existing drawings.

## D-005: Transfer the workspace to Ubuntu through GitHub

- Date: 2026-10-23
- Status: Accepted destination; reversible repository layout selected during setup
- Decision: Use the user-provided `Sayyam2911/Gitlab_Transcend` GitHub repository for workspace continuity, tracking planning files in the parent repository and the unchanged Excalidraw baseline as a pinned submodule.
- Reason: The user is resuming in dual-boot Ubuntu. Recursive cloning restores the documents and original source without transferring Windows dependencies or caches.
- Consequence: Use `git clone --recurse-submodules`. Publish future Excalidraw changes to a writable source remote before updating the parent pointer. Final GitLab submission layout remains pending.

## Pending decisions

- Hosting platform and budget.
- Baseline revision and runtime versions.
- Trigger, bounded repair implementation, and retry count.
- Test corpus, regression, and evidence format.
- Branch protections, deployment permissions, and recovery mechanism.

## Template

### D-NNN: Title

- Date:
- Status: Proposed / Accepted / Superseded
- Context:
- Decision:
- Alternatives:
- Consequences:
- Evidence or source:
