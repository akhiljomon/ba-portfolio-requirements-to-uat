# 5. Process Maps

## As-is: counter ordering at peak

```mermaid
flowchart TD
    A([Customer arrives]) --> B[Joins counter queue]
    B --> C{Queue longer<br/>than ~10 min?}
    C -- Yes --> D([Customer leaves: lost sale])
    C -- No --> E[Orders at counter]
    E --> F[Counter staff key order into POS]
    F --> G[Customer pays at counter]
    G --> H[Ticket prints at bar]
    H --> I[Barista makes drink]
    I --> J[Barista calls out name]
    J --> K([Customer collects])
```

**Pain points found in observation and interviews**

1. Queue time drives walk-outs (step C).
2. Staff time at peak goes to taking orders and payments (steps E to G), not making drinks.
3. Called-out names are missed in a noisy store, leading to drinks left on the counter.

## To-be: click-and-collect through the app

```mermaid
flowchart TD
    A([Customer opens app]) --> B[Selects store and confirms it]
    B --> C[Builds and customises order]
    C --> D[Chooses pickup slot]
    D --> E{Slot full?}
    E -- Yes --> D
    E -- No --> F[Pays in app]
    F --> G{Payment approved?}
    G -- No --> H([Shown 'Payment declined'; no order sent])
    G -- Yes --> I[Order sent to store screen]
    I --> J{Store acknowledges<br/>within 2 min?}
    J -- No --> K([Automatic refund and customer notified])
    J -- Yes --> L[Labels print at bar]
    L --> M[Barista makes order]
    M --> N[Barista taps Ready]
    N --> O[Push notification to customer]
    O --> P[Customer collects from pickup shelf]
    P --> Q[Order marked collected; loyalty points added]
```

## Gap analysis

| Area | As-is | To-be | Change needed | Requirement |
|------|-------|-------|---------------|-------------|
| Ordering | Counter only | App ordering ahead | App ordering flow | FR-01 to FR-05 |
| Payment | At counter | In app before arrival | Gateway integration | FR-05, NFR-03 |
| Bar workload | Unplanned peaks | Capped per slot | Slot throttling | FR-07 |
| Order handover | Name called out | Push notification, pickup shelf | Ready notification, shelf | FR-08 |
| Failure handling | Not applicable | Automatic refund | Acknowledgement timer | FR-10, NFR-04 |
| Measurement | Manual estimates | Daily report | Reporting | FR-12 |
