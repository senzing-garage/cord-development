# Workflows

## add-labels-standardized.yaml

When issues are opened or reopened,
this action adds appropriate labels to the issue.
(e.g. "triage", "customer-submission")

- [Add Labels Standardized GitHub Action]
  - Uses: [senzing-factory/build-resources/.../add-labels-to-issue.yaml]

## add-to-project-garage-dependabot.yaml

When a Dependabot Pull Request (PR) is made against `main` branch,
this action adds the PR to the "Garage" project board as "In Progress".

- [Add to Project Garage Dependabot GitHub Action]
  - Uses: [senzing-factory/build-resources/.../add-to-project-dependabot.yaml]

## add-to-project-garage.yaml

When an issue is opened or reopened,
this action adds the issue to the "Garage" board as "Backlog".

- [Add to Project Garage GitHub Action]
  - Uses: [senzing-factory/build-resources/.../add-to-project.yaml]

## check-claude-attribution.yaml

When a Pull Request (PR) is opened, updated, reopened, or its description is edited,
this action reports a failing check if any of its commits or its description carry a Claude attribution trailer.

- [Check Claude Attribution GitHub Action]
  - Uses: [senzing-factory/build-resources/.../check-claude-attribution.yaml]

## claude-pr-review.yaml

When a Pull Request is opened or updated,
this action runs an automated Claude code review.

- [Claude PR Review GitHub Action]
  - Uses: [senzing-factory/build-resources/.../claude-pull-request-review.yaml]

## dependabot-approve-and-merge.yaml

When a Dependabot Pull Request (PR) is made against the `main` branch,
this action determines if it should be automatically approved and merged into the `main` branch.
Once this action occurs [move-pr-to-done-dependabot.yaml] moves the PR on the "Garage" project board to "Done".

- [Dependabot Approve and Merge GitHub Action]
  - Uses: [senzing-factory/build-resources/.../dependabot-approve-and-merge.yaml]

## lint-workflows.yaml

When a Pull Request is made against the `main` branch,
this action runs [super-linter] to run multiple linters against the code.

- [Lint Workflows GitHub Action]
  - Configuration:
    - [.checkov.yaml]
    - [.jscpd.json]
    - [.yaml-lint.yml]
    - [zizmor.yaml]
  - Uses: [senzing-factory/build-resources/.../lint-workflows.yaml]

## move-pr-to-done-dependabot.yaml

When a Pull Request is closed against the `main` branch,
this action moves the PR on the "Garage" project board to "Done".

- [Move PR to Done Dependabot GitHub Action]
  - Uses: [senzing-factory/build-resources/.../move-pr-to-done-dependabot.yaml]

## spellcheck.yaml

When a Pull Request is made against the `main` branch,
this action runs [cspell] to check spelling, as configured by [.vscode/cspell.json].

- [Spellcheck GitHub Action]
  - Configuration:
    - [.vscode/cspell.json]
  - Uses: [senzing-factory/build-resources/.../cspell.yaml]

[.checkov.yaml]: ../linters/README.md#checkovyaml
[.jscpd.json]: ../linters/README.md#jscpdjson
[.vscode/cspell.json]: ../../.vscode/cspell.json
[.yaml-lint.yml]: ../linters/README.md#yaml-lintyml
[Add Labels Standardized GitHub Action]: add-labels-standardized.yaml
[Add to Project Garage Dependabot GitHub Action]: add-to-project-garage-dependabot.yaml
[Add to Project Garage GitHub Action]: add-to-project-garage.yaml
[Check Claude Attribution GitHub Action]: check-claude-attribution.yaml
[Claude PR Review GitHub Action]: claude-pr-review.yaml
[cspell]: https://cspell.org/
[Dependabot Approve and Merge GitHub Action]: dependabot-approve-and-merge.yaml
[Lint Workflows GitHub Action]: lint-workflows.yaml
[Move PR to Done Dependabot GitHub Action]: move-pr-to-done-dependabot.yaml
[move-pr-to-done-dependabot.yaml]: move-pr-to-done-dependabot.yaml
[senzing-factory/build-resources/.../add-labels-to-issue.yaml]: https://github.com/senzing-factory/build-resources/blob/main/.github/workflows/add-labels-to-issue.yaml
[senzing-factory/build-resources/.../add-to-project-dependabot.yaml]: https://github.com/senzing-factory/build-resources/blob/main/.github/workflows/add-to-project-dependabot.yaml
[senzing-factory/build-resources/.../add-to-project.yaml]: https://github.com/senzing-factory/build-resources/blob/main/.github/workflows/add-to-project.yaml
[senzing-factory/build-resources/.../check-claude-attribution.yaml]: https://github.com/senzing-factory/build-resources/blob/main/.github/workflows/check-claude-attribution.yaml
[senzing-factory/build-resources/.../claude-pull-request-review.yaml]: https://github.com/senzing-factory/build-resources/blob/main/.github/workflows/claude-pull-request-review.yaml
[senzing-factory/build-resources/.../cspell.yaml]: https://github.com/senzing-factory/build-resources/blob/main/.github/workflows/cspell.yaml
[senzing-factory/build-resources/.../dependabot-approve-and-merge.yaml]: https://github.com/senzing-factory/build-resources/blob/main/.github/workflows/dependabot-approve-and-merge.yaml
[senzing-factory/build-resources/.../lint-workflows.yaml]: https://github.com/senzing-factory/build-resources/blob/main/.github/workflows/lint-workflows.yaml
[senzing-factory/build-resources/.../move-pr-to-done-dependabot.yaml]: https://github.com/senzing-factory/build-resources/blob/main/.github/workflows/move-pr-to-done-dependabot.yaml
[Spellcheck GitHub Action]: spellcheck.yaml
[super-linter]: https://github.com/super-linter/super-linter
[zizmor.yaml]: ../linters/README.md#zizmoryaml
