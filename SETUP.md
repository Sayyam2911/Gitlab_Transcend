# Setup and access

Updated: 2026-10-23. Only mark steps complete after observing success or receiving explicit user confirmation.

## Sequence

1. Confirm Devpost participation and sign in to the intended GitLab.com account.
2. Open [Transcend contributor onboarding](https://contributors.gitlab.com/transcend-hackathon/) and submit the hackathon access request. Record its actual status and submission time.
3. While approval is pending, clone Excalidraw locally, record the exact revision, inspect upstream instructions, install matching dependencies, and verify the baseline build.
4. After approval, inspect the automatically created group, subgroup, project, and onboarding issue. Confirm the organizer-provided Developer + AI role, Duo access, and runner availability.
5. Configure Git authentication through the user's chosen login/credential flow. Set the provided GitLab project as the submission destination and preserve GitHub as upstream. Do not assume a project URL.
6. Import or push the source without overwriting organizer-created content. Inspect existing remote history first.
7. Verify a baseline GitLab pipeline and a minimal Duo operation before relying on an architecture that needs those permissions.
8. Select and configure hosting after architecture and cloud account/budget choices are settled.

## Observed local environment

| Item | Observed state |
| --- | --- |
| Workspace | Parent GitHub repository with the Excalidraw checkout registered as a pinned Git submodule |
| Git | 2.45.1.windows.1 |
| Node.js | 24.14.0; satisfies upstream >=18 requirement; upstream Dockerfile also uses Node 24 |
| npm | 11.19.1 |
| Corepack | 0.34.6 |
| Yarn | Repository pins 1.22.22; installation started through Corepack |
| Docker CLI | 29.6.1; Docker Desktop Linux engine is not running/reachable; using native Node for the baseline |
| Ancestor AGENTS.md files | None found in the inspected ancestor directories |
| GitHub terminal connectivity | Restricted connection failed; approved network-enabled clone succeeded |

## Account and permission status

| Item | Status |
| --- | --- |
| Devpost joined | Not verified |
| GitLab identity | Signed in as Sayyam2911, verified in browser |
| Contributor onboarding request | Submitted: user provided the portal's successful registration / awaiting admin approval message on 2026-10-23 |
| Organizer approval | Pending admin review, per portal message supplied by user |
| Provisioned GitLab project URL | Unknown |
| Developer + AI role | Not verified |
| Duo credits and flow execution | Not verified |
| GitLab runners | Not verified |
| GitLab push authentication | Not verified |
| Cloud project and billing | Not configured in this session |

The [official resources](https://gitlab-transcend.devpost.com/resources) state approval takes about 24 business hours; the workspace is provisioned after approval. They specify the Developer + AI role and 500 GitLab Credits per participant per month. Use the organizer-provided role first rather than requesting broader permissions by default.

## Baseline evidence

- Checkout path: `excalidraw/`.
- Source revision: `b7de45e88111f5680ae4bb3c3f3541c7d3b279fe` (upstream master observed 2026-10-23; not claimed to be a stable release tag).
- Local branch: `hackathon/baseline`.
- GitHub remote: `upstream`, pointing to `https://github.com/excalidraw/excalidraw.git`. GitLab destination remains unset.
- Clone preserves master history with a blob-filtered single-branch clone; older file contents may require network retrieval.
- Windows dependency installation: started with Yarn 1.22.22 and `--frozen-lockfile`; no successful completion captured. The former process session is no longer available. Reinstall on Ubuntu.
- Build: pending.
- Browser smoke check: pending.
- No cloud resources created or paid services enabled.

## Browser handoff

Opened the official contributor onboarding page and selected Get started. User completed GitLab account onboarding; signed-in identity Sayyam2911 was verified. The Contributor Platform requested `read_user` authorization, which the user handled. The user then supplied the portal confirmation: registration received and awaiting admin approval; a dedicated subgroup and project will be provisioned after review. Submission is confirmed by this user-provided portal message on 2026-10-23; exact time was not captured. Approval has not arrived. The portal's October 5 wording describes the start of provisioning, not an additional future waiting period.

## Local commands

Run in the `excalidraw` subdirectory. These process-local cache settings avoid changing the system-wide package manager installation:

```powershell
$env:COREPACK_HOME = Join-Path (Split-Path (Get-Location) -Parent) '.setup-cache\corepack'
$env:YARN_CACHE_FOLDER = Join-Path (Split-Path (Get-Location) -Parent) '.setup-cache\yarn'
corepack.cmd yarn install --frozen-lockfile --non-interactive --network-timeout 600000
corepack.cmd yarn build:app:docker
```

The `build:app:docker` script builds static application files with Sentry disabled; it does not itself build or run a Docker container. Build verification is still pending.

## Ubuntu continuation

The user is switching to dual-boot Ubuntu because of Windows setup issues. The workspace transfer repository is `https://github.com/Sayyam2911/Gitlab_Transcend.git`; this does not replace the required GitLab submission project.

```bash
git clone --recurse-submodules https://github.com/Sayyam2911/Gitlab_Transcend.git
cd Gitlab_Transcend
```

Install Git and Node.js 24 using trusted distribution/vendor instructions if missing. The current source pins Yarn 1.22.22 and its Dockerfile uses Node 24. Ensure Corepack is available, then run:

```bash
cd excalidraw
corepack yarn --version
corepack yarn install --frozen-lockfile --non-interactive --network-timeout 600000
corepack yarn build:app:docker
```

If Corepack is absent, install it from its official npm package after installing Node. Read the checkout's AGENTS.md before editing application code. Package installation, build, and browser smoke verification remain pending until observed on Ubuntu.

The submodule references the public upstream commit, so recursive cloning does not depend on an unpublished local source commit. A newly initialized submodule normally has a detached HEAD; create a working branch before making changes. Publish future source commits to a writable fork or the provisioned GitLab project before committing their pointer in this parent repository.
