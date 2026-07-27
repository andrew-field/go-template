# Title

[![Go Doc](https://pkg.go.dev/badge/github.com/andrew-field/REPONAME?status.svg)](https://pkg.go.dev/github.com/andrew-field/REPONAME "GoDoc")
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org)
[![Build and test](https://github.com/andrew-field/REPONAME/actions/workflows/build-test.yml/badge.svg)](https://github.com/andrew-field/REPONAME/actions/workflows/build-test.yml)
[![CodeQL](https://github.com/andrew-field/REPONAME/actions/workflows/github-code-scanning/codeql/badge.svg)](https://github.com/andrew-field/REPONAME/actions/workflows/github-code-scanning/codeql)
[![Super Linter](https://github.com/andrew-field/REPONAME/actions/workflows/super-linter.yml/badge.svg)](https://github.com/andrew-field/REPONAME/actions/workflows/super-linter.yml)

1. Update title (Don't remove for linting purposes).
2. Remove badges as necessary.
   - If the repository is private, can remove codeql.
   - Remove the Go Doc if the repository will not have a release.
3. Update this readme (badge links) with the correct REPONAME.
4. Add the my-github-authorised-app app client id as APP_CLIENT_ID and the my-github-authorised-app private key as APP_PRIVATE_KEY as action repository secrets.
5. - If the repository is a package to be released, add the release please personal access token as RELEASE_PLEASE_TOKEN as an action repository secret.
   - If the repository is NOT a package to be released, delete the release-please yaml file.
6. Go through the workflow yaml files and check things look correct. Check if the -race flag should be removed in build-test.
7. If the repository is public, add CodeQL code scanning from Settings -> Code security and analysis, use default settings.
8. Enable all settings in Settings -> Code security. This should include Dependabot version updates. Enabling this will add the corresponding yaml file. There should be two update sections, package-ecosystem "gomod" and package-ecosystem "github-actions". Should look similar to:
  ```
  -  package-ecosystem: "gomod"
    directory: "/"
    schedule:
      interval: "weekly"
    cooldown:
      default-days: 7
  - package-ecosystem: "github-actions"
    directory: "/"
    schedule:
      interval: "weekly"
    cooldown:
      default-days: 7
  ```
9. If public, in settings-> code security, enable private vulnerability reporting.
10. If the repository is public, in Settings->Branches, add a branch rule set, "MergeToMaster". Target branch default. The rules should be to
 - (By default restrict deletions).
 - Uncheck "Block force pushes" (To allow force pushes).
 - Require linear history.
 - Require signed commits.
 - Require a pull request.
 - Require conversation resolution before merging.
 - Allowed merge methods: Squash, Rebase.
 - Require status checks (Call build and test action).
 - Require the branch is up to date.
11. In settings->actions, allow GitHub actions to create and approve pull requests.
12. In general settings, check "Require contributors to sign off on web-based commits Loading", "Automatically delete head branches" and "Always suggest updating pull request branches".
13. In general settings, deselect "Allow merge commits".
14. In general settings, set the default commit message for squash merging to "Pull request title".
15. If the repository would benefit from the Biome formatter and linter, add a biome.json file.
