# nv-portfolio-web

Personal website of **Nikunj Vasava**, built with the [Zola](https://www.getzola.org/)
static site generator. Minimal, fast, and inspired by the bearblog aesthetic
(à la [mrkaran.dev](https://mrkaran.dev/)).

## Getting started

Install Zola (already installed on this machine via Homebrew):

```sh
brew install zola
```

Run a local dev server with live reload:

```sh
zola serve
```

Then open <http://127.0.0.1:1111>.

Build the static site into `public/`:

```sh
zola build
```

## Project layout

```
config.toml          # Site config: title, menu, feed, syntax highlighting
content/
  _index.md          # Homepage intro (edit this first)
  posts/             # Blog posts (one Markdown file each)
  projects/_index.md # Projects list (edit the [extra.projects] entries)
  contact.md         # Contact page
templates/           # HTML templates (Tera)
static/
  css/main.css       # Styles (light + dark via prefers-color-scheme)
  favicon.svg
```

## What to edit

1. **`config.toml`** — set `base_url` to your real domain, and fill in the
   `[extra]` social/email links so they appear in the footer.
2. **`content/_index.md`** — your homepage intro.
3. **`content/projects/_index.md`** — your projects (`[[extra.projects]]` blocks).
4. **`content/contact.md`** — your contact details.
5. **`content/posts/`** — delete `hello-world.md` and add your own posts.
6. Optionally add a `static/images/avatar.jpg` and reference it on the homepage.

## Deploy

`zola build` outputs a fully static site to `public/`. Host it anywhere —
GitHub Pages, Cloudflare Pages, Netlify, or your own server behind Caddy/nginx.
Remember to set `base_url` in `config.toml` to your production URL first.