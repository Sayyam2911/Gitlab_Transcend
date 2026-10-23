# Architecture working document

Status: PROPOSED. Finalize in the user's separate architecture chat after baseline setup.

## Candidate components

| Component | Proposed responsibility |
| --- | --- |
| Excalidraw fork | End-user drawing application |
| GitLab Duo custom flow | Understand changes, investigate failures, propose repairs, summarize evidence |
| GitLab CI jobs | Build, test, enforce gates, package, and deploy |
| Synthetic drawing fixtures | Reproducible compatibility examples |
| Container registry | Store identifiable release artifacts |
| Cloud Run, subject to choice | Host application revisions and support controlled promotion |

## Candidate workflow

User change -> explicit flow trigger -> inspect and verify -> bounded repair loop -> package and verify candidate -> release report -> human production approval -> promotion -> live checks.

## Decisions still needed

- Which Excalidraw revision becomes the baseline?
- Which regression is realistic, bounded, and reproducible?
- How are mandatory checks kept independent of repairs?
- How does the flow execute tests and handle its own repair loop?
- How do source changes invalidate old approval/evidence?
- Where does a candidate run before production promotion?
- How is production access separated from agent execution?
- How do we handle failed deployment checks and browser-data compatibility?
- How is the upstream history integrated with the provisioned GitLab project's existing files?

## References

- [GitLab custom flows](https://docs.gitlab.com/user/duo_agent_platform/flows/custom/)
- [Flow execution](https://docs.gitlab.com/user/duo_agent_platform/flows/execution/)
- [Manual jobs](https://docs.gitlab.com/ci/jobs/job_control/)
- [Excalidraw development and self-hosting](https://docs.excalidraw.com/docs/introduction/development)
- [Cloud Run revisions and traffic](https://docs.cloud.google.com/run/docs/rollouts-rollbacks-traffic-migration)

Documentation describes possible capabilities, not proof they are enabled in the participant's project.
