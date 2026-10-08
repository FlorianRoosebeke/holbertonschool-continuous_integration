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
