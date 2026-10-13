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

## Other repos can hide paths on this site

Any other repo of mine with GitHub Pages turned on is served at
`natasharw.github.io/<repo-name>/`, and that wins over a folder of the same
name here. Until 3 October 2026 the old `natasharw/legal` repo still had Pages
on, so it owned `/legal/` and every page added here after 14 September
(Feeling Wheel support, In Your Own Words) returned 404.

So if a page here 404s, check whether a repo with that name still has Pages
on. To move an old repo's URLs into this site, add the redirect stubs here
first, then turn off Pages on the old repo.

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
`<app>-support.html` naming, then in `index.html`:

1. Copy an existing `<li class="app">` row in the "More apps" list (or a
   `<article class="trail">` card for a trail app) and change the name, description,
   store links and `data-shots`.
2. Add the icon and three screenshots to `assets/apps/` as
   `<app>-icon.webp` and `<app>-shot0.webp` to `-shot2.webp`. The App Store
   serves resized copies, e.g. swap the end of a screenshot URL for
   `600x0w.webp` (icons `256x0w.webp`).
3. Add the privacy and support links to the footer list.

The page is light mode only, on purpose.
