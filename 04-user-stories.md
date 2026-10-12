# 4. User Stories and Acceptance Criteria

Stories follow INVEST. Acceptance criteria use Given / When / Then so they convert directly into
UAT test cases (see [uat-test-cases.csv](uat-test-cases.csv)).

---

### US-01: Choose my pickup store
**As a** BrewLine app customer **I want** to choose which store I'm collecting from **so that** my
order is made where I'll actually be.
*Traces to:* FR-01, FR-02 · *Priority:* Must

- **AC1** Given I open "Order ahead", when I have location turned on, then the nearest three open
  stores are listed with distance.
- **AC2** Given I have selected a store, when I reach the payment screen, then the store name and
  address are shown and I must confirm them before I can pay.
- **AC3** Given a store is closed, when I view the store list, then it is shown as closed and cannot
  be selected.

### US-02: Customise my drink
**As a** customer **I want** to change size, milk, shots and sugar **so that** I get my usual order.
*Traces to:* FR-03 · *Priority:* Must

- **AC1** Given I select an item, when I change an option with a surcharge, then the item price
  updates immediately.
- **AC2** Given an option is unavailable at my store, when I view the options, then it is greyed out
  with the label "Not available today".

### US-03: Pick a collection time
**As a** customer **I want** to choose when I'll collect **so that** my coffee is fresh when I arrive.
*Traces to:* FR-04, FR-07 · *Priority:* Must

- **AC1** Given the time is 7:42 am, when I open the time picker, then the earliest slot offered is
  7:55 am and slots are in 5-minute steps.
- **AC2** Given a slot has reached the store's cap, when I view the time picker, then that slot is
  shown as "Full" and cannot be selected.
- **AC3** Given the store closes at 3:00 pm, when I view the time picker, then the last slot is
  2:55 pm.

### US-04: Pay in the app
**As a** customer **I want** to pay with a saved card **so that** collection is quick.
*Traces to:* FR-05, NFR-03 · *Priority:* Must

- **AC1** Given I have a saved card, when I tap "Pay", then payment completes without re-entering
  card details.
- **AC2** Given payment is declined, when the gateway responds, then I see "Payment declined" and
  no order is sent to the store.

### US-05: See app orders at the bar
**As a** barista **I want** paid app orders on my screen with a printed label per item **so that** I
can make them without re-keying anything.
*Traces to:* FR-06, NFR-01, NFR-06 · *Priority:* Must

- **AC1** Given a customer pays, when payment succeeds, then the order appears on the store screen
  within 10 seconds, sorted by pickup time.
- **AC2** Given an order has three items, when it reaches the store, then three labels print, each
  showing customer first name, item, options and pickup time.

### US-06: Tell the customer it's ready
**As a** barista **I want** to mark an order ready **so that** the customer knows to collect it.
*Traces to:* FR-08, FR-11 · *Priority:* Must

- **AC1** Given an order is on the screen, when I tap "Ready", then the customer receives a push
  notification within 30 seconds.
- **AC2** Given the customer opens the app, when the order is ready, then its status shows "Ready
  for pickup".

### US-07: Get my money back if the store misses my order
**As a** customer **I want** an automatic refund if the store never receives my order **so that** I
don't pay for coffee I won't get.
*Traces to:* FR-10, NFR-04 · *Priority:* Must

- **AC1** Given the store has not acknowledged my order within 2 minutes, when the timer expires,
  then the order is cancelled, a refund is issued, and I am notified.

### US-08: Earn points on app orders
**As a** loyalty member **I want** points for app orders **so that** ordering ahead isn't a penalty.
*Traces to:* FR-09 · *Priority:* Should

- **AC1** Given my order is marked collected, when I view my loyalty balance, then the points for
  that order have been added.

### US-09: Daily app order report
**As a** store manager **I want** a daily report of app orders **so that** I can see how the bar is
coping.
*Traces to:* FR-12, BR-04 · *Priority:* Should

- **AC1** Given it is the next morning, when I open the report, then it shows app order count,
  average ready-to-collect time, and remakes for my store for the previous day.
