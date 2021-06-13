# conventional-changelog

Generate a changelog from git metadata, https://github.com/conventional-changelog/conventional-changelog/tree/master/packages/conventional-changelog-cli

## Quick start

```shell
# Generate CHANGELOG.md from current git repository
docker run -v $PWD:$PWD -w $PWD diodonfrost/hello-conventional-changelog:latest
```

This will not overwrite any previous changelogs. The above generates a changelog based on commits since the last semver tag that matches the pattern of "Feature", "Fix", "Performance Improvement" or "Breaking Changes".

If this is your first time using this tool and you want to generate all previous changelogs, you could do

```shell
docker run -v $PWD:$PWD -w $PWD diodonfrost/hello-conventional-changelog:latest conventional-changelog -p angular -i CHANGELOG.md -s -r 0
```

This will overwrite any previous changelogs if they exist.