+++
title = "Legal"
description = "USIPS legal FAQ and law enforcement guide: safe harbor posture, DMCA agent, and the legal process required for each category of data."
template = "page.html"

[extra]
doc_id = "USIPS-NET-005"
effective = "2026-07-30"
revised = "None"
owner = "M. Hardin, Secretary"
review = "Annual"
+++

Short, declarative answers, in the order a legal or law enforcement reader needs them. This document also serves as the first-tier response sent from our intake addresses.

## What is USIPS?

The United States Internet Preservation Society, a 501(c)(4) nonprofit corporation, EIN 33-2907939. Full legal identity, officers, and independent verification pointers are on the [Organization page](/organization/).

## What does USIPS operate, and why?

USIPS operates Internet number resources and carrier infrastructure in furtherance of its exempt purpose: preserving open, private, and impartial access to the Internet. USIPS is an infrastructure operator. It is not the publisher of the traffic it carries, and it hosts no end-user content at present.

## How do I verify an IP address is USIPS's?

Query [ARIN Whois](https://whois.arin.net/rest/org/USIPS) for Org ID `USIPS`. The authoritative inventory, including ranges currently in ARIN transfer to USIPS, is on the [Network page](/network/). If ARIN Whois and this site disagree, ARIN Whois is authoritative and we would like to hear about the discrepancy at <noc@usips.net>.

## What does USIPS log, and what can it produce?

Flow-level operational telemetry is retained up to 30 days, aggregate rollups up to one year, and anonymous counters indefinitely. Packet payloads and content are not captured. USIPS cannot identify an individual end user of a downstream network from an IP address and a timestamp, and cannot produce records it does not retain. The complete schedule, including what is never collected, is the [Privacy & Retention policy](/privacy/).

## What is USIPS's DMCA safe harbor posture?

For traffic transiting the network, USIPS is a conduit provider under 17 U.S.C. § 512(a): transmissions are initiated by others, carried automatically, and not stored. There is no takedown obligation for conduit traffic, and § 512(h) subpoenas do not reach § 512(a) conduits (*RIAA v. Verizon*, 351 F.3d 1229 (D.C. Cir. 2003)). Should USIPS ever host content, § 512(c) notice-and-takedown will be operated for it; USIPS hosts no content at present.

## What is the repeat infringer policy?

USIPS has adopted, reasonably implements, and hereby communicates a policy under § 512(i)(1)(A): a customer or address-space lessee determined to be a repeat infringer is terminated in appropriate circumstances. DMCA notices concerning downstream networks are forwarded and counted toward that assessment.

## Who is the designated DMCA agent?

As registered with the U.S. Copyright Office:

```
Matthew Hardin
The Law Office of Matthew D. Hardin, PLLC
101 Rainbow Drive #11506
Livingston, TX 77399
Phone: 202-802-1948
Email: matt@matthewhardin.com
```

Notices may additionally be copied to <dmca@usips.net>.

## What legal process is required for what data?

| Data sought | Process required |
|---|---|
| Subscriber records | Subpoena, 18 U.S.C. § 2703(c)(2) |
| Non-content records | Court order, § 2703(d) |
| Content | Warrant, § 2703(a) |
| Preservation | § 2703(f) request; 90 days, one 90-day extension |
| Emergency disclosure | § 2702(b)(8); reviewed by Joshua Moon and Matthew Hardin |

Serve process at <legal@usips.net>, or by mail to United States Internet Preservation Society, 25 1st Ave SW, Ste A, Watertown, SD 57201. Note that most data categories above concern records USIPS largely does not hold; see the retention schedule before drafting process.

## How are requesters authenticated?

Legal process must issue from an identifiable authority, on letterhead or via an official e-service system, from a verifiable official email domain, with a callback number we can independently confirm. We reject facially invalid process, process served on the wrong entity, and requests whose requester cannot be authenticated.

## Does USIPS notify customers of legal process?

Yes. Our standing policy is to notify the affected customer before disclosure unless a court order or statute prohibits it, in which case notice is given when the prohibition lapses.

## What about foreign requests?

Foreign government requests are routed through the MLAT process or a CLOUD Act executive agreement, as applicable. Foreign administrative orders without recognition under United States law receive a written response declining to act.

## What happens to demands without legal force?

They are declined in writing. Informal requests, letters from private parties, pressure campaigns, and foreign orders without US recognition all receive the same response: a written statement that USIPS acts on valid legal process and on its published policies, and on nothing else. We do not volunteer data, and we do not obstruct valid orders. This applies with equal force to demands that we terminate a customer: our termination triggers are published in the [AUP](/aup/), and no demand outside them is actioned.

## What about CSAM?

Apparent CSAM is reported to the NCMEC CyberTipline as required by 18 U.S.C. § 2258A, with preservation as required by § 2258A(h). USIPS conducts no affirmative monitoring of traffic content, consistent with § 2258A(f), and nothing in this document should be read to assume otherwise.

## Commitments

> **We require legal process for anything legal process is required for,** neither more nor less. We do not volunteer data, and we do not obstruct valid orders.

> **We retain minimally and publish what we retain.** What we cannot produce cannot be subpoenaed out of anyone through us. Undisclosed retention is a liability to every network in the chain.

> **We publish our performance only against targets we instrument.** Claims without measurement are theater; see the [Abuse Policy](/abuse/) targets section.
