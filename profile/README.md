# Hexese

Software that speaks human. Hexese is the software studio of Aaron Kuyucu in
Frankfurt am Main — one person, run as a side business since 1 September 2026.
It builds tools that turn official German into sentences you understand at
first read.

## Projects

- **[Amtsorakel](https://amtsorakel.de)** — an app that explains letters from
  German authorities in plain language and keeps track of their deadlines. It
  quotes what the letter says and judges nothing. The product site is live in
  ten languages; the app is in development and not in any store yet.
- **[hexese.com](https://hexese.com)** — the studio site: a static export with
  WebGL2 scenes written without a library.

## How we work

- **No third-party requests.** No CDN, no external fonts, no tracking. The
  privacy policies promise it, and a Content Security Policy enforces it.
- **Checked before it ships.** Every build runs a gate that fails on outbound
  requests, inline style or script blocks and leftover markers, and checks that
  the legal notice and privacy policy are present. CI runs the same gate on
  every pull request.
- **Issue → branch → pull request → release.** `main` is what is live,
  `staging` collects reviewed work, and every go-live is a tagged release.
- **Deploys by hand only.** Nothing goes live on a push.

The product repositories are private. This repository holds the organisation
profile and the default community files (contributing guide, code of conduct,
security policy, issue and pull request templates).

Contact: [info@hexese.com](mailto:info@hexese.com)
