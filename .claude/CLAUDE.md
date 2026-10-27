# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This repository holds CORD, a "Senzing-Ready Data Collection".
What a CORD contains is not yet defined and no issue tracks that question yet; the
definition is the development team's to write. DevOps owns the repository's
configuration -- workflows, linters, branch protection -- not its contents.
Do not infer it.
The repository was created from [senzing-garage/template-repository](https://github.com/senzing-garage/template-repository) and currently holds only the standard Senzing Garage artifacts: README, CONTRIBUTING, CODE_OF_CONDUCT, LICENSE, CHANGELOG, SECURITY, and GitHub workflows.

## CI/CD and Automation

GitHub Actions workflows are thin callers of reusable workflows from [senzing-factory/build-resources](https://github.com/senzing-factory/build-resources).
See [.github/workflows/README.md](../.github/workflows/README.md) for the full list.

- **lint-workflows.yaml**: Runs super-linter on PRs to main, restricted to files under `.github/`
- **spellcheck.yaml**: Runs cspell on PRs to main, configured by `.vscode/cspell.json`
- **check-claude-attribution.yaml**: Reports a failing check on a PR to main that carries a Claude attribution trailer
- **claude-pr-review.yaml**: Automated Claude PR review on opened/synchronized PRs
- **dependabot-approve-and-merge.yaml**: Auto-approves and merges dependabot PRs
- **move-pr-to-done-dependabot.yaml**: Moves a closed PR to "Done" on the Garage project board
- **add-to-project-garage-dependabot.yaml**: Adds a PR to the Garage project board
- **add-labels-standardized.yaml**: Adds labels to new issues
- **add-to-project-garage.yaml**: Adds issues to the Garage project board

## CHANGELOG Convention

CHANGELOG.md follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) format with [Semantic Versioning](https://semver.org/). Changes are manually curated (not auto-generated) to describe user-facing impacts.

## Claude Slash Commands

- `/senzing` - Runs steps from the centralized senzing command
