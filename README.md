# Olango Fiber Payment Tracker (Prototype)

A browser-based prototype for importing customer due records from an Excel workbook, recording Cash/GCash payments, recording categorized expenses, viewing a date-based collections calendar, and tracking daily/month-to-date collections minus expenses.

## Run it
1. Download/extract the ZIP.
2. Open `index.html` in a modern browser while connected to the internet (the Excel reader is loaded from a CDN).
3. Go to **Customers & Import**, select a copy of the workbook, select a monthly worksheet, click **Preview selected sheet**, review, then **Import customers**.
4. Record payments and expenses. Use **Records & Export** to download CSVs and a JSON backup.

## Important limitations
- Prototype only: records are stored in local browser storage on one device. No user accounts, shared database, cloud sync, role permissions, audit log, or automated cloud backups.
- Do not use as the sole official record until tested and upgraded to secure persistent storage and authentication.
- Workbook import intentionally imports only customer name, area/address, due day, and due amount; contact numbers, Wi-Fi names, and Wi-Fi passwords are not imported.
- Importing a sheet merges customers by exact case-insensitive name and updates the due details. Review the customer list after import because names can vary between monthly sheets.
- The monthly collection calendar estimates due customers using the day of month and monthly due amount. It is not a full ledger of historical invoices.
- Daily cash surplus = recorded payments minus recorded expenses. It is not formal accounting gross profit.
- SheetJS is loaded from jsDelivr CDN; an internet connection is required for the Excel import feature.

## Before real use
1. Test with a copy and fake records first.
2. Confirm import mapping and due-date rules with the business owner.
3. Add secure authentication, a real database, backups, access control, and audit logging before using sensitive customer records in a shared/production environment.
