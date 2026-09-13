# Active Impersonation Review

**Generated:** 2026-09-13T17:02:54.504914+00:00

This stage scores live DNSTwist lookalike domains against the real brand sites using lightweight fingerprinting, then emits conservative blocking lists from only the highest-confidence non-canonical findings.

Quick links:

- [Back to Hardening](../README.md)
- [Back to Repo Root](../../README.md)

## What This Means

- **HIGH_MATCH** - the candidate looks materially like the baseline and deserves immediate review
- **MEDIUM_MATCH** - some signals line up, but it still needs analyst judgment
- **LOW_MATCH / INCONCLUSIVE** - weak resemblance or not enough content to decide
- **OFFLINE / ERROR** - the candidate did not respond cleanly during this run

Domains that only canonical-redirect to the real brand are filtered out of the visible findings and are **not** added to the blocking lists.

## Settings

- Targets audited: `40`
- Candidate domains audited: `5686`
- Visible findings kept: `5317`
- Canonical brand redirects filtered out: `369`
- Blocklist entries emitted: `0`
- Max workers: `10`
- Target jobs: `2`
- Connect timeout: `3.0` seconds
- Read timeout: `5.0` seconds
- Max response bytes: `262144`
- Max domains per target: `unlimited`
- TSV report: [results.tsv](results.tsv)
- JSON report: [report.json](report.json)
- Aggregated hosts blocklist: [categories/active_impersonation.txt](categories/active_impersonation.txt)
- Aggregated RPZ blocklist: [categories/active_impersonation.rpz](categories/active_impersonation.rpz)

## Overall Summary

| HIGH | MEDIUM | LOW | INCONCLUSIVE | OFFLINE | ERROR |
|------|--------|-----|--------------|---------|-------|
| 0 | 8 | 1948 | 1056 | 2305 | 0 |

## Blocking Lists

Only `HIGH_MATCH` domains that do **not** canonical-redirect to the real brand are added to these exact-host blocklists.

| Output | Entries | File |
|--------|---------|------|
| Hosts | 0 | [categories/active_impersonation.txt](categories/active_impersonation.txt) |
| RPZ | 0 | [categories/active_impersonation.rpz](categories/active_impersonation.rpz) |

## Per-Target Summary

