# Release Process

The process of creating a release is described in this document. Replace `X.Y.Z` with the version to be released.

## 1. Create a `release-X.Y.Z` branch

The `release-X.Y.Z` branch should be created from the desired tag in [helm repository](https://github.com/helm/helm.git).
For example, to create a new branch based on helm tag v3.7.2 the following commands can be executed:

```
git remote add helm https://github.com/helm/helm.git
git fetch helm
git checkout tags/v3.7.2 -b release-3.7.2
```

## 2. Create a `fybrik-release-X.Y.Z` branch

Based on the branch that was created in previous section, a new branch `fybrik-release-X.Y.Z` should be created 
with additions to support OCI registry.

## 3. Create a [new release](https://github.com/fybrik/helm/releases/new) 

Use `vX.Y.Z-fybrik-update` tag and set `fybrik-release-X.Y.Z` as the target.

Ensure that the release notes explicitly mention upgrade instructions and any breaking change.
