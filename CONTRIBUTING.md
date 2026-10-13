# Contributing to Medical Transcriber PT

## Layout

The project ships three versions side by side — `Transcritor-Medico-PT/Windows`,
`Transcritor-Medico-PT/Linux` and `Transcritor-Medico-PT/macOS`. A change in one usually belongs in all
three. Before opening a pull request, check what differs between them:

```bash
git diff --no-index --stat Transcritor-Medico-PT/Windows Transcritor-Medico-PT/Linux
git diff --no-index --stat Transcritor-Medico-PT/Linux Transcritor-Medico-PT/macOS
```

Any difference that remains should be one the platform requires, and the
pull request should say why.

## Branches

Short-lived branches off `main`, one topic each, merged by pull request and
deleted on merge:

| Prefix | For |
| :--- | :--- |
| `feat/…` | new functionality |
| `fix/…` | bug fixes |
| `security/…` | security fixes |
| `docs/…` | documentation only |

`main` is protected: CI must be green on Windows, Linux and macOS before a
merge.

## Versions

Versions are **semver tags** (`vMAJOR.MINOR.PATCH`) with a GitHub release and
an entry in `Transcritor-Medico-PT/CHANGELOG.md` — never a branch per version.

## Tests

CI runs the full suite on all three platforms. Locally, run the tests for the
files you changed, from the platform folder you are working in.
