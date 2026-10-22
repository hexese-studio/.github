# Security policy

## Reporting a vulnerability

Please do not open a public issue. Write to **info@hexese.com** with the
subject "Security" and the name of the site or repository (hexese.com,
amtsorakel.de, the Amtsorakel app). Describe what you found, how to reproduce
it and what impact it has. You will usually get an answer within seven days.
There is no bounty programme; credit in the release notes on request.

## Scope

- hexese.com and amtsorakel.de: anything that breaks the promises of the
  privacy policies (outbound requests, data sharing), bypasses the Content
  Security Policy, injects scripts or affects the upload to the server.
- The Amtsorakel app and its backend: access to another person's letters,
  deadlines or account data, and anything that keeps data after it was deleted.

## Supported versions

Only what is live — the state of `main` in each repository — receives fixes.

## Secrets

The repositories never contain credentials. If you find a key in a repository
or its history, report it immediately: it is revoked at the provider, not only
removed from the repository.

Each repository may carry its own `SECURITY.md` with details; it takes
precedence over this file.
