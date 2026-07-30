+++
title = "Network"
description = "USIPS network facts: ASN, originated prefixes, RPKI and IRR posture, peering policy, and Letter of Authorization verification."
template = "page.html"

[extra]
doc_id = "USIPS-NET-002"
effective = "2026-07-30"
revised = "None"
owner = "J. Moon, President"
review = "Annual"
+++

This page is the factual record of the USIPS network for peering coordinators and upstream engineers. It contains no marketing.

> **Status: pre-operational.** USIPS does not yet originate routes. Number resources are in the ARIN transfer process described below. Commitments on this page marked *from turn-up* bind USIPS from the first day of BGP operation.

## Number resources

| Resource | Type | ARIN handle | Status |
|---|---|---|---|
| `2607:46C0::/32` | IPv6 direct allocation | [NET6-2607-46C0-1](https://whois.arin.net/rest/net/NET6-2607-46C0-1) | Registered to 1776 Solutions, LLC; ARIN transfer to USIPS in progress (donation) |
| `23.164.216.0/24` | IPv4 direct allocation | [NET-23-164-216-0-1](https://whois.arin.net/rest/net/NET-23-164-216-0-1) | Registered to 1776 Solutions, LLC; ARIN transfer to USIPS in progress (donation) |
| ASN | n/a | n/a | Pending issuance |

Until the transfers complete, ARIN Whois shows the current registrant of record. The IPv4 range is presently announced by the current registrant under AS397702; the IPv6 range is not announced. This page will be revised the day each record changes, and any other announcement of this space should be treated as suspect and reported to <noc@usips.net>.

## Routing security

| Item | Position |
|---|---|
| RPKI ROAs | Maintained for the prefixes above, authorized under ARIN POC [MOONJ18-ARIN](https://whois.arin.net/rest/poc/MOONJ18-ARIN) (Joshua Moon) |
| Route origin validation | *From turn-up:* ROV enforced at all EBGP borders, RPKI-invalid routes dropped |
| IRR | Route objects maintained in the ARIN IRR |
| Source address validation | *From turn-up:* BCP 38 ingress filtering on all customer edges |

<!-- Restore when real:
| IRR as-set | (publish the as-set name after ASN issuance) |
| MANRS | (add participation entry once listed at manrs.org) |
-->

## Interconnection

| Item | Position |
|---|---|
| Peering policy | **Open.** We peer with any network that maintains accurate Whois and PeeringDB data, publishes a monitored abuse contact, and does not point default |
| Peering requests | <peering@usips.net> |

<!-- Restore rows as each exists:
| PeeringDB | (link the PeeringDB record after ASN issuance) |
| IXPs and facilities | (list each IXP and facility as established) |
| Looking glass | (link after turn-up) |
-->

## Letters of Authorization

- LOAs for USIPS address space are issued **only** by Joshua Moon, President (ARIN POC [MOONJ18-ARIN](https://whois.arin.net/rest/poc/MOONJ18-ARIN)).
- To verify any LOA claiming to cover USIPS space, email <noc@usips.net> with a copy of the document. We confirm or repudiate in writing.
- Report suspected LOA forgeries to <abuse@usips.net>. A forged LOA is treated as an attempted hijack of the address space, per the [Acceptable Use Policy](/aup/).

## Address space leasing

Leasing of USIPS address space is available when applicable to the USIPS mission and as resources permit. Every lease is registered in ARIN Whois via SWIP, carries the [Acceptable Use Policy](/aup/) by contract, and requires a verified legal identity. Space is not leased to parties we cannot identify.
