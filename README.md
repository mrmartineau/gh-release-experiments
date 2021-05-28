# github-release-experiments

This repo is my playground for GitHub actions to release a webapp.

# Production Release workflow

- [x] When a production release is needed: run the "Create Release" workflow
  - [x] input release version number
  - [x] input git commit sha that will be used for this release
- [x] update the package.json version
- [x] add new git tag
- [ ] GitHub release notes and/or a changelog file should automatically be created
- [ ] Send message to Teams/Slack once the release is done

# Staging

- Every push to the `main` branch will trigger a release to the `staging` environment
  - this includes merges into `main` from PRs
  - commits to `main` should be restricted to PRs and workflow runs only

# PR

- Each PR should have its own preview deployment
