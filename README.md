# holbertonschool-continuous_integration

## Task 0

## workflow
https://github.com/FlorianRoosebeke/holbertonschool-continuous_integration/actions/runs/37741502917

## Task 1

## CI proof

Successful pull request:
https://github.com/FlorianRoosebeke/holbertonschool-continuous_integration/actions/runs/37744216054

Failing pull request:
https://github.com/FlorianRoosebeke/holbertonschool-continuous_integration/actions/runs/37744828337

## Task 2 — Node.js test matrix

Tests passed with Node.js 18, 20, and 22:

https://github.com/FlorianRoosebeke/holbertonschool-continuous_integration/actions/runs/37747005077

## Task 3 — Dependency caching

| Run | Duration | Link |
|---|---:|---|
| Before npm cache | 16 seconds | [View run]https://github.com/FlorianRoosebeke/holbertonschool-continuous_integration/actions/runs/37753793718 |
| After npm cache | 17 seconds | [View run]|https://github.com/FlorianRoosebeke/holbertonschool-continuous_integration/actions/runs/37753850330/job/113233423504
CI cache enabled.

## Task 4 — Secrets and control flow

The `deploy-check` job uses the `CI_TOKEN` repository secret through
`${{ secrets.CI_TOKEN }}` without printing it.

It runs only after linting and all tests pass (`needs: [lint, test]`),
and only on the `main` branch.


## Task 0 – Build Docker image in CI

This project adds a GitHub Actions workflow that **builds a Docker image** on every `push` to the main branch.

- The workflow is in `.github/workflows/image.yml`.
- It uses `docker/build-push-action` with `push: false` to only test the build.
- The image is built from the `Dockerfile` at the root of the repository.

https://github.com/FlorianRoosebeke/holbertonschool-continuous_integration/actions/runs/37781744525/job/113326273538

## Task 1 - Docker image

The Docker image is built and published to GitHub Container Registry on every push to the `main` branch.

https://github.com/users/FlorianRoosebeke/packages/container/package/holbertonschool-continuous_integrations

## Task 2 - Docker image tags

Docker image tags are generated automatically:

- `latest` for the `main` branch
- Branch name, for example `main`
- Short commit SHA
- Git version tags, for example `v1.0.0`

## Task 3
test