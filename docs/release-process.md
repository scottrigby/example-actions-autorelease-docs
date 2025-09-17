# Release Process

## Automated Release

1. Go to source repo Actions tab
2. Run "Prepare Release" workflow with target version
3. Draft release is created automatically
4. Review and publish the draft release
5. Documentation is automatically updated

## Manual Release (if CI fails)

1. Create release branch: `git checkout -b release-vX.Y.Z`
2. Update `version.json` with new version
3. Commit: `git commit -am "Prepare release vX.Y.Z"`
4. Push: `git push origin release-vX.Y.Z`
5. Create PR and merge to main
6. Create tag: `git tag vX.Y.Z && git push origin vX.Y.Z`
7. Create GitHub release from tag
8. Update docs repo `docs/config.yml`, `docs/versions.md`, `docs/index.md`
9. Create docs PR and merge
