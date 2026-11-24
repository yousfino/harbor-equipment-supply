# Harbor Equipment Supply — ERP Project Brief

**Status** Draft for client review · **Platform** Microsoft Dynamics 365 Business Central  
**Sponsor** Company owner · **Delivery lead** Solo ERP consultant

### Business problem

Harbor is a 20-person equipment distributor with one warehouse. Sales tracks orders in spreadsheets, the warehouse records allocations on paper, and accounting invoices in a separate system. In a recent order, sales saw 15 pumps on hand and promised 12 by Thursday. Six had already been set aside for another customer, leaving only nine to ship.

### Objective and proposed scope

Give sales visibility into available stock before promising delivery, and let sales, warehouse, and accounting work from the same order. The proposed first release covers supplier purchases and receipts, inventory and stock commitments at one warehouse, sales orders, full and partial shipments, and invoicing. Rehearse migration of item, customer, and vendor records, opening stock, and open orders. Confirm the accounting cutover with the accountant before committing to go-live.

Configure standard Business Central workflows first. Document any gaps and build AL extensions for company-specific requirements the owner approves. The React dashboard, multi-warehouse operations, and historical transaction migration are proposed for later consideration.

### Delivery and sign-off

| Milestone | Deliverable and review |
|---|---|
| Scope agreement | Process map, prioritized requirements, and acceptance criteria reviewed by the owner. |
| Sandbox demo | Configured purchase-to-receipt and order-to-invoice workflows with representative data. Sales and warehouse review stock availability and partial shipments. |
| Acceptance and handover | Migration rehearsal, user acceptance tests, training, and a cutover and support plan. The owner signs off after sales, warehouse, and accounting verify their workflows. |

The consultant owns configuration, development, documentation, demos, and testing. This public portfolio repository tracks requirements, decisions, test scripts, and any AL source. The owner approves scope changes and go-live.

### Primary acceptance scenario

With 15 pumps on hand, six already committed, and no incoming stock before Thursday, sales sees **nine available for Thursday** before confirming a request for 12. If the customer agrees to a partial shipment, warehouse ships nine, accounting invoices those nine, and three remain open on the order.

### Decisions to confirm

- When does an order commit stock, and who can override or release that commitment?
- Who approves partial shipments and confirms a date for the remaining units?
- Will Business Central replace the current invoicing system at launch? What opening balances and outstanding invoices must carry over?