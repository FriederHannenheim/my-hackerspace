# Releasing

Set variables:

    $ export VERSION=X.Y.Z
    $ export GPG_KEY=EA456E8BAF0109429583EED83578F667F2F3A5FA  # Danilo

Update version numbers:

    $ vim app/build.gradle

Update changelog:

    $ vim CHANGELOG.md

Add the changelog to `metadata/en-US/changelogs/<version>.txt` as well.

Commit & tag:

    $ git commit -S${GPG_KEY} -m "Release v${VERSION}"
    $ git tag -s -u ${GPG_KEY} v${VERSION} -m "Version ${VERSION}"
