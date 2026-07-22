A fixed-price service for marketplace or ERP CSV exports whose column names are not recognized by the standard tool.

**Try the privacy-safe check first (free)**

Download v1.2.0 and run:

```bash
ecom-profit orders.csv --inspect-header
```

This command reads the CSV header row only, never order records. Exit code `0` means the export is already compatible; exit code `2` lists the required fields that need mapping. Buy the service only if the free check reports missing required fields.

**Deliverables**

- one custom `column-map.json`;
- one copy-ready `ecom-profit` command;
- reproducible verification using a synthetic row;
- one re-check for the same header within seven days.

**Price and turnaround**

- USD 5 / RMB 39
- within 24 hours after scope and legitimate payment are confirmed

**Privacy boundary**

Submit only a sanitized first header row and descriptions of non-standard columns. Do not submit real order rows, names, phone numbers, addresses, account details, credentials, secrets, or payment information in public.

- Service/order form: https://github.com/zhailong8845-art/china-ecom-csv-cleaner-product/issues/new?template=profit-map-service.yml
- Product v1.2.0: https://github.com/zhailong8845-art/china-ecom-profit-analyzer/releases/tag/v1.2.0
- 13 tests and six OS/Python install jobs: https://github.com/zhailong8845-art/china-ecom-profit-analyzer/actions/runs/29892258825

An inquiry, issue, or delivery is not treated as paid until funds are actually received and usable.
