# CSV Row Realigner now works entirely in your browser — local file, fail-closed audit

I released a browser edition for a specific CSV failure: one free-text field contains an unquoted comma, so the rest of that row shifts into the wrong columns.

Click **Try the synthetic sample** to verify the complete workflow without preparing a file. For your own data, the tool asks you to choose the affected text column, repairs only over-wide rows, and refuses short or malformed rows instead of guessing. It then downloads:

- an Excel-ready UTF-8 BOM CSV; and
- a JSON audit with input/output counts, repaired rows, failures and record-count preservation.

The file stays in the browser; there is no upload endpoint. The release includes full source, eight automated tests, synthetic before/after evidence, a README and an offline ZIP.

- Live browser app: https://zhailong8845-art.github.io/csv-row-realigner-web/
- Source and tests: https://github.com/zhailong8845-art/csv-row-realigner-web
- Versioned ZIP: https://github.com/zhailong8845-art/csv-row-realigner-web/releases/tag/v1.0.1

Suggested product price: **USD 9 / RMB 59**. If you have one file up to 500 rows and prefer a human-checked result, the fixed-price first batch is **USD 5**: https://gist.github.com/zhailong8845-art/04d87e552899eabf815da343567f8439

Please use only synthetic examples in public replies. Do not post customer/order records, personal data, credentials, private URLs or payment information.
