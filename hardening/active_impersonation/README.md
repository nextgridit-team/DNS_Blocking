# Active Impersonation Review

**Generated:** 2026-09-19T09:55:57.186438+00:00

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
- Visible findings kept: `5319`
- Canonical brand redirects filtered out: `367`
- Blocklist entries emitted: `1`
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
| 1 | 8 | 1972 | 1013 | 2325 | 0 |

## Blocking Lists

Only `HIGH_MATCH` domains that do **not** canonical-redirect to the real brand are added to these exact-host blocklists.

| Output | Entries | File |
|--------|---------|------|
| Hosts | 1 | [categories/active_impersonation.txt](categories/active_impersonation.txt) |
| RPZ | 1 | [categories/active_impersonation.rpz](categories/active_impersonation.rpz) |

## Per-Target Summary

| Target | Seeds | Audited | Visible | Blocklist | Filtered Redirects | High | Medium | Low | Offline | Errors | Note |
|--------|-------|---------|---------|-----------|--------------------|------|--------|-----|---------|--------|------|
| Adobe | 2 | 181 | 181 | 0 | 0 | 0 | 0 | 78 | 84 | 0 |  |
| Amazon | 1 | 262 | 122 | 0 | 140 | 0 | 0 | 34 | 79 | 0 |  |
| Apple | 2 | 350 | 333 | 0 | 17 | 0 | 0 | 128 | 159 | 0 |  |
| Atlassian | 1 | 47 | 42 | 0 | 5 | 0 | 0 | 15 | 18 | 0 |  |
| Auth0 | 1 | 187 | 183 | 0 | 4 | 0 | 0 | 5 | 73 | 0 |  |
| Box | 1 | 103 | 103 | 0 | 0 | 0 | 0 | 72 | 26 | 0 |  |
| Cloudflare | 1 | 172 | 170 | 0 | 2 | 0 | 0 | 33 | 126 | 0 |  |
| Coinbase | 1 | 255 | 255 | 1 | 0 | 1 | 0 | 20 | 50 | 0 |  |
| DHL | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Skipped target because no reachable baselines were available. |
| Docker | 1 | 87 | 87 | 0 | 0 | 0 | 0 | 45 | 30 | 0 |  |
| DocuSign | 1 | 90 | 85 | 0 | 5 | 0 | 0 | 30 | 40 | 0 |  |
| Dropbox | 2 | 132 | 131 | 0 | 1 | 0 | 0 | 58 | 65 | 0 |  |
| Duo | 1 | 118 | 118 | 0 | 0 | 0 | 0 | 75 | 26 | 0 |  |
| FedEx | 1 | 118 | 118 | 0 | 0 | 0 | 0 | 42 | 66 | 0 |  |
| Figma | 1 | 81 | 81 | 0 | 0 | 0 | 0 | 43 | 24 | 0 |  |
| GitHub | 1 | 156 | 150 | 0 | 6 | 0 | 0 | 65 | 55 | 0 |  |
| GitLab | 1 | 80 | 80 | 0 | 0 | 0 | 0 | 41 | 35 | 0 |  |
| Google | 2 | 561 | 550 | 0 | 11 | 0 | 8 | 156 | 316 | 0 |  |
| Intuit | 1 | 140 | 140 | 0 | 0 | 0 | 0 | 49 | 68 | 0 |  |
| Jira | 1 | 100 | 100 | 0 | 0 | 0 | 0 | 67 | 23 | 0 |  |
| Microsoft | 5 | 929 | 860 | 0 | 69 | 0 | 0 | 332 | 398 | 0 |  |
| Notion | 1 | 12 | 12 | 0 | 0 | 0 | 0 | 6 | 6 | 0 |  |
| Okta | 1 | 110 | 109 | 0 | 1 | 0 | 0 | 59 | 31 | 0 |  |
| OneLogin | 1 | 31 | 31 | 0 | 0 | 0 | 0 | 9 | 19 | 0 |  |
| PayPal | 1 | 213 | 205 | 0 | 8 | 0 | 0 | 57 | 50 | 0 |  |
| Ping Identity | 1 | 31 | 31 | 0 | 0 | 0 | 0 | 1 | 29 | 0 |  |
| QuickBooks | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Skipped target because no reachable baselines were available. |
| Salesforce | 1 | 119 | 104 | 0 | 15 | 0 | 0 | 32 | 56 | 0 |  |
| ServiceNow | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Skipped target because no reachable baselines were available. |
| Shopify | 1 | 183 | 146 | 0 | 37 | 0 | 0 | 76 | 53 | 0 |  |
| Slack | 1 | 90 | 90 | 0 | 0 | 0 | 0 | 49 | 23 | 0 |  |
| Stripe | 1 | 99 | 93 | 0 | 6 | 0 | 0 | 47 | 35 | 0 |  |
| Trello | 1 | 61 | 60 | 0 | 1 | 0 | 0 | 30 | 16 | 0 |  |
| TurboTax | 1 | 151 | 127 | 0 | 24 | 0 | 0 | 21 | 95 | 0 |  |
| UPS | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Skipped target because no reachable baselines were available. |
| USPS | 1 | 98 | 98 | 0 | 0 | 0 | 0 | 63 | 24 | 0 |  |
| Venmo | 1 | 73 | 72 | 0 | 1 | 0 | 0 | 34 | 19 | 0 |  |
| Zendesk | 1 | 58 | 56 | 0 | 2 | 0 | 0 | 26 | 20 | 0 |  |
| Zoom | 1 | 81 | 81 | 0 | 0 | 0 | 0 | 32 | 39 | 0 |  |
| eBay | 1 | 127 | 115 | 0 | 12 | 0 | 0 | 42 | 49 | 0 |  |

## Per-Target Blocking Lists

| Target | Entries | Hosts | RPZ |
|--------|---------|-------|-----|
| Coinbase | 1 | [lists/coinbase.txt](lists/coinbase.txt) | [lists/coinbase.rpz](lists/coinbase.rpz) |

## Top Suspicious Matches

| Target | Domain | Status | Score | Baseline | Redirect | Title | Content |
|--------|--------|--------|-------|----------|----------|-------|---------|
| Coinbase | `coinbose.com` | HIGH_MATCH | 9 | `coinbase.com` | `domains.atom.com` | 1.00 | 1.00 |
| Google | `xn--gogl-jpa1d.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--gogl-jpa1d.com` | 1.00 | 0.13 |
| Google | `xn--gool-dxa1756b.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--gool-dxa1756b.com` | 1.00 | 0.11 |
| Google | `xn--gogle-1ta.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--gogle-1ta.com` | 1.00 | 0.08 |
| Google | `xn--ooge-21a88g.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--ooge-21a88g.com` | 1.00 | 0.08 |
| Google | `xn--ooge-9wa5r.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--ooge-9wa5r.com` | 1.00 | 0.06 |
| Google | `xn--googl-9cc.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--googl-9cc.com` | 1.00 | 0.05 |
| Google | `xn--googl-lsa.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--googl-lsa.com` | 1.00 | 0.05 |
| Google | `xn--gogle-g91b.com` | MEDIUM_MATCH | 3 | `google.com` | `xn--gogle-g91b.com` | 1.00 | 0.04 |

## Operational Notes

1. Canonical redirects to the real brand are intentionally excluded from both the report rows and the blocklists
2. The blocking lists are conservative and only include `HIGH_MATCH` domains
3. Review `MEDIUM_MATCH` findings manually before promoting them anywhere
4. Re-run the report when you regenerate hardening lists or change target coverage
