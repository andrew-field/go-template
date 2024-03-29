# Title

[![License](https://img.shields.io/github/license/andrew-field/REPONAME)](./LICENSE)
[![Go Report Card](https://goreportcard.com/badge/github.com/andrew-field/REPONAME)](https://goreportcard.com/report/github.com/andrew-field/REPONAME)
[![Codecov](https://codecov.io/gh/andrew-field/REPONAME/branch/master/graph/badge.svg)](https://codecov.io/gh/andrew-field/REPONAME)
[![Build and test](https://github.com/andrew-field/REPONAME/actions/workflows/build-test.yml/badge.svg)](https://github.com/andrew-field/REPONAME/actions/workflows/build-test.yml)
[![CodeQL](https://github.com/andrew-field/REPONAME/actions/workflows/github-code-scanning/codeql/badge.svg)](https://github.com/andrew-field/REPONAME/actions/workflows/github-code-scanning/codeql)
[![Lint Code Base](https://github.com/andrew-field/REPONAME/actions/workflows/linter.yml/badge.svg)](https://github.com/andrew-field/REPONAME/actions/workflows/linter.yml)

1. Update title (Don't remove for linting purposes).
2. Remove badges as necessary. If the repository is private, can remove go report card, Codecov, codeql. Remove licence badge if the repository will have no licence.
3. Update this readme (badge links) with the correct REPONAME.
4. If repository is private, remove the go report card workflow.
5. Add CodeQL code scanning from Settings -> Code security and analysis, use default settings. Can't add CodeQL if the repository is private.
6. Add Dependabot version updates from Settings -> Code security and analysis. There should be two update sections, package-ecosystem "gomod" and package-ecosystem "github-actions". Should look similar to:
- package-ecosystem: "gomod"
  directory: "/"
  schedule:
    interval: "weekly"
- package-ecosystem: "github-actions"
  directory: "/"
  schedule:
    interval: "weekly"
7. In settings->branches, update branch protection rule to require status checks, the branch is up to date and commits require a signature. Can't add these rules if the repository is private.
8. In settiings->actions, update GitHub actions workflow permissions to read and write. Allow GitHub actions to create and approve pull requests.
9. Check "Automatically delete head branches" and "Always suggest updating pull request branches" in settings main page.
