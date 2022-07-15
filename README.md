# Materialize fork of Cilium

This is [Materialize](https://materialize.com)'s fork of
[Cilium](https://cilium.io).

Patches:

  *

Deploying a new version:

```
# Make changes
# Add note of changes to this README
make docker-cilium-image
git commit
VERSION=v11.4-mz.X
git tag -am $VERSION $VERSION
docker tag quay.io/cilium/cilium:latest materialize/cilium:$VERSION
git push materialize/cilium:$VERSION
```

Be sure to run the above commands from an x86 machine.
