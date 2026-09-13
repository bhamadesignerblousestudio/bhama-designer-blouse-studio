# COMMERCE MASTER STUDIO — LOCKED MASTER BLUEPRINT v1.0

## Purpose
This folder is the reusable master starting point for BHAMA and future commerce websites.
For a new client/brand, preserve the architecture and replace only brand identity, contact details,
catalog/products, posters, media assets, policy/business data and integration credentials.

## Locked business architecture
Customer-facing commerce + authenticated customer portal + CRM + ERP + production/workflow +
payments + shipping + WhatsApp + automation + analytics.

### Customer rule
Guest checkout is disabled. A customer must register/login before an order can be placed.

### Customer portal
Profile, addresses, saved measurements, measurement version history, uploads/references, wishlist,
cart, active orders, detailed production timeline, courier tracking, purchase history, invoices,
receipts, payment history, balance payments, refunds, returns/exchanges, alteration history,
support tickets, consultation bookings, loyalty/store credit and reorder/review actions.

### Commerce flow
Browse -> Product/Collection -> Login/Register -> Wishlist/Cart -> Size/Measurements ->
Customization -> Address -> Payment -> Order -> Production Tracking -> Shipping Tracking ->
Invoice -> Purchase History -> Alteration/Return/Support -> Reorder/Review.

### Custom-product workflow
Reference upload -> options/configuration -> measurements -> consultation/quote -> approval ->
production -> QC -> trial/alteration if needed -> packing -> shipping/delivery.

### Production status model
Order Confirmed -> Measurement Verified -> Design Approved -> Cutting -> Stitching ->
Handwork/Value Addition -> Finishing -> QC -> Trial -> Alteration -> Ready -> Packed ->
Shipped -> Delivered.

### Admin / ERP / CRM
Products, categories, collections, prices, media, stock, customers, leads, orders, payments,
refunds, measurements, consultations, suppliers, purchases, raw materials, production stages,
staff workload, QC, alterations, GST invoices, expenses, profitability and management reports.

### Integrations
- Source control: GitHub
- Frontend hosting: Cloudflare Pages
- Custom database/auth: Supabase/Postgres
- ERP + CRM backbone: ERPNext
- Payments: Razorpay or Cashfree
- WhatsApp: Meta Cloud API
- Shipping: Shiprocket or equivalent
- Automation: n8n / server functions
- Media: Cloudflare R2 or Supabase Storage

## Source-of-truth rule
Do not manually maintain the same operational data in multiple systems.
Each entity (customer, product, order, payment, stock, measurement, production job) must have a
defined source of truth and integrations must sync automatically.

## Reuse checklist for every new website
1. Duplicate this master repository/folder.
2. Replace brand name, logo, colors, typography and SEO metadata.
3. Replace contact, social, address and policy data.
4. Replace posters, hero/category/product/lookbook/packaging assets.
5. Replace catalog, variants, pricing, tax and inventory rules.
6. Configure login/auth; keep order placement behind login unless the project explicitly changes it.
7. Configure payment, shipping, WhatsApp and email credentials.
8. Configure ERP/CRM company, warehouses, taxes, workflows and roles.
9. Test customer account, checkout, payment callbacks, inventory sync, production tracking,
   invoice generation, shipping tracking, returns/refunds and notifications.
10. Deploy staging, complete acceptance testing, then deploy production.

## BHAMA status
BHAMA is the first reference implementation of this master. Current visual frontend is included.
Backend modules are the locked implementation target and will be connected phase-by-phase.
