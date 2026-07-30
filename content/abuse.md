+++
title = "Abuse"
description = "How to report abuse to USIPS, what we log, and the written disposition every report receives."
template = "page.html"

[extra]
doc_id = "USIPS-NET-004"
effective = "2026-07-30"
revised = "None"
owner = "J. Moon, President"
review = "Annual"
+++

This page is built around what you, the reporter, get back. Every report enters a documented process and exits with a written disposition. Where the answer is no action, the disposition states why, and what we can offer instead. You do not need us to agree with you to close your ticket.

## Address inventory

What runs where, so you can identify what you are looking at before writing to us.

| Range | Service | Ports | Notes |
|---|---|---|---|
| `2607:46C0::/32` | None; not announced | n/a | ARIN transfer to USIPS in progress |
| `23.164.216.0/24` | Operated by current registrant | n/a | Announced by AS397702; ARIN transfer to USIPS in progress |

USIPS does not yet operate these ranges. Reports about current activity in them belong with the abuse contact published in ARIN Whois for the registrant of record. This table is revised as USIPS services turn up, with each service listed against its range and ports.

## What we log

Before you write, know what we can and cannot tell you. USIPS retains flow-level operational telemetry for up to 30 days, aggregate traffic rollups for up to one year, and anonymous counters indefinitely. We do not capture packet payloads and we do not inspect content. USIPS cannot identify an individual end user of a downstream network from an IP address and a timestamp; what flow records can establish, for up to 30 days, is which interconnection or downstream network carried the traffic. The full schedule is in the [Privacy & Retention policy](/privacy/).

## How to report

- **Address:** <abuse@usips.net>
- **Include:** the IP address(es) involved, timestamps with time zone, and evidence (logs, headers, or samples). Reports without timestamps usually cannot be investigated.
- **Formats:** plain email, [ARF](https://datatracker.ietf.org/doc/html/rfc5965), and [X-ARF](https://github.com/abusix/xarf) are accepted.
- **Acknowledgment:** a human reads and answers every report within 24 hours, barring exceptional circumstances. There is no unmonitored queue behind this address.

## Disposition matrix

Every report resolves into one of the following categories. The right-hand column is what you receive in writing.

| Category | Our action | What the reporter receives |
|---|---|---|
| CSAM | Immediate removal or null route. NCMEC CyberTipline report. Evidence preservation. | Confirmation that action was taken. No further detail. |
| NCII (valid removal request) | Removal within 48 hours; reasonable efforts against identical copies. Intake: <ncii@usips.net>. | Confirmation and case reference. |
| Network abuse from a downstream (spam, scanning, DDoS, malware, C2) | Forwarded to the downstream with a remediation deadline; [AUP](/aup/) enforcement ladder on non-compliance. | Case reference, the deadline set, and a closure notice with the outcome. |
| Network abuse from USIPS infrastructure | Direct remediation. | Confirmation and a remediation summary. |
| DMCA notice against transit traffic | § 512(a) conduit; no takedown obligation exists. Forwarded to the downstream where identifiable; counted toward repeat-infringer assessment. | Written statement of our conduit posture and confirmation of forwarding. |
| DMCA notice against hosted content | § 512(c) process: takedown, notice to the subscriber, counter-notice handling. (USIPS hosts no content at present.) | Standard § 512 correspondence. |
| Complaint about lawful content | **No action.** | Written statement that the content is lawful, that USIPS does not remove lawful content, and that USIPS is not the publisher; referral to the host or publisher. |
| Request for subscriber identity without legal process | **No action.** | Pointer to the [legal process table](/legal/), naming the process type required for the data sought. |
| Request for data that is not retained | **No action possible.** | Written statement of what is not retained, plus the standing offer below. |
| Traffic you do not want to receive | Filtering of your prefixes at our edge, on request. | Confirmation of the block and its scope. |

## The standing offer

> If you do not wish to receive traffic from our network, send us the address ranges you control and we will filter traffic toward them at our edge. We will confirm in writing when the filter is in place.

This offer stands regardless of the disposition of the underlying complaint.

## Out of scope

- We do not operate mail services. Direct spam complaints to the operator identified in the message headers.
- USIPS ranges are network infrastructure and transit; we do not host end-user content at present.
- We do not operate the services reachable through our downstreams. Their abuse contacts are published in ARIN Whois; where a reassignment exists, it is SWIP'd and the responsible party is identifiable there.

## Targets

USIPS publishes only targets it actually operates. Today that is one: **human acknowledgment of every abuse report within 24 hours, barring exceptional circumstances.** Numeric resolution targets by severity class will be published here when, and only when, they are instrumented and measured.
