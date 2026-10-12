# 1. Problem Statement and Scope

## Background

*BrewLine Cafés* (fictional) runs 40 cafés across south-east Queensland. Customers already use the
BrewLine app for a points-based loyalty card. Orders are placed only at the counter.

## Problem statement

During the 7:00 to 9:30 am peak, queues at busy stores regularly exceed 10 minutes. Store managers
report customers walking out of the queue, and staff spend peak time taking orders instead of
making drinks. The loyalty app has no way to order ahead.

## Business objectives

| ID | Objective |
|----|-----------|
| OBJ-1 | Reduce average peak-time wait for app customers to under 3 minutes from arrival to collection |
| OBJ-2 | Shift at least 20% of peak orders to the app within 6 months of launch |
| OBJ-3 | Keep order accuracy at or above the current counter level (98%) |
| OBJ-4 | Increase loyalty app monthly active users by 15% |

## Success measures

- Average time from "order ready" notification to collection (from order timestamps)
- Share of peak-period orders placed through the app (POS reporting)
- Order accuracy rate (remakes logged at the bar)
- Monthly active app users (app analytics)

## Scope

**In scope**
- Ordering ahead in the existing loyalty app (menu, customisation, store selection, pickup time)
- In-app payment using the existing payment gateway
- Sending app orders to the store's order screen and printer
- "Order ready" notification to the customer
- Loyalty points earned on app orders

**Out of scope**
- Delivery (third-party or in-house)
- Changes to the counter POS beyond receiving app orders
- Catering and bulk orders
- A web ordering site

## Assumptions

- Stores keep the same menu and pricing as the counter
- The existing payment gateway supports pre-authorised card payments
- Every store has a working order screen and network connection

## Constraints

- Launch before the next financial year so the marketing campaign can run
- No new hardware budget beyond one label printer per store
- Must comply with the Australian Privacy Principles for customer data

## Risks

| ID | Risk | Likelihood | Impact | Mitigation |
|----|------|-----------|--------|------------|
| R-1 | Bar staff overloaded by app orders at peak | Medium | High | Store-level throttling of pickup slots (FR-07) |
| R-2 | Orders sent to the wrong store | Low | High | Clear store confirmation before payment (FR-02) |
| R-3 | Payment taken but order not received in store | Low | High | Order acknowledgement and automatic refund (FR-10, NFR-04) |
