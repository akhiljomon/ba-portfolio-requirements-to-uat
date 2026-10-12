# 8. Requirements Traceability Matrix

Every Must and Should requirement traces forward to at least one user story and UAT test case.
Status reflects the end of UAT cycle 2.

| Requirement | Priority | User story | Test case(s) | Defect | Status |
|-------------|----------|------------|--------------|--------|--------|
| FR-01 Store menu and availability | M | US-01 | TC-01 | | Passed |
| FR-02 Confirm pickup store | M | US-01 | TC-02, TC-03 | | Passed |
| FR-03 Customise items | M | US-02 | TC-04, TC-05 | DEF-02 (closed) | Passed in cycle 2 |
| FR-04 Pickup time slots | M | US-03 | TC-06, TC-08 | | Passed |
| FR-05 Pay in app | M | US-04 | TC-09, TC-10 | | Passed |
| FR-06 Orders to store screen and labels | M | US-05 | TC-11, TC-12 | | Passed |
| FR-07 Slot capacity cap | M | US-03 | TC-07 | DEF-01 (closed) | Passed in cycle 2 |
| FR-08 Ready notification | M | US-06 | TC-13 | | Passed |
| FR-09 Loyalty points on collection | S | US-08 | TC-16 | | Passed |
| FR-10 Auto-refund if not acknowledged | M | US-07 | TC-15 | | Passed |
| FR-11 Order status in app | S | US-06 | TC-14 | | Passed |
| FR-12 Daily app order report | S | US-09 | TC-17 | DEF-03 (deferred) | Accepted with workaround |
| FR-13 Re-order in two taps | C | | | | Not in this release |
| FR-14 Schedule for another day | W | | | | Out of scope |
| NFR-01 Order on screen within 10 s | M | US-05 | TC-11 | | Passed (4 s) |
| NFR-03 No card data stored | M | US-04 | TC-09 | | Passed (gateway token only) |
| NFR-04 Refund within 5 minutes | M | US-07 | TC-15 | | Passed |
| NFR-02, NFR-05, NFR-06, NFR-07 | M/S | | | | Covered by vendor device, privacy and performance testing |

## Coverage summary

- **Must functional requirements:** 9 of 9 traced to stories and test cases; all passed by cycle 2.
- **Should requirements:** 3 of 3 traced; one accepted with a documented workaround.
- **Could / Won't:** recorded and explicitly excluded, so scope decisions stay visible.
