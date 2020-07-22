# SLO Bot

Lints for slo rules (issue_slo_rules.json) file and creates a check on the PR. Comments on the PR if it is invalid.

(https://github.com/googleapis/repo-automation-bots/blob/master/README.md) for deploying and testing your bots.

This bot uses nock for mocking requests to GitHub, and snap-shot-it for capturing responses; This allows updates to the API surface to be treated as a visual diff, rather than tediously asserting against each field.

## Usage:
Create Out of SLO label in the repo. Update `label_name.yml` with the name of OOSLO label. 

Create `issue_slo_rules.json` file inside of org level or repo level .github directory. This file should consist of a list of slo rules that either applies to all of the repos under the same organization or applies to a specific repository.

 Example:
  `name: ooslo`
