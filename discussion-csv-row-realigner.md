# CSV Row Realigner now works entirely in your browser — local file, fail-closed audit

I released a browser edition for a specific CSV failure: one free-text field contains an unquoted comma, so the rest of that row shifts into the wrong columns.

The tool asks you to choose the affected text column, repairs only over-wide rows, and refuses short or malformed rows instead of guessing. It then downloads:

- an Excel-ready UTF-8 BOM CSV; and
- a JSON audit with input/output counts, repaired rows, failures and record-count preservation.

The file stays in the browser; there is no upload endpoint. The release includes full source, eight automated tests, synthetic before/after evidence, a README and an offline ZIP.

![CSV Repair Service — USD 5 / RMB 39, Local, Private, Auditable](https://zhailong8845-art.github.io/china-ecom-csv-cleaner-product/og-csv-repair.png)

## Free self-service tool

- Live browser app: https://zhailong8845-art.github.io/csv-row-realigner-web/
- Source and tests: https://github.com/zhailong8845-art/csv-row-realigner-web
- Versioned ZIP: https://github.com/zhailong8845-art/csv-row-realigner-web/releases/tag/v1.0.1

## Human-verified repair — USD 5 / RMB 39

For one CSV up to 500 rows and one agreed shifted text field, the fixed-price service includes an Excel-ready repaired CSV, JSON record-count audit, and one recheck.

- Scope, privacy rules, evidence and FAQ: https://zhailong8845-art.github.io/china-ecom-csv-cleaner-product/csv-repair-service.html
- Submit a sanitized request: https://github.com/zhailong8845-art/china-ecom-csv-cleaner-product/issues/new?template=csv-row-realigner-web-purchase.yml

Please use only field names and synthetic examples in public requests. Do not post customer/order records, personal data, credentials, private URLs or payment information.
