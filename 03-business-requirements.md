# 3. Business Requirements

Priority uses MoSCoW: **M**ust, **S**hould, **C**ould, **W**on't (this release).

## Business requirements

| ID | Requirement | Objective |
|----|-------------|-----------|
| BR-01 | Customers can order and pay ahead through the BrewLine app | OBJ-1, OBJ-2 |
| BR-02 | Stores receive app orders in a form baristas can act on immediately | OBJ-1, OBJ-3 |
| BR-03 | App orders earn loyalty points the same way counter orders do | OBJ-4 |
| BR-04 | The business can measure app order volume, wait time and accuracy | All |

## Functional requirements

| ID | Requirement | Priority | Traces to |
|----|-------------|----------|-----------|
| FR-01 | The app shows the selected store's current menu, prices and item availability | M | BR-01 |
| FR-02 | The customer must confirm the pickup store before payment | M | BR-01 |
| FR-03 | The customer can customise items (size, milk, extra shot, sugar) with price changes shown | M | BR-01 |
| FR-04 | The customer chooses a pickup time in 5-minute slots, from 10 minutes ahead up to store closing | M | BR-01 |
| FR-05 | The customer pays in the app with a saved or new card before the order is sent | M | BR-01 |
| FR-06 | Paid orders appear on the store's order screen and print a label for each item | M | BR-02 |
| FR-07 | Each store can cap the number of app orders per 5-minute slot; full slots cannot be selected | M | BR-02 |
| FR-08 | Staff mark an order "ready", which sends a push notification to the customer | M | BR-01, BR-02 |
| FR-09 | Loyalty points are added to the customer's account when the order is marked collected | S | BR-03 |
| FR-10 | If the store does not acknowledge an order within 2 minutes, the customer is refunded and notified | M | BR-01 |
| FR-11 | The customer can see order status (received, being made, ready, collected) | S | BR-01 |
| FR-12 | A daily report shows app orders, average ready-to-collect time and remakes per store | S | BR-04 |
| FR-13 | The customer can re-order a previous order in two taps | C | BR-01 |
| FR-14 | Scheduling orders for another day | W | - |

## Non-functional requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| NFR-01 | An order reaches the store screen within 10 seconds of successful payment | M |
| NFR-02 | The ordering flow works on the two most recent major iOS and Android versions | M |
| NFR-03 | Card details are never stored by BrewLine; only the payment gateway token is kept | M |
| NFR-04 | Refunds for failed orders are issued automatically within 5 minutes | M |
| NFR-05 | Order and customer data are handled in line with the Australian Privacy Principles | M |
| NFR-06 | The store order screen is readable from 2 metres in bar lighting | S |
| NFR-07 | The system handles 2,000 orders per hour across all stores at peak | S |
