# Core Data Modules

Customer
- id, identity/auth, profile, contacts, addresses, preferences, tags, loyalty/store credit

MeasurementProfile
- id, customer_id, profile_name, version, measurements, fit notes, created_at, supersedes_version

Product / Variant
- id, SKU, category, collection, media, options, price, tax, stock policy, customization rules

Cart / Wishlist
- customer-owned only

Order
- id, customer_id, items, customization snapshot, measurement_version_id, totals, tax, status,
  promised_date, payment_status, shipping_status

Payment / Refund
- gateway reference, order, amount, status, receipt, reconciliation metadata

ProductionJob
- order/item, assigned staff, stage, timestamps, SLA/deadline, notes, QC state

Inventory
- item/SKU/raw material, warehouse, movement, reservation, reorder level, costing

CRM Lead / Opportunity
- source, customer/lead, stage, follow-up, owner, campaign, conversion/lost reason

Support / Alteration / Return
- order-linked case, reason, evidence, status, resolution, financial impact

AuditEvent
- actor, action, entity, before/after reference, timestamp
