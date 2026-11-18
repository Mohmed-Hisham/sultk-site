# sultk.me

The public website for the Sultk app: a home page, the privacy policy and the delete-account page, in English and Arabic.

- Plain HTML and one CSS file (`assets/site.css`). No JavaScript, no cookies, no analytics, no web fonts.
- One page per language. The Arabic pages are under `/ar/` with `dir="rtl"`.
- The facts come from `../docs/privacy-data-facts.md`. When that file changes, change these pages and the "Last updated" date.
- Hosted on Cloudflare Pages only (project `sultk-site`, no build, output = the repo root). A push to `main` deploys it. `_headers` sets the security headers.
- GitHub Pages is not used. Do not add a `CNAME` file.

## Before publishing

This must print nothing (no placeholders left):

    grep -rn "{{" --include=*.html .

## Preview

    python3 -m http.server 8791 --bind 127.0.0.1

Then open http://localhost:8791.
