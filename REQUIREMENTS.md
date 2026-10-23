# Requirements

Status: hackathon obligations recorded; implementation requirements are a draft for the architecture chat.

## Hackathon obligations

Verified against the [official rules](https://gitlab-transcend.devpost.com/rules) on 2026-10-23:

- Use GitLab Duo Agent Platform.
- Path B starts from an MIT-licensed open-source project and links to the original.
- New automation and deployment must be created during the submission period beginning October 5, 2026.
- Provide a public MIT-licensed GitLab repository, setup instructions, and visible pipeline history.
- Provide a publicly accessible deployed application; keep it available through the winner announcement, around November 16.
- Submit a demonstration video under three minutes on YouTube. Prefer Public visibility to satisfy the rules' wording.
- Submission deadline: October 27, 2026, 13:00 UTC / 18:30 IST.
- Google Cloud deployment is optional and eligible for up to 0.2 bonus points; include deployment code and the live URL if claiming it.

The [resources FAQ](https://gitlab-transcend.devpost.com/resources) additionally instructs participants to leave submitted materials and linked project content unchanged during judging. Preserve the submission version; continue subsequent work separately.

## Proposed functional requirements

- Accept a proposed Excalidraw code change.
- Exercise existing-drawing workflows and collect reproducible evidence.
- Diagnose a failure and attempt a bounded application-code repair.
- Stop with an explanation when checks remain unsuccessful.
- Prepare a release report identifying the exact tested version.
- Require user approval before production promotion.
- Check the deployed application after release.

## Proposed quality requirements

- Keep testing independent of the agent's claims.
- Prevent automated repair from weakening mandatory tests or release gates.
- Invalidate readiness when the tested source changes.
- Use synthetic drawings and keep credentials out of source and artifacts.
- Keep the setup feasible for one developer and one end-user product.

## Open questions

Exact failure scenario, fixture coverage, enforced permission boundaries, source revision, test tools, deployment platform, and recovery behavior remain to be finalized.
