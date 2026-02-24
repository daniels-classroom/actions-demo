# Actions Demo

A collection of well-commented GitHub Actions workflows designed to introduce
someone who is completely new to Actions to its core concepts.

## Workflows

| File | Trigger | Concepts covered |
|------|---------|-----------------|
| [`01-hello-world.yml`](.github/workflows/01-hello-world.yml) | `push` to main, manual | Workflow structure, `run` steps, expressions, context variables |
| [`02-greet-on-pr.yml`](.github/workflows/02-greet-on-pr.yml) | Pull request opened | `pull_request` trigger, `permissions`, `actions/github-script`, GitHub API |
| [`03-basic-ci.yml`](.github/workflows/03-basic-ci.yml) | `push` / PR to main, manual | `actions/checkout`, `actions/setup-node`, caching, artifacts, strategy matrix |
| [`04-multi-job.yml`](.github/workflows/04-multi-job.yml) | `push` to main, manual | Multiple jobs, `needs`, job outputs, `if` conditions, `concurrency` |
| [`05-scheduled.yml`](.github/workflows/05-scheduled.yml) | Daily cron, manual | `schedule`, cron syntax, `secrets`, environments, `inputs` |

## Key Concepts at a Glance

- **Triggers (`on:`)** – events that start a workflow (push, pull_request, schedule, workflow_dispatch, …)
- **Jobs** – independent units of work, each running on a fresh virtual machine
- **Steps** – individual tasks inside a job; either shell commands (`run:`) or pre-built Actions (`uses:`)
- **Actions** – reusable building blocks published to the [GitHub Marketplace](https://github.com/marketplace?type=actions)
- **Expressions `${{ }}`** – embed dynamic values from context, secrets, or step outputs
- **Artifacts** – files uploaded during a run that can be downloaded from the Actions UI
- **Matrix** – run the same job across multiple OS or language versions in parallel
- **Secrets** – encrypted values stored in repo settings, never visible in logs

## Learning Path

Read the workflows in order (01 → 05). Each one builds on the previous and
introduces a small set of new concepts with inline comments explaining the *why*.
