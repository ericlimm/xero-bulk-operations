# Xero bulk operations — what Xero can't do in bulk, and how people work around it

A maintained list of the bulk actions Xero does **not** offer natively, with the vote counts on
Xero's own Product Ideas board, the manual workaround for each, and the tools that fill the gap.
Written by the developer of [BulkOps](https://bulkops.microspear.app) (a Xero add-on) — so read
the tool recommendations with that in mind. Corrections and additions welcome via issues or PRs.

| Gap | Product Ideas votes | Status on Xero's board | Manual workaround | Tool |
|---|---|---|---|---|
| Allocate many credit notes to invoices in one go | 480+ (open since 2017) | Accepted, "not planned for the short term" | Open each credit note → Allocate credit → type amounts → save, one at a time | [BulkOps](https://bulkops.microspear.app) — preview, batch run, one-click undo |
| Include credit notes in a batch payment | 920+ | Open | Allocate credit notes first, then batch-pay the remaining balances | [BulkOps batch payment run](https://bulkops.microspear.app/guides/xero-batch-payment-credit-notes) |
| Bulk export / print attached files | 690+ | Accepted, no ETA | Open each document and download each attachment | [BulkOps attachment export](https://bulkops.microspear.app/guides/bulk-export-xero-attachments) (ZIP grouped by document) |
| Bulk archive tracking category options | 150+ | Open | Archive options one by one; 100-option limit per category | [BulkOps tracking archive](https://bulkops.microspear.app/guides/bulk-archive-tracking-categories-xero) |
| Bulk remove / void sales invoices | 250+ | Open | Void one at a time; a free community script (Bulkdozer) exists | — (BulkOps deliberately does not do irreversible actions) |
| Allocate overpayments and prepayments in bulk | (part of the credit note thread) | — | Same one-at-a-time screen as credit notes | [BulkOps overpayment allocation](https://bulkops.microspear.app/guides/bulk-allocate-overpayments-xero) |

## Guides (manual process first, tool second)

- [How to bulk allocate credit notes in Xero](https://bulkops.microspear.app/guides/bulk-credit-note-allocation-xero)
- [How to allocate one credit note to multiple invoices](https://bulkops.microspear.app/guides/allocate-credit-note-to-multiple-invoices-xero)
- [How to remove a credit note allocation (undo a misallocation)](https://bulkops.microspear.app/guides/remove-credit-note-allocation-xero)
- [How to bulk allocate overpayments](https://bulkops.microspear.app/guides/bulk-allocate-overpayments-xero)
- [How to include credit notes in a Xero batch payment](https://bulkops.microspear.app/guides/xero-batch-payment-credit-notes)
- [How to bulk export attachments from Xero](https://bulkops.microspear.app/guides/bulk-export-xero-attachments)
- [How to bulk archive tracking categories and options](https://bulkops.microspear.app/guides/bulk-archive-tracking-categories-xero)
- [Xero's tracking category limits explained](https://bulkops.microspear.app/guides/xero-tracking-categories-limit)
- [Xero's most requested bulk features](https://bulkops.microspear.app/guides/xero-most-requested-bulk-features)

## Why bulk tools are only safe for some actions

Xero's Accounting API can **remove** a credit note allocation, an overpayment allocation and a
tracking option archive — so a tool that shows a full preview and records before/after state can
make those operations reversible. Voiding invoices or deleting documents has no undo in the API,
which is why this list recommends no tool for those.

## About

BulkOps is built by one person. It connects through Xero's official OAuth (no passwords stored),
previews every change before writing, runs jobs under Xero's rate limits, and can undo an entire
job in one click. Free to try: unlimited previews and the first 25 executed items are free.
Contact: support@microspear.app · Release notes: https://bulkops.microspear.app/changelog
