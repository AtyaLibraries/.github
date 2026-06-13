# Contributing

## Development setup

Install the SDK version specified by the affected repository, clone it, and
run the applicable validation commands:

```bash
dotnet restore
dotnet format --verify-no-changes
dotnet build --configuration Release --no-restore
dotnet test --configuration Release --no-build
dotnet pack --configuration Release --no-build
```

Some repositories may not contain tests or packable projects. Follow the
repository documentation when its validation steps differ.

## Branching model

Create a short-lived branch from `development` and open a pull request back to
`development`. These pull requests are squash-merged.

Release pull requests promote `development` to `master` and must use a merge
commit so the long-lived branches retain shared history.

## Commit style

Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/),
for example `feat: add parser support` or `fix: reject invalid input`. Keep
commits focused and include breaking-change footers when applicable.

Developer Certificate of Origin sign-off is optional unless the affected
repository requires it. To sign off, use `git commit -s`, which adds:

```text
Signed-off-by: Your Name <you@example.com>
```

## Pull request checklist

- Confirm the pull request targets `development`, except for a release
  promotion from `development` to `master`.
- Run `dotnet restore`.
- Run `dotnet format --verify-no-changes`.
- Run the Release build and applicable tests.
- Run `dotnet pack` for packable projects.
- Add or update tests for behavior changes.
- Update user-facing documentation and release notes when applicable.
- Confirm package metadata remains accurate.

## Security issues

Do not file public issues for vulnerabilities. Follow [SECURITY.md](SECURITY.md)
and report the issue privately through the affected repository.
