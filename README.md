# anmol-goyal7.github.io

My personal site, live at **[anmol-goyal7.github.io](https://anmol-goyal7.github.io)**.

A single static page: no build step, no dependencies, no framework. Just HTML with
inline CSS and about 30 lines of vanilla JavaScript.

## Layout

| File | Purpose |
| --- | --- |
| `index.html` | The whole site — markup, styles and the hash router, in one file |
| `404.html` | Not-found page, served automatically by GitHub Pages |
| `resume.pdf` | Linked from the header |

## How it works

The four sections (`about`, `bookshelf`, `setup`, `training`) all live in
`index.html` as `<section class="view">` blocks. A small hash router shows one at a
time and keeps `#about`, `#bookshelf`, `#setup` and `#training` linkable.

With JavaScript disabled, every section renders as one long page — the router
hides sections only after the `js` class lands on `<html>`.

## Running it locally

No toolchain required. Open the file directly:

```bash
xdg-open index.html
```

Or serve it, which is closer to how GitHub Pages behaves (root-relative links and
the 404 page resolve properly):

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>. To check the 404 page, request any path that
doesn't exist.

## Deploying

GitHub Pages serves `main` from the repository root, so a push to `main` is the
deploy:

```bash
git push origin main
```

The site updates within a minute or two.

## License

[MIT](LICENSE) — fork and modify freely, just keep the copyright notice.
