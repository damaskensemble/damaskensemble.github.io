# Damask — vocal quartet website

A Jekyll site for GitHub Pages. Structural approach borrowed from
[sylvyanscombe.com](https://www.sylvyanscombe.com/) — flat, minimal
layouts, a single-row nav, and a dated collection (`_notices/`, standing
in for that site's `/backpages/`) for chronological items instead of a
conventional blog. Visual identity (palette, type, content) is themed
after [damaskquartet.com](https://damaskquartet.com).

## Structure

```
_config.yml         site settings, nav, ensemble member data
_layouts/           default.html (shell), page.html, home.html, notice.html
_includes/          nav.html, footer.html, members.html
_sass/_base.scss    all styling — palette, type, components
assets/css/         style.scss imports _sass/_base.scss
_notices/           one file per event/news item (sorted by date on /events/)
index.md            home page
about.md            English bio
fr.md                French bio
repertoire.md       repertoire page
events.md           lists the _notices collection
listen.md           video/audio page
o-schone-nacht.md   album page
contact.md          contact page + form
```

## Running locally

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Deploying to GitHub Pages

1. Push this repo to GitHub (public repo, or Pro/Team/Enterprise for
   private).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, choose either:
   - **Deploy from a branch** → branch `main`, folder `/ (root)` — the
     simplest option, since this repo already uses the `github-pages`
     gem, which matches what GitHub's own builder uses.
   - **GitHub Actions** — if you'd rather use a custom workflow (needed
     if you add plugins outside the `github-pages` gem's supported
     list).
4. If you're using a custom domain, add it in the Pages settings and
   update `url:` in `_config.yml` to match. Otherwise leave
   `url: https://<username>.github.io` and set `baseurl: ""` for a user
   site, or `baseurl: "/<repo-name>"` for a project site.

## Adding content

- **Events** — one file per event in `_notices/`, named
  `YYYY-MM-DD-short-title.md`, with `title`, `date`, `venue` and
  `excerpt` in the front matter. `/events/` lists them (upcoming and
  past) automatically. The collection is empty for now: the draft's
  three sample events were invented and have been removed.
- **Member portraits** — add `photo: "/assets/images/<file>.jpg"` to a
  member in `_config.yml`; without it only the name and voice show.
- **Not yet on the site** (removed placeholders, to restore when real
  material exists): a Listen page with video embeds (see git history
  for `listen.md`), a "Buy the album" link, and a contact form (needs a
  form backend such as Formspree, since GitHub Pages is static).
