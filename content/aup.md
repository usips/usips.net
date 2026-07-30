+++
title = "Acceptable Use Policy"
description = "The USIPS Acceptable Use Policy: permitted use, prohibited use, enforcement, emergency action, and appeals."
template = "page.html"

[extra]
doc_id = "USIPS-NET-003"
effective = "2026-07-30"
revised = "None"
owner = "J. Moon, President"
review = "Annual"
+++

## 1. Background and purpose

The United States Internet Preservation Society operates network infrastructure and Internet number resources in furtherance of its 501(c)(4) purpose. This policy states what the USIPS network may and may not be used for, and exactly what happens when it is misused. It is written to be predictable: a customer, peer, or complainant reading this page should be able to forecast our response before contacting us.

## 2. Scope

This policy applies to all traffic originating from, destined to, or transiting USIPS-operated infrastructure and USIPS-held address space, whether the interconnection is direct or indirect. It binds USIPS customers and, through them, every device and party a customer permits to use the service, including the customer's own downstream customers, employees, and third parties. Each downstream agreement flows this policy down by contract.

## 3. Permitted use

The USIPS network may be used for any lawful purpose. Use must not:

- interfere with the operation of the network or with other customers' use of it;
- violate the acceptable use policies of networks the traffic transits; or
- use another provider's services to circumvent the intent of this policy.

## 4. Prohibited use

The following are prohibited without exception:

- Child sexual abuse material (CSAM) and nonconsensual intimate imagery (NCII)
- Unsolicited bulk email (spam) and phishing
- Malware distribution and command-and-control infrastructure
- Botnet operation and DDoS-for-hire services
- Operating open resolvers, open amplifiers, or other reflection/amplification infrastructure
- Source address spoofing
- Announcing address space without authorization from its registrant, including announcements under forged Letters of Authorization

## 5. Enforcement

- **Enforcement officer.** Interpretation and enforcement of this policy rest with Joshua Moon, President.
- **Initiation.** Enforcement begins on receipt of a complaint or on direct detection.
- **Notice.** The customer's administrative contact receives written notice identifying the activity and the required remediation.
- **Remediation window.** Two business days, or sooner where the law or an emergency requires.
- **Remediation standard.** The activity has ceased and is not likely to recur.
- **Graduated ladder.** Notice, then a remediation window, then filtering or rate-limiting, then null route, then suspension, then termination. Enforcement starts at the rung proportionate to the harm; CSAM, NCII, and active network attacks start at immediate technical action under § 6.

Every enforcement action is documented, and the complainant receives a written disposition per the [Abuse Policy](/abuse/).

## 6. Emergency action

Where inaction risks critical harm to the network or serious legal liability, USIPS may filter or null route traffic immediately and without prior notice. Emergency authority rests with the President or, where time is of the essence, the enforcement officer acting alone. Every emergency action is reviewed by the officers after the fact, and emergency measures expire fourteen days after imposition unless renewed in writing by the enforcement officer.

## 7. Non-customer traffic

USIPS reserves the right to block or filter traffic originating from or destined to a third party engaged in activity prohibited by this policy, even where that party is not a USIPS customer, to protect the network and its users.

## 8. Appeals

A party subject to enforcement may appeal in writing to an officer not involved in the initial decision, and from that officer to the USIPS board. Appeal contact: <noc@usips.net>, subject line beginning `[APPEAL]`. The appeal decision is issued in writing.

## 9. Amendment

This policy is amended only by resolution of the USIPS board. The effective and revision dates in the register block above are the authoritative version record.

## 10. Operating commitments

These commitments are the positions of the organization applied to its own network, stated here so counterparties know our termination triggers in advance.

> **We carry lawful traffic without regard to viewpoint.** USIPS does not terminate or degrade service over lawful speech, political position, or third-party pressure campaigns. Our termination triggers are the prohibited-use list in § 4 and nonpayment. There are no others.

> **We act decisively on the short list of things that are actually illegal.** CSAM, NCII, and active network abuse receive immediate action under § 6. The list is short, firm, and published; that is what makes the first commitment credible rather than reckless.

> **Enforcement is graduated, documented, and appealable.** Customers receive notice and a remediation window except in defined emergencies. This is the due process USIPS demands of other infrastructure operators, applied to ourselves.

> **Every obligation flows downstream by contract.** Each downstream maintains an AUP no less restrictive than this one, designates its own DMCA agent, registers with NCMEC where applicable, operates a monitored abuse contact, and warrants the accuracy of its Whois reassignment data.
