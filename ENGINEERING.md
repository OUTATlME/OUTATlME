# Engineering notes

These notes describe selected decisions in SCORESIST as of **14 September 2026**. They are a product case study, not installation instructions for the private application.

## Keeping live updates moving

Scores, goals, cards and substitutions do not necessarily become available together. A score can arrive before the corresponding event record. Heavy event polling can also delay other work if it shares the same execution lock.

SCORESIST separates the fast score loop from bounded event collection. Normal event checks use a longer cadence than score checks, while changed scores and newly finished matches receive additional, limited follow-up. This helps capture late-match events without assuming that the final whistle means the data is complete.

Unchanged event payloads avoid unnecessary database writes. Reconciliation must still allow corrections, including cancelled goals. Missing goal details are not invented from the score.

**Trade-off:** freshness depends on provider availability, scheduling and the client's next refresh. A polling interval is not an end-to-end delivery guarantee.

## Sharing a finite request budget

Live data is only one part of the workload. Upcoming fixtures, head-to-head records, historical matches and team/player enrichment also need provider access.

The synchronization design uses bounded batches and daily/minute request limits, with capacity reserved for scores and background work. Upcoming fixtures receive additional attention in the next 48-hour window where records are missing or stale. A provider-empty response remains distinct from a failed request or an unattempted job.

**Trade-off:** prioritization improves allocation; it does not make unavailable lineups appear days before kickoff or prove complete historical coverage.

## Designing connected screens

Football standings place the most useful summary columns near the team identity. Recent form uses compact result indicators. Match events link to identifiable players, and lineup formations preserve the provider's positional information.

Visual changes are checked against layout constraints. For example, improving a pitch border should preserve player positions, formation labels and the surrounding content. The same principle applies to long stadium names and narrow-screen tables.

**Trade-off:** desktop and narrow-screen render checks cover specific layouts; they are not a substitute for testing every physical device.

## Release verification

The application uses automated client/API checks and a PostgreSQL integration gate. The latest completed release verification recorded:

| Check | Dated result |
| --- | --- |
| Flutter tests | 397 passed |
| API unit tests | 1,087 passed |
| Security end-to-end tests | 33 passed |
| PostgreSQL integration gate | Passed |
| Analysis, formatting and builds | Passed for the release |
| Web deployment verification | Deployed bundle hashes matched the release artifact |

These figures describe the **14 September 2026 release verification**. They are not a continuously updated badge or a guarantee that the product has no defects. Screenshots and visual review complement the automated checks.

## Scope

The public repository intentionally contains showcase material rather than application code, provider credentials or operational configuration. Public web availability does not imply an Android store release, enabled account registration or live Formula 1 timing.

[← Back to the SCORESIST showcase](https://github.com/OUTATlME)
