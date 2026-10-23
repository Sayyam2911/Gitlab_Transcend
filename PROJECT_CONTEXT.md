# Project context

Updated: 2026-10-23. Participant timezone: Asia/Kolkata.

## Confirmed direction

- Participant: solo developer; strongest in application development and AI, learning infrastructure while building.
- Hackathon: GitLab Life After Code on Devpost.
- Track: Path B, bringing an existing MIT-licensed project to GitLab.
- Autonomy: supervised; automation performs multiple steps and the user reviews the outcome before production release.
- Base project: [Excalidraw](https://github.com/excalidraw/excalidraw). References to Excalibur or Accelerator in conversation mean Excalidraw.
- Prefer one complete hosted end-user application, without a separate demonstration product.
- Candidate problem: protect existing drawings when releasing application updates.

## Current user request

First establish accounts, hackathon access, permissions, local Git checkout, and a verified build. Submit the access request early because organizer approval takes about 24 business hours. The user plans to finalize architecture in a separate chat and wants these Markdown files to carry context across chats.

## Proposed, not finalized

Setup update: the user is moving to dual-boot Ubuntu and supplied `https://github.com/Sayyam2911/Gitlab_Transcend.git` for transferring the workspace. Root documents and a pinned Excalidraw submodule are tracked there. Ubuntu build verification will resume after cloning; GitLab organizer approval remains pending.

- One GitLab Duo custom flow investigates a change, runs checks, attempts a bounded repair, and prepares release evidence.
- CI verifies behavior and deploys only the approved tested artifact.
- Google Cloud Run is the suggested hosting platform; account, billing, and deployment have not been configured.
- A small set of synthetic existing drawings covers persistence, editing, and export.
- Suggested initial repair limit: two attempts.
- Multiplayer, new product accounts, and in-app AI features are outside the proposed first scope.

## Key limitations

- A frontend release rollback does not restore data already modified in a browser.
- Excalidraw collaboration requires extra services beyond the basic editor deployment.
- Agent statements are not test evidence. Passing tests and linked artifacts should support release decisions.
- The precise regression, test library integration, build revision, permissions, and deployment flow require inspection and validation.
