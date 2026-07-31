# CLAUDE.md

Guidance for Claude Code when working in this repository.

## What this is

usips.net is the network operations site of the United States Internet Preservation Society (USIPS), a 501(c)(4) nonprofit, EIN 33-2907939. Audience: risk officers at upstream ISPs, peering coordinators, abuse desks, and law enforcement. It complements the advocacy site usips.org (`../usips.org/`), which owns the brand design system this site's tokens derive from.

Zola 0.22 static site. **No JavaScript. No third-party resources.** Design goal: boring, technical, deliberate. A filed document, not a marketing page.

## Commands

```bash
zola serve                        # dev at http://127.0.0.1:1111
zola build                        # build to public/
zola check --skip-external-links  # validate internal links
```

For a local visual check, build with an explicit base URL first; the config base_url is absolute and a plain `zola build` output will not style locally: `zola build --base-url http://127.0.0.1:PORT --output-dir <tmp> --force`.

## Workflow rules

1. **Do not commit or push unless Josh explicitly asks.** Prepare changes and report; he decides when history gets written.
2. `docs/` is untracked working material (the MVP spec and compliance reference). Read it for context; never commit it.

## Writing style

1. **No em dashes, anywhere.** Not in page copy, front matter, code comments, README, or this file. Use a colon, comma, semicolon, parentheses, or a new sentence. Also no arrow-chain sequences in prose; write "then". These are AI-authorship tells and Josh screens for them.
2. Empty table cells and null register values: use `n/a` in table cells, `None` for the register `revised` field.
3. Page title separator is `|` (set in templates).
4. Voice: plain, declarative, operator-to-operator. Short sentences. No marketing adjectives, no "robust", no "comprehensive".

## Hard rules

1. **FTC Act § 5 discipline: never publish a capability that is not actually performed.** Targets, logging practices, and enforcement mechanics must describe reality. Do not "improve" policy text into claims the organization cannot instrument. The only published target is human acknowledgment of abuse reports within 24 hours.
2. **Pending content is commented out, not shown as "pending".** Things USIPS does not have yet live in `<!-- Restore when real: ... -->` HTML comments in the content files. Currently commented out: IRR as-set and MANRS rows plus PeeringDB, IXP, and looking glass rows (`content/network.md`), and the role-address PGP section (`content/contact.md`). Uncomment and fill in as each becomes real. The exception is the ASN and the ARIN transfers: those are stated as pending in visible text because counterparties need the status.
3. **Consistency:** address strings (`abuse@usips.net` etc.), the EIN, ARIN handles, and the DMCA agent record must match character for character everywhere they appear (site, ARIN Whois, PeeringDB, security.txt, Copyright Office record). The DMCA agent block in `content/legal.md` must match the Copyright Office registration exactly; do not reformat it.
4. **The document register:** every policy page carries `[extra]` front matter (`doc_id`, `effective`, `revised`, `owner`, `review`). On any substantive content change, set `revised` and mirror it in the register table in `content/_index.md`. AUP and privacy amendments require a board resolution; flag, don't freelance.
5. **Page weight:** every HTML page stays under 14KB (TCP initial congestion window). CI warns on breach.

## Facts not recorded elsewhere

- Role addresses are @usips.net, forwarded to @usips.org mailboxes. Officer personal addresses: moon@, crawley@, hardin@ (all @usips.org), keys on the usips.org board page.
- The DMCA agent record in `content/legal.md` is Matthew Hardin's law office as registered with the Copyright Office.
- `23.164.216.0/24` is currently announced by AS397702 (the current registrant, 1776 Solutions, LLC). `2607:46C0::/32` is not announced. Verified 2026-07-30 via RIPEstat.
- Values Josh has not yet supplied: registered agent name and address (row intentionally absent from `/organization`), role-address PGP keys, NCMEC ESP registration completion date, ASN.
- Whether every role address is actually delivered to multiple officers is unverified; `/contact` currently claims it. Confirm with Josh before launch.
- Two more published claims to verify against the real mail setup before launch: `/contact` says untagged subject lines "may be rejected by the mail server" (Josh's addition; contradicts `/abuse` and RFC 2142 expectations for automated reports if enforced on abuse@), and `/legal` says the FAQ "serves as the first-tier response sent from our intake addresses" (no autoresponder exists yet).

## Current state (2026-07-30)

Pre-operational: no ASN yet; prefixes `2607:46C0::/32` and `23.164.216.0/24` are registered to 1776 Solutions, LLC, in ARIN transfer to USIPS (donation). When issuance lands: update `/network`, the `/abuse` inventory, the landing facts table, and the header `ASN:` line in `templates/base.html`, and restore the commented-out rows as each artifact (as-set, PeeringDB, looking glass, MANRS) exists.

## Structure

- `content/*.md`: one file per document; front matter uses `template = "page.html"` plus the register block
- `templates/`: `base.html` (header/nav/footer), `page.html` (register block), `index.html`, `404.html`
- `sass/_tokens.scss`: USIPS design tokens (USWDS model, subset of usips.org `themes/usips/sass/_variables.scss`)
- `sass/main.scss`: the entire stylesheet. The header is text-only; `static/logo.small.png` is used solely as the faint `.page-content::before` watermark seal at the foot of each page, with matching reserved padding (Josh's placement; do not re-add the logo to the header, he rejected that twice)
- `static/.well-known/security.txt`: RFC 9116; `Expires:` must be refreshed annually (currently 2027-07-30)
