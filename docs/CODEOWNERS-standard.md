# CODEOWNERS standard

GitHub does not inherit `CODEOWNERS` from the organization `.github`
repository. Each repository must contain its own `CODEOWNERS` file.

Use the organization team as the default owner:

```text
* @AtyaLibraries/maintainers
```

The bare organization handle is not a valid code owner. The
`@AtyaLibraries/maintainers` team must exist, have access to the repository,
and be visible to GitHub for review requests to work.

This standard should be added to the package repository template in a later
phase.
