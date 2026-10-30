# Fictional worked example

**All organizations, people, account IDs and tickets below are invented. This is not a real audit or customer case study.**

## Review header

- Review: EX-2026-10-01, v1; system: ExampleCo project tracker, production tenant.
- Scope: every tenant account, including guests and service accounts; no exclusions.
- Review date: 30 October 2026; snapshot: 09:00 UTC that day.
- Owner/approver: Priya (operations lead). Reviewer: Lee (engineering lead). Priya separately reviews Lee's own access.
- Source: private admin account export EX-E01; all-status filter; guest and service-account views checked separately. Six unique IDs in export; six in workbook; no duplicates. Current roster EX-E02 and access approvals EX-E03 used for comparison.
- Policy: fictional internal IAM policy, quarterly review plus event-driven removal. This frequency illustrates ExampleCo's decision, not a framework mandate.

## Decisions and outcomes

| Account | Type / status | Owner | Current access | Decision and rationale | Reviewer / date | Action / evidence | Outcome |
|---|---|---|---|---|---|---|---|
| usr-101 | Human / active | Lee | Admin | Retain: tenant configuration is part of assigned role; approval EX-A01 | Priya / 30 Oct | No change; EX-E03 | Reviewed |
| usr-102 | Human / active | Morgan | Admin | Change to Member: no current administration responsibility | Lee / 30 Oct | EX-T01, Priya, due 30 Oct | Role changed 10:10 UTC; Lee verified via new role export EX-E04 at 10:20 UTC |
| usr-103 | Human / active | Jo (former contractor) | Member | Remove: contract ended 29 Oct; roster EX-E02 | Lee / 30 Oct | EX-T02, Priya, due immediately under fictional policy | Account disabled and sessions revoked 09:35 UTC; Lee verified EX-E05 at 09:45 UTC; retained records per policy |
| gst-104 | Guest / active | Sam; sponsor Priya | One project | Retain: current collaboration through 6 Nov, EX-A04 | Lee / 30 Oct | Set follow-up EX-T03 for 6 Nov | Sponsor to confirm removal or renewed approval on expiry |
| svc-105 | Service / active | Priya | Admin API integration | Investigate: integration exists but minimum required permissions are unconfirmed | Lee / 30 Oct | EX-T04, Priya, due 2 Nov; exception EX-X01 | OPEN; do not disable before dependency check |
| usr-106 | Human / disabled | Alex (former employee) | Member, disabled | Retain disabled state pending scheduled record disposal; check tokens and group grants | Lee / 30 Oct | EX-T05 | Priya confirmed no active sessions, tokens or group grants; Lee verified EX-E06 at 10:30 UTC |

## Open exception EX-X01

Service account svc-105 retains Admin temporarily while its integration permissions are tested. Priya accepts the documented interim risk through 2 November, restricts access to the credential store and reviews integration activity daily. EX-T04 must record the permission test, chosen role and verification. This example does not imply those measures are sufficient for another system.

## Sign-off

Six of six accounts reviewed; two retain active access, one role reduction, one removal, one investigation, one disabled-state validation. The guest expiry is a scheduled follow-up. Service-account remediation remains open.

Lee signs the decisions on 30 October 2026. Priya approves the review with EX-X01 explicitly open and reviews Lee's own access. **Status: review completed; remediation open.** Priya will reassess EX-X01 on 2 November and the guest on 6 November. No claim of full remediation or audit acceptance is made.
