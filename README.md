# README.md

- [README.md](#readmemd)
  - [GitOps Settings](#gitops-settings)
    - [Gitlab settings](#gitlab-settings)
    - [Application Repository Configuration (CI Configuration)](#application-repository-configuration-ci-configuration)
      - [Configure CI file (.gitlab-ci.yaml)](#configure-ci-file-gitlab-ciyaml)


## GitOps Settings

### Gitlab settings

- Protected branches
  - Settings > Repository > Protected branches
    - dev
      - Allowed to merge: Maintainers
      - Allowed to push and merge: No one
    - prod
      - Allowed to merge: Maintainers
      - Allowed to push and merge: No one
- GitOps
  - Settings Access Token
    - Token name: argocd
    - Role: Maintainer
    - Scopes: api, read_api, read_respository, write_repository

**sample-gitops-example-dev-team**
> GIT_TOKEN_USER: argocd
> GIT_TOKEN: <generated_token>  

### Application Repository Configuration (CI Configuration)

- Variables
  - Settings > CI/CD > Variables:
    - GIT_TOKEN_USER: argocd
    - GIT_TOKEN: <generated_token>
