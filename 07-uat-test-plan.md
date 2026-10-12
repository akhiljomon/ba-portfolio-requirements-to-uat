# 7. User Acceptance Testing (UAT) Plan

## Purpose

Confirm, with real users, that click-and-collect meets the agreed business requirements before
rollout to all 40 stores.

## Scope

All **Must** and **Should** requirements (FR-01 to FR-12, NFR-01 to NFR-06), tested end to end
from the customer app to the store screen. Load testing (NFR-07) is covered by the vendor's
performance testing, not UAT.

## Approach

- Test cases are derived directly from the acceptance criteria in [04-user-stories.md](04-user-stories.md).
- Executed in a pilot store outside trading hours with real devices, the production-like test
  environment and the payment gateway's test mode.
- Testers: two store managers, three baristas, and four customer volunteers from the loyalty programme.
- Defects are logged with steps to reproduce, expected vs actual result, and severity.

## Entry criteria

- System testing complete with no open Critical defects
- Test environment connected to the pilot store's screen and printer
- Test data loaded: menu, store hours, slot capacities, test customer accounts and test cards

## Exit criteria

- 100% of Must test cases executed and passed
- No open Critical or High defects
- Medium defects have an agreed fix date or a documented workaround signed off by the sponsor

## Severity definitions

| Severity | Meaning |
|----------|---------|
| Critical | Customer charged incorrectly, data exposed, or ordering unusable |
| High | A Must requirement fails with no workaround |
| Medium | Requirement partly fails, workaround exists |
| Low | Cosmetic or wording issue |

## Roles

| Role | Responsibility |
|------|----------------|
| Business analyst | Plan UAT, write test cases, facilitate sessions, log and triage defects, report results |
| Store managers and baristas | Execute store-side test cases, confirm operational fit |
| Customer volunteers | Execute app-side test cases |
| Vendor | Fix defects and support retesting |
| Head of Operations | Sign off UAT exit |

## Results summary (cycle 1)

| Measure | Result |
|---------|--------|
| Test cases executed | 17 of 17 |
| Passed | 14 |
| Failed | 3 (TC-05, TC-07, TC-17) |
| Defects raised | 3 (1 High, 1 Medium, 1 Low) |
| Exit criteria met | No: High defect DEF-01 open |

After fixes for DEF-01 and DEF-02 and a retest in cycle 2, all Must test cases passed and the exit
criteria were met. DEF-03 (Low, on a Should requirement) was accepted by the sponsor for the next
release with a documented workaround. See [uat-test-cases.csv](uat-test-cases.csv) and
[defect-log.csv](defect-log.csv).
