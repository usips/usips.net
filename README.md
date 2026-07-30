# usips.net

Network operations site of the United States Internet Preservation Society. A minimal, NOC-oriented documentation site: legal identity, network facts, acceptable use, abuse handling, legal process, and retention. The advocacy and membership site is [usips.org](https://usips.org) ([usips/usips.org](https://github.com/usips/usips.org)).

Built with [Zola](https://www.getzola.org/) 0.22. No JavaScript, no third-party resources, every page under the 14KB TCP initial congestion window.

## Development

```bash
zola serve    # dev server at http://127.0.0.1:1111
zola build    # build to public/
zola check --skip-external-links
```

No npm step; the site has no JavaScript.

## Structure

- `content/`: one Markdown file per document (see the register below)
- `templates/`: Tera templates (`base.html`, `page.html`, `index.html`, `404.html`)
- `sass/`: `_tokens.scss` (USIPS design tokens, USWDS model) and `main.scss`
- `static/`: fonts, favicons, `CNAME`, `.nojekyll`, `.well-known/security.txt`

## The document register

Every policy page is a filed document. Front matter carries the record:

```toml
[extra]
doc_id = "USIPS-NET-003"
effective = "2026-07-30"
revised = "None"
owner = "J. Moon, President"
review = "Annual"
```

When a policy changes: update `revised`, and keep the register table on `content/_index.md` in sync. Amendments to the AUP and privacy policy are by board resolution.

**Consistency rule:** contact address strings (`abuse@usips.net`, etc.) must match character for character across this site, ARIN Whois, PeeringDB, security.txt, and the Copyright Office designated-agent record. When changing one, change all.

## Deployment

GitHub Actions builds and deploys to GitHub Pages on push to `master` (`.github/workflows/github-pages.yml`, official Pages actions). In the repository settings, under Pages, set the source to "GitHub Actions" and the custom domain to `usips.net`. Canonical URLs are without `www`. `static/.well-known/security.txt` has an `Expires:` field that must be refreshed before 2027-07-30.