| Target | Seeds | Audited | Visible | Blocklist | Filtered Redirects | High | Medium | Low | Offline | Errors | Note |
|--------|-------|---------|---------|-----------|--------------------|------|--------|-----|---------|--------|------|
| Adobe | 2 | 181 | 181 | 0 | 0 | 0 | 0 | 77 | 80 | 0 |  |
| Amazon | 1 | 262 | 122 | 0 | 140 | 0 | 0 | 33 | 79 | 0 |  |
| Apple | 2 | 350 | 333 | 0 | 17 | 0 | 0 | 128 | 154 | 0 |  |
| Atlassian | 1 | 47 | 42 | 0 | 5 | 0 | 0 | 16 | 17 | 0 |  |
| Auth0 | 1 | 187 | 183 | 0 | 4 | 0 | 0 | 5 | 72 | 0 |  |
| Box | 1 | 103 | 103 | 0 | 0 | 0 | 0 | 72 | 28 | 0 |  |
| Cloudflare | 1 | 172 | 170 | 0 | 2 | 0 | 0 | 30 | 127 | 0 |  |
| Coinbase | 1 | 255 | 255 | 0 | 0 | 0 | 0 | 20 | 50 | 0 |  |
| DHL | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Skipped target because no reachable baselines were available. |
| Docker | 1 | 87 | 87 | 0 | 0 | 0 | 0 | 44 | 30 | 0 |  |
| DocuSign | 1 | 90 | 85 | 0 | 5 | 0 | 0 | 26 | 44 | 0 |  |
| Dropbox | 2 | 132 | 131 | 0 | 1 | 0 | 0 | 55 | 66 | 0 |  |
| Duo | 1 | 118 | 118 | 0 | 0 | 0 | 0 | 74 | 26 | 0 |  |
| FedEx | 1 | 118 | 118 | 0 | 0 | 0 | 0 | 5 | 67 | 0 |  |
| Figma | 1 | 81 | 81 | 0 | 0 | 0 | 0 | 46 | 22 | 0 |  |
| GitHub | 1 | 156 | 150 | 0 | 6 | 0 | 0 | 62 | 54 | 0 |  |
| GitLab | 1 | 80 | 80 | 0 | 0 | 0 | 0 | 43 | 33 | 0 |  |
| Google | 2 | 561 | 550 | 0 | 11 | 0 | 8 | 156 | 319 | 0 |  |
| Intuit | 1 | 140 | 140 | 0 | 0 | 0 | 0 | 53 | 63 | 0 |  |
| Jira | 1 | 100 | 100 | 0 | 0 | 0 | 0 | 66 | 23 | 0 |  |
| Microsoft | 5 | 929 | 860 | 0 | 69 | 0 | 0 | 343 | 396 | 0 |  |
| Notion | 1 | 12 | 12 | 0 | 0 | 0 | 0 | 7 | 5 | 0 |  |
| Okta | 1 | 110 | 109 | 0 | 1 | 0 | 0 | 60 | 30 | 0 |  |
| OneLogin | 1 | 31 | 31 | 0 | 0 | 0 | 0 | 10 | 19 | 0 |  |
| PayPal | 1 | 213 | 205 | 0 | 8 | 0 | 0 | 59 | 45 | 0 |  |
| Ping Identity | 1 | 31 | 31 | 0 | 0 | 0 | 0 | 1 | 29 | 0 |  |
| QuickBooks | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Skipped target because no reachable baselines were available. |
| Salesforce | 1 | 119 | 104 | 0 | 15 | 0 | 0 | 35 | 51 | 0 |  |
| ServiceNow | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Skipped target because no reachable baselines were available. |
| Shopify | 1 | 183 | 144 | 0 | 39 | 0 | 0 | 74 | 53 | 0 |  |
| Slack | 1 | 90 | 90 | 0 | 0 | 0 | 0 | 48 | 24 | 0 |  |
| Stripe | 1 | 99 | 93 | 0 | 6 | 0 | 0 | 46 | 36 | 0 |  |
| Trello | 1 | 61 | 60 | 0 | 1 | 0 | 0 | 30 | 17 | 0 |  |
| TurboTax | 1 | 151 | 127 | 0 | 24 | 0 | 0 | 25 | 89 | 0 |  |
| UPS | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Skipped target because no reachable baselines were available. |
| USPS | 1 | 98 | 98 | 0 | 0 | 0 | 0 | 63 | 24 | 0 |  |
| Venmo | 1 | 73 | 72 | 0 | 1 | 0 | 0 | 33 | 19 | 0 |  |
| Zendesk | 1 | 58 | 56 | 0 | 2 | 0 | 0 | 27 | 21 | 0 |  |
| Zoom | 1 | 81 | 81 | 0 | 0 | 0 | 0 | 33 | 39 | 0 |  |
| eBay | 1 | 127 | 115 | 0 | 12 | 0 | 0 | 43 | 54 | 0 |  |

## Per-Target Blocking Lists

No block-worthy domains were emitted in this run.

## Top Suspicious Matches

| Target | Domain | Status | Score | Baseline | Redirect | Title | Content |
|--------|--------|--------|-------|----------|----------|-------|---------|
| Google | `xn--gogl-jpa1d.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--gogl-jpa1d.com` | 1.00 | 0.14 |
| Google | `xn--gool-dxa1756b.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--gool-dxa1756b.com` | 1.00 | 0.13 |
| Google | `xn--gogle-1ta.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--gogle-1ta.com` | 1.00 | 0.10 |
| Google | `xn--ooge-21a88g.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--ooge-21a88g.com` | 1.00 | 0.10 |
| Google | `xn--googl-9cc.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--googl-9cc.com` | 1.00 | 0.06 |
| Google | `xn--googl-lsa.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--googl-lsa.com` | 1.00 | 0.05 |
| Google | `xn--gogle-g91b.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--gogle-g91b.com` | 1.00 | 0.04 |
| Google | `xn--ooge-9wa5r.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--ooge-9wa5r.com` | 1.00 | 0.04 |

## Operational Notes

1. Canonical redirects to the real brand are intentionally excluded from both the report rows and the blocklists
2. The blocking lists are conservative and only include `HIGH_MATCH` domains
3. Review `MEDIUM_MATCH` findings manually before promoting them anywhere
4. Re-run the report when you regenerate hardening lists or change target coverage
