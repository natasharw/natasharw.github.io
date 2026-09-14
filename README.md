# natasharw.github.io

The live site at <https://natasharw.github.io>. Plain HTML, no build step.

## Which branch is live

**`main` is the live branch.** GitHub Pages serves it. It holds the apps
homepage (`index.html`), the per-app legal pages (`legal/`), and
`app-ads.txt` for AdMob verification.

**`gh-pages` is retired.** It holds an old Jekyll portfolio theme that is no
longer published. Don't edit it, and don't be misled if your local checkout
is sitting on it: `git checkout main` first.

There is also a separate `natasharw/legal` repo containing older copies of
the same legal pages. It is superseded by the `legal/` directory here. Edit
the pages in this repo, not that one.

## Legal page URLs are registered with Apple

App Store Connect holds the privacy policy and support URLs for each shipped
app, so **renaming a file in `legal/` breaks a link Apple depends on**. If a
page has to be renamed, leave a redirecting stub at the old path rather than
deleting it.

That is why `legal/rehearsal-privacy.html` and `legal/rehearsal-support.html`
still exist: the app formerly called Rehearsal shipped as **In Your Own
Words** in September 2026, its pages moved to `in-your-own-words-*.html`, and
the old paths now redirect. Apple still has the old URLs on file.

## Adding an app

Copy an existing pair in `legal/`, keep the `<app>-privacy.html` /
`<app>-support.html` naming, and add a card to `index.html` with the App
Store link.
