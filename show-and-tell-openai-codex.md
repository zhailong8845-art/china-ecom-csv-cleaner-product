## What I built

I used Codex to build **GitHub Bounty Preflight**, a small zero-dependency CLI for agents and developers who work from GitHub issue queues.

It tries to stop an agent before it spends tokens and implementation time on a stale or already-claimed bounty. Given a public issue URL, it checks:

- whether the underlying issue is still open;
- whether an explicit USD/USDC amount appears together with a `bounty`, `funded`, or `reward` label;
- whether the repository has been pushed in the last 90 days;
- whether pull requests already reference the issue;
- whether the issue says `claimed`, `filled`, or has no slots left.

It emits Markdown or JSON and exits `0` only for `REVIEW`; rejected candidates exit `2`. `REVIEW` intentionally does **not** mean the payer, escrow, acceptance, or payout rail is trustworthy—those remain manual checks.

## A real result

The included example checks an open issue advertising USD 16 with `bounty` and `funded` labels. The tool still rejects it because the single slot is claimed and two PRs already reference the issue. That was the failure mode I most wanted to catch: a plausible-looking amount and open state are not enough.

- Source and release: https://github.com/zhailong8845-art/github-bounty-preflight
- Example report: https://github.com/zhailong8845-art/github-bounty-preflight/blob/main/examples/frantic-claimed.md
- Tests: 8 deterministic unit tests; the packaged wheel was installed into a clean target and re-ran the live example successfully.

I would especially value feedback on additional fail-closed signals that are useful in Codex workflows, such as linked-PR detection beyond textual issue references or portable evidence formats.

For transparency: the CLI is free and MIT licensed. I also offer an optional USD 5 human-reviewed report for up to 20 public issue URLs, but no purchase is required to use the tool. Please do not share private repositories, credentials, tokens, identity details, or payment information.
