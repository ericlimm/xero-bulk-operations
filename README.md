# Bulk operations for Xero — guides and a tool for the jobs that are still one-at-a-time

If you use Xero and need to do something in bulk that the product handles one item at a time
(allocating many credit notes, building a batch payment that includes credit notes, exporting a
year of attachments, archiving tracking options), this page collects the manual steps and points
to [BulkOps](https://bulkops.microspear.app), a Xero add-on that does each of these in one run.

Written by the developer of BulkOps, so read the tool recommendations with that in mind.
Corrections and additions are welcome via issues or pull requests.

| What you need to do in bulk | Interest on Xero's Product Ideas board | Manual steps today | With BulkOps |
|---|---|---|---|
| Allocate many credit notes to open invoices | 480+ votes | Open each credit note → Allocate credit → enter amounts → save | Scan, propose matches, preview every line, run as one job, undo in one click |
| Allocate overpayments and prepayments | part of the same request | Same one-at-a-time screen | Same flow as credit notes ([guide](https://bulkops.microspear.app/guides/bulk-allocate-overpayments-xero)) |
| Build a batch payment that includes credit notes | 920+ votes | Allocate credit notes first, then batch-pay the remaining balances | Allocation and batch payment in one run ([guide](https://bulkops.microspear.app/guides/xero-batch-payment-credit-notes)) |
| Export attached files for a date range | 690+ votes | Open each document and download each attachment | One ZIP grouped by invoice or bill number ([guide](https://bulkops.microspear.app/guides/bulk-export-xero-attachments)) |
| Archive many tracking-category options | 150+ votes | Archive options one by one (100-option limit per category) | Select and archive in one job, with undo ([guide](https://bulkops.microspear.app/guides/bulk-archive-tracking-categories-xero)) |

## Guides (manual steps first, tool second)

- [How to bulk allocate credit notes in Xero](https://bulkops.microspear.app/guides/bulk-credit-note-allocation-xero)
- [How to allocate one credit note to multiple invoices](https://bulkops.microspear.app/guides/allocate-credit-note-to-multiple-invoices-xero)
- [How to remove a credit note allocation](https://bulkops.microspear.app/guides/remove-credit-note-allocation-xero)
- [How to bulk allocate overpayments](https://bulkops.microspear.app/guides/bulk-allocate-overpayments-xero)
- [How to include credit notes in a Xero batch payment](https://bulkops.microspear.app/guides/xero-batch-payment-credit-notes)
- [How to bulk export attachments from Xero](https://bulkops.microspear.app/guides/bulk-export-xero-attachments)
- [How to bulk archive tracking categories and options](https://bulkops.microspear.app/guides/bulk-archive-tracking-categories-xero)
- [Xero's tracking category limits explained](https://bulkops.microspear.app/guides/xero-tracking-categories-limit)
- [Xero's most requested bulk features](https://bulkops.microspear.app/guides/xero-most-requested-bulk-features)

## Which bulk actions are safe to automate

Xero's Accounting API lets a tool remove a credit note allocation, an overpayment allocation and a
tracking-option archive. That is what makes these jobs reversible: BulkOps records the before and
after state of every write and can undo a whole job. Actions with no undo in the API, such as
voiding invoices, are deliberately left out.

## About BulkOps

BulkOps connects through Xero's official OAuth (no passwords stored), previews every change before
writing, runs jobs under Xero's API rate limits with automatic pause and resume, and can undo an
entire job in one click with a CSV audit trail. Free to try: unlimited previews and the first 25
executed items are free. Built and supported by one person.
Contact: support@microspear.app · Release notes: https://bulkops.microspear.app/changelog
