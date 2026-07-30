+++
title = "Privacy & Retention"
description = "What USIPS logs, how long it is retained, what is never collected, and how to make a data subject access request."
template = "page.html"

[extra]
doc_id = "USIPS-NET-006"
effective = "2026-07-30"
revised = "None"
owner = "J. Moon, President"
review = "Annual"
+++

This policy covers the USIPS network and this website. The retention schedule below is the load-bearing element: it states both what USIPS can produce and what it cannot, because what is not retained cannot be produced by anyone, about anyone, through us.

## Retention schedule

| Category | Contents | Retention | Deletion |
|---|---|---|---|
| Flow-level telemetry | Source and destination addresses, ports, protocol, byte and packet counts, timestamps, interface; no payloads | Up to 30 days | Automatic, rolling |
| Aggregate rollups | Per-prefix and per-interface traffic totals derived from flow data; no complete flow tuples | Up to 1 year | Automatic, rolling |
| Anonymous counters | Interface and service totals containing no addresses | Indefinite | n/a |
| Abuse and legal correspondence | Reports received, dispositions issued, enforcement records | Retained as organizational records | Per record schedule |

> USIPS cannot identify an individual end user of a downstream network from an IP address and a timestamp. Flow records, while they exist, attribute traffic to an interconnection or a downstream network, not to a person. After 30 days, that attribution is gone too.

## What is never collected

- Packet payloads or application content
- Browsing histories, DNS query logs, or any per-user activity records of end users
- Directories of downstream networks' subscribers

## Legal hold

A litigation hold or a preservation request under 18 U.S.C. § 2703(f) suspends the retention schedule for the specific records it identifies. Held records are segregated, access-restricted, and deleted when the hold lapses. A hold does not create records that do not exist, and does not extend collection going forward.

## Data subject requests

Requests under state comprehensive privacy laws are taken at <privacy@usips.net>. Note the practical scope: for network traffic, USIPS holds no records that identify an individual, so most requests resolve to a written statement of that fact, which we provide.

## Third parties

No third party has routine access to USIPS operational logs. Records leave USIPS in exactly two ways: in response to valid legal process, per the [Legal FAQ](/legal/), or as statutorily required reports (NCMEC CyberTipline). USIPS does not sell, rent, or share operational data.

## This website

usips.net is a static site. It sets no cookies, runs no analytics, and loads no third-party resources. It is served by GitHub Pages, which maintains standard access logs subject to [GitHub's privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

## Changes

Amendments are made by board resolution and recorded in the register block above and in this site's public revision history.
