## CSV Row Realigner v1.0.0 — fix shifted columns without losing records

A free-text field containing an unquoted comma can shift every later value into the wrong CSV column. CSV Row Realigner repairs that specific failure mode using an explicitly configured text column, then verifies the result instead of silently guessing.

The offline, dependency-free CLI:

- restores the expected row width;
- normalizes selected dates to `yyyy-mm-dd`;
- rejects missing or duplicate unique IDs;
- preserves quoted delimiters and line breaks;
- refuses to overwrite an existing output unless `--force` is explicit; and
- emits a JSON audit with input/output counts and every repair.

The real bundled example preserves all three records, repairs one shifted row, normalizes two dates, and reports zero failures. Eight automated tests pass.

**Download v1.0.0:** https://github.com/zhailong8845-art/csv-row-realigner/releases/tag/v1.0.0

Suggested price is **USD 5 / RMB 39**, including source, wheel, examples, tests, audit evidence and terminal demo. The source is public so buyers can inspect it before purchasing support or a packaged handoff.

**Privacy-safe purchase inquiry:** https://github.com/zhailong8845-art/china-ecom-csv-cleaner-product/issues/new?template=csv-row-realigner-purchase.yml

Do not post real CSV records, customer data, credentials, contact details, or payment information in a public issue.
