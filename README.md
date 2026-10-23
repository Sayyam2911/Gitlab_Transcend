# GitLab Life After Code workspace

Workspace repository: [Sayyam2911/Gitlab_Transcend](https://github.com/Sayyam2911/Gitlab_Transcend).

Windows working directory: `C:\Users\Sayyam Jain\Desktop\Hackathons\Gitlab_Transcend`. On Ubuntu, use your own local clone directory.

Start with [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) and [HANDOFF.md](HANDOFF.md) when continuing in another chat.

## Documentation map

| File | Purpose |
| --- | --- |
| [AGENTS.md](AGENTS.md) | Entry instructions so future workspace chats find the context |
| [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) | User preferences, chosen project, and scope |
| [SETUP.md](SETUP.md) | Sequential account, access, clone, and build checklist; observed results |
| [REQUIREMENTS.md](REQUIREMENTS.md) | Hackathon obligations and proposed product requirements |
| [ARCHITECTURE.md](ARCHITECTURE.md) | Architecture working document; proposals remain provisional |
| [DECISIONS.md](DECISIONS.md) | Accepted decisions, alternatives, and unresolved decisions |
| [TEST_PLAN.md](TEST_PLAN.md) | Baseline verification and proposed compatibility scenarios |
| [HANDOFF.md](HANDOFF.md) | Current state and next actions for another chat |

## Workspace layout

These documents live at the workspace root. The Excalidraw source lives in `excalidraw/` as a Git submodule pinned to the recorded baseline. This preserves upstream history and lets one recursive clone restore the workspace. The source submodule retains its upstream MIT license and attribution. The final GitLab submission layout remains to be decided.

## Resume on Ubuntu

```bash
git clone --recurse-submodules https://github.com/Sayyam2911/Gitlab_Transcend.git
cd Gitlab_Transcend
```

If you already cloned without the recursive flag:

```bash
git submodule update --init --recursive
```

Read [HANDOFF.md](HANDOFF.md), then follow the Ubuntu instructions in [SETUP.md](SETUP.md). Start with a fresh dependency installation on Ubuntu; Windows package caches are not part of this repository.

The GitHub repository is the workspace transfer destination. The hackathon's GitLab project is still awaiting organizer provisioning.

Do not store passwords, access tokens, recovery codes, private keys, or cloud credentials in these documents.
