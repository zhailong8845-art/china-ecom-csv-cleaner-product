## Stop coding stale or already-claimed GitHub bounties

GitHub Bounty Preflight v1.0.0 is a zero-dependency, fail-closed CLI for public issue URLs.

It checks:

- whether the underlying issue is open;
- whether an explicit USD/USDC amount appears with a bounty/funded/reward label;
- whether the repository has been pushed in the last 90 days;
- whether pull requests already reference the issue;
- whether the bounty says claimed, filled, or has no slots left.

The included real example rejects an open, funded-looking USD 16 issue because two PRs reference it and the slot is already claimed. An advertised amount is never treated as escrow, acceptance, or payment proof.

- Free source and v1.0.0 release: https://github.com/zhailong8845-art/github-bounty-preflight/releases/tag/v1.0.0
- Real example report: https://github.com/zhailong8845-art/github-bounty-preflight/blob/main/examples/frantic-claimed.md
- Tool tests: 8/8 passing locally; packaged wheel installed and re-ran the live check successfully.

For people who want a human-reviewed result, I also offer a fixed USD 5 / RMB 39 report covering up to 20 public issue URLs, with evidence, rejection reasons, top-three scoring, and one re-check:

https://github.com/zhailong8845-art/china-ecom-csv-cleaner-product/issues/new?template=bounty-preflight-report.yml

Do not submit private repositories, tokens, credentials, identity details, wallet information, or payment data. A report or inquiry is not counted as income until legitimate funds are actually received and usable.
