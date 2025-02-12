# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html),
and is generated by [Changie](https://github.com/miniscruff/changie).

## v0.2.2 - 2025-01-22

- _bug-fix_: Align autoassign tag number to 2.0.0 for auto-assign-action.

## v0.2.1 - 2025-01-22

- _security_: Improve release workflow with designated permissions in the reusable template.

## v0.2.0 - 2024-10-07

- _new-product-feature_: Improve linting with additional job that validates changie entry exists when it should be included. Certain exclusions are added such as labels for `dependencies` by Renovate, and `no-changie-required` label for exceptions. This will use PR comment type so automatic changes required will show up.
- _new-product-feature_: Template `changie-trigger-release` can be passed additional file paths that `git add {}` would take allowing repos like dsv-k8s to include chart and other files that get modified during changie update to be included.
- _bug-fix_: Use the calculated label instead of hard coded value for the dependencies add.

## v0.1.2 - 2024-07-18

- _refactor_: If new format of kind is used with keys, then use this, else use the prior format, to avoid breaking repos with older changie configs.

## v0.1.1 - 2024-01-25

### 🔨 Refactor

- Aqua path is different for different repos. Use `jq` to parse out the path detected by aqua dynamically (first only) so that aqua path is always correctly used in updating tags for package.

## v0.1.0 - 2024-01-23

### 🎉 Feature

- New template to simplify maintenance by workflow dispatch adding required changelog entries to create a pull request that bumps the version and runs changie commands to generate a new release.

This is done to help the development effort to bump a release based on dependency updates without having to clone and run cli tools locally.

- New template to trigger a changie based release from just CI. Will create PR for release to be reviewed and approved.

### ⬆️ Dependencies

- Maintenance release due to updated dependencies.

## v0.0.46 - 2024-01-18

### 🔨 Refactor

- Adjust linting permissions back down to avoid issues with downstream calls requiring too many permissions.

## v0.0.45 - 2023-04-11

### 🤖 CI & Build

- Add aqua policy env variable to allow installation of policies in current project. This further improves supply chain security for ci tooling and dev tools.

## v0.0.44 - 2023-04-11

### 🔨 Refactor

- Change lint, test, and scan to not cancel on concurrency match. This is causing downstream problems with composite based using pipelines.

## v0.0.43 - 2023-03-03

### 🔨 Refactor

- Lint workflow now runs aqual install with the args: `--tags lint` to allow setting up tooling via Aqua. This can help eliminate the need to resetup sealed versions of tools like Golangci-lint which are already configured in aqua.yaml and resetup via trunk can be slow or cause mismatch in versioning.

## v0.0.42 - 2023-03-03

### 🎉 Feature

- Add new template for caching trunk to improve the results of linting checks performance.
- Add new template for annotations based on trunk result.
  This will eventually run seperately from trunk to allow forks to securely be annotated as well.
  At this time it's just a unused template.
