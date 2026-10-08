# holbertonschool-continuous_integration
## workflow
https://github.com/FlorianRoosebeke/holbertonschool-continuous_integration/actions/runs/37741502917

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

## Task 0 – Build Docker image in CI

This project adds a GitHub Actions workflow that **builds a Docker image** on every `push` to the main branch.

- The workflow is in `.github/workflows/image.yml`.
- It uses `docker/build-push-action` with `push: false` to only test the build.
- The image is built from the `Dockerfile` at the root of the repository.

Example GitHub Actions run