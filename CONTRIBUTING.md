# Contributing

This file holds the rules that are the same for **every** repository in this
organization. What is specific to one project — what it does, how to run it,
what it deliberately will not do — lives in that project's own `AGENTS.md`,
`README.md` and `docs/ARCHITECTURE.md`. Read those first. Where they disagree
with this file, the project wins.

## Commit messages

Say what changed, and answer four questions:

- **What** changed.
- **Why** — the reason, not a restatement of the diff.
- **How it was verified** — the command you ran and what it printed.
- **How to roll it back.**

One logical change per commit. A commit that cannot stand on its own — does not
run, does not pass its own checks — is not finished.

## Do not bump the version

A version number is bumped as its own step, never as part of a feature or a fix.
A change that alters a version will be asked to drop that part. How a release
actually happens is documented per project, where the project has one.

## Contract changes update the docs in the same change

Anything a user can observe — behaviour, an interface signature, a configuration
key, an output format — must update the `README` (how to use it) and
`docs/ARCHITECTURE.md` (how the design changed) in the **same** change. If that
is not possible, list the debt explicitly instead of leaving it silent.

## Never paste credentials

Keys, tokens and session data do not belong in an issue, a pull request, a commit
message or a log. If a real credential reaches one of those, treat it as leaked:
revoke it first, then write the report.

## Security issues

Do not use the public issue tracker — see [SECURITY.md](SECURITY.md).
