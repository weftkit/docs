# weftkit docs

The documentation site for [weftkit](https://github.com/weftkit/weftkit), built with
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) and served at
[weftkit.org](https://weftkit.org).

## Local preview

```sh
python3 -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Then open http://127.0.0.1:8000.

## Deploy (Cloudflare Pages)

The site is hosted on Cloudflare Pages, which rebuilds on every push to the default branch.
Configure the project once with these settings.

- Framework preset: None
- Build command: `mkdocs build`
- Build output directory: `site`
- Environment variable: `PYTHON_VERSION` = `3.12`

Cloudflare installs `requirements.txt` automatically before running the build command. Add
`weftkit.org` under the project's custom domains to serve it on the apex domain.
