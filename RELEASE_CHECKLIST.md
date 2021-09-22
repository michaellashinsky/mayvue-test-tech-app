# RELEASE CHECKLIST

This checklist comes from something done with all projects.  It is modified per project and followed precisely.  It should be worked through when releasing a new version.

More info about our release process can be found in the [`RELEASE_PROCESS.md`](./RELEASE_PROCESS.md) document.

## Pre-Release

- [ ] Look through all open issues and PRs (if any) of that release and close them / move them to another
release if still open
- [ ] Look through all closed issues and PRs of that release to see what has changed.
- [ ] Close release on JIRA
- [ ] Create a new draft release in JIRA

# Testing

- [ ] Deploy and test release intensively
- [ ] Look through the release and test all new major changes
- [ ] Run `npm test`

## Prepare Package

- [ ] Create a new branch to bump version in `package.json`
- [ ] Install the latest `npm` version or if CI testing requires, Docker container with latest `node` and `npm`
- [ ] Bump version in `package.json`, remove `node_modules` folder and run `npm install` and `npm prune --production && npm shrinkwrap`
- [ ] Look through closed PRs and update `CHANGELOG.md`
- [ ] Make sure all files that need to be pushed are included in `package.json -> files`
- [ ] Send PR and merge PR with new version to be released
- [ ] Add the changes made to `CHANGELOG.md`
- [ ] Go back to branch you want to release from (e.g. `master`) and pull bumped version changes from GitLab
- [ ] Make sure there are no local changes to your repository (or reset with `git reset --hard HEAD`)
- [ ] Check `package.json`, `package-lock.json` and `npm-shrinkwrap.json` version config to make sure it fits what we want to release

## Releasing

- [ ] Publish the new functions
- [ ] Verify new versions exist in Prod
- [ ] Circulate Release Notes
- [ ] Circulate Build Procedures if updated


## Validate Release

- [ ] Validate that all functionality are up and running
- [ ] Execute any automation/integration tests (postman/gatling for endpoints, selenium)

## Post-Release

- [ ] Execute all V/V test cases and concurrency tests verifying that the scaling occurs