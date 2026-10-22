# Contributing to Hexese

This is the default guide for every repository in `hexese-studio`. A
repository with its own `CONTRIBUTING.md` (hexese-website, amtsorakel) takes
precedence; read that one first, then its `docs/ONBOARDING.md`.

## The flow in one line

    Issue → branch from staging → pull request into staging → review report → merge commit → release PR staging → main → deploy by hand

- **`main`** is production: what is live. It moves only through a release pull
  request `staging → main` titled `Release: staging → main (YYYY-MM-DD)`,
  followed by an annotated tag `vYYYY.MM.DD` and a GitHub release.
- **`staging`** is integration: reviewed and checked, not necessarily live.
- **Every plan becomes an issue** (templates: Bug, Feature, Task). Title:
  `Area: what`, as an English sentence.
- **One branch per issue**, cut from `staging`: `feature/…`, `fix/…`,
  `chore/…`, `docs/…`, `ci/…`, ideally with the issue number.
- **Pull request into `staging`**, title as a Conventional Commit ending with
  the issue number: `fix(header): keep the mark visible on dark scenes (#42)`.
  Body after the pull request template. The workflow "Checks" must be green.
- **Review report:** GitHub does not let you approve your own pull request, so
  every pull request carries one comment "Review report" listing what was
  actually checked — and nothing that was not.
- **Merge with a merge commit** (no squash). `Closes #n` does not fire on
  `staging`; close the issue by hand with "Shipped in #<pr> (staging)."
- **Deploy is never part of a merge.** Only the owner deploys, by hand.

## Commits

English, [Conventional Commits](https://www.conventionalcommits.org/):
`<type>(<scope>): <what changes, lower case, no full stop>`. Types: `feat`,
`fix`, `refactor`, `perf`, `style`, `docs`, `chore`, `ci`. No secrets, no
`.env`, no build output, no files over 20 MB.

## Enforcement, honestly

The product repositories are private on the GitHub Free plan, where branch
protection and rulesets are not available. The rules above are a convention,
kept by CI, the review report and the owner's review (`CODEOWNERS`).

## Conduct and security

Everyone follows the [Code of Conduct](CODE_OF_CONDUCT.md). Security issues go
by e-mail, never into a public issue — see [SECURITY.md](SECURITY.md).
