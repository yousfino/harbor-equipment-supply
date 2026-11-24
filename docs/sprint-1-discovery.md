# Sprint 1 discovery

Draft for the fictional Harbor Equipment Supply client. See the [project brief](ERP_Project_Brief.md) for release scope.

## Current workflow

| Step | Owner | Record |
|---|---|---|
| Receive request and confirm quantity and delivery date | Maya, sales | Customer email, inventory spreadsheet, sales spreadsheet |
| Allocate and pick stock | Omar, warehouse | Paper pick list. On-hand spreadsheet is updated when stock ships. |
| Handle shortage | Omar reports the shortage. Maya negotiates a split shipment. | Phone and customer communication |
| Invoice after shipment confirmation | Accounting | Separate invoicing system |

## Proposed sandbox workflow

Record supplier receipts and customer orders in Business Central. Check stock for the requested date before confirming an order, and use the same sales order for shipping and invoicing. For the demo, assume the sales team commits stock on confirmation, records customer consent for split delivery, and invoices shipped quantities only.

## Pending decisions

| Decision | Proposed approver | Status |
|---|---|---|
| When to commit stock and who may release or override it | Owner with sales and warehouse leads | Pending |
| Who authorizes partial shipments and confirms the backorder date | Owner with sales and warehouse leads | Pending |
| Whether Business Central replaces current invoicing at launch, and which opening balances and open invoices to migrate | Owner with accountant | Pending |

## Acceptance scenarios

| Test | Expected result |
|---|---|
| Purchase and receive 10 units, then ship and invoice three | Inventory rises by seven from its starting balance. Posted quantities and ledger entries reconcile. |
| Start with 15 on hand and six committed at one location. A second customer requests 12 by Thursday, with no inbound supply before then. | Sales sees nine available before confirming. After simulated customer consent, ship and invoice nine. Three remain open for the second customer and six stay committed to the first. |

Record actual results and document references during sandbox testing. Client approval and execution of both tests are pending.
