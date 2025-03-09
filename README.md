# Title

[![License](https://img.shields.io/github/license/andrew-field/REPONAME)](./LICENSE)
[![Go Doc](https://pkg.go.dev/badge/github.com/andrew-field/REPONAME?status.svg)](https://pkg.go.dev/github.com/andrew-field/REPONAME "GoDoc")
[![GitHub Release](https://img.shields.io/github/v/release/andrew-field/REPONAME)](https://github.com/andrew-field/REPONAME/releases/latest "GitHub release")
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org)
[![Go Report Card](https://goreportcard.com/badge/github.com/andrew-field/REPONAME)](https://goreportcard.com/report/github.com/andrew-field/REPONAME)
[Code cov markdown goes here]
[![Build and test](https://github.com/andrew-field/REPONAME/actions/workflows/build-test.yml/badge.svg)](https://github.com/andrew-field/REPONAME/actions/workflows/build-test.yml)
[![CodeQL](https://github.com/andrew-field/REPONAME/actions/workflows/github-code-scanning/codeql/badge.svg)](https://github.com/andrew-field/REPONAME/actions/workflows/github-code-scanning/codeql)
[![Super Linter](https://github.com/andrew-field/REPONAME/actions/workflows/super-linter.yml/badge.svg)](https://github.com/andrew-field/REPONAME/actions/workflows/super-linter.yml)

1. Update title (Don't remove for linting purposes).
2. Remove badges as necessary.
   - If the repository is private, can remove go report card and codeql.
   - Remove licence badge if the repository will have no licence.
   - Remove the Go Doc and Github Release badge if the repository will not have a release.
3. Update this readme (badge links) with the correct REPONAME.
4. Go to Code Cov and copy the badge markdown to the top and bottom of the readme. Copy the icicle svg link and replace the link in the code cov - svg markdown at the bottom.
5. Add the global upload token from Code cov as CODECOV_TOKEN as an action repository secret.
6. Add the bump go version personal access token as BUMP_GO_VERSION_TOKEN as an action repository secret.
7.
   - If the repository is a package to be released, add the release please personal access token as RELEASE_PLEASE_TOKEN as an action repository secret.
   - If the repository is NOT a package to be released, delete the release-please yaml file.
8. If repository is private, remove the go report card workflow.
9. Go through the workflow yaml files and delete the incorrect action permissions depending on whether the repository is private or not. The files have the necessary comments.
10. If repository is public, add CodeQL code scanning from Settings -> Code security and analysis, use default settings.
11. Add Dependabot version updates from Settings -> Code security and analysis. Enable all options (If the repo is private, do not need to enable "Dependabot on self-hosted runners").
12. Update the dependabot file. There should be two update sections, package-ecosystem "gomod" and package-ecosystem "github-actions". Should look similar to:
  ```
  -  package-ecosystem: "gomod"
    directory: "/"
    schedule:
      interval: "weekly"
  - package-ecosystem: "github-actions"
    directory: "/"
    schedule:
      interval: "weekly"
  ```
13. If public, in settings-> code security, enable private vulnerability reporting.
14. In settings->branches, update branch protection rule to require status checks, the branch is up to date and commits require a signature. Can't add these rules if the repository is private.
15. In settings->actions, allow GitHub actions to create and approve pull requests.
16. Check "Automatically delete head branches" and "Always suggest updating pull request branches" in settings->general page.

[Code cov icicle svg markdown goes here]
