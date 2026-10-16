# Konflux

Container images build on Konflux (`rosa-tenant` / `kflux-prd-rh02`).

| Component | Containerfile | Quay image |
| --------- | ------------- | ---------- |
| `rosa-seaplane-ecr-creds-sync` | `Dockerfile` | `quay.io/redhat-user-workloads/rosa-tenant/ecr-creds-sync` |

Application: `rosa-seaplane-ecr-creds-sync`.

| PipelineRun | Trigger |
| ----------- | ------- |
| `rosa-seaplane-ecr-creds-sync-on-pull-request` | Every pull request to `main` |
| `rosa-seaplane-ecr-creds-sync-on-push` | Every push to `main` |

Onboarding checklist and Quay tag rules: [HyperFleet Konflux onboarding](https://github.com/openshift-online/rosa-hyperfleet/blob/main/docs/konflux-onboarding.md).

Pin `:<full-git-sha>` from a green on-push build. PR tags `on-pr-<sha>` expire after 5 days.
