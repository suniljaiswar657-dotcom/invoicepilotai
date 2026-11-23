# ReceiptGuard AI

A mobile-friendly invoice register and rule-based audit dashboard for small businesses.

## MVP features
- Add invoice records with vendor, invoice number, date, amount, currency and due date.
- Detect exact vendor + invoice-number duplicates.
- Flag same-vendor/same-amount/same-date records for review.
- Flag invoices more than 2x a vendor's previously recorded average.
- Flag past-due invoices.
- Search, filter, import CSV and export invoice/report CSV files.
- Responsive dashboard with spend breakdown by vendor.
- Browser-local storage; no account, server, paid API or external dependency required.

## Run locally
Open `index.html` in a modern browser. No build step or package installation is required.

## CSV import format
Required headers: `vendor,invoice_number,date,amount`

Optional headers: `currency,due_date,notes`

Example:
```csv
vendor,invoice_number,date,amount,currency,due_date,notes
Acme Supplies,INV-1042,2026-11-23,12500,INR,2026-12-10,Office materials
```

## Important limitations
- This MVP does **not** perform OCR or parse PDF/image invoices. Enter invoice details manually or import a CSV.
- Audit checks are deterministic heuristics, not AI fraud detection and not proof of fraud.
- Records stay in the current browser's local storage. They are not synced, backed up, or shared across devices.
- Currency totals are kept separate; no foreign-exchange conversion is performed.
- Do not upload confidential customer or financial records to a shared/public device.

## Deploy
Import this repository into Vercel. It is a static HTML/CSS/JavaScript site; use the repository root as the project root and no build command. Vercel's Git integration can automatically deploy commits to the connected project.

## License
MIT
