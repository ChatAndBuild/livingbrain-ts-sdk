# Changelog

## [0.3.1] - 2026-11-04

- Updated repository metadata after the SDK repositories moved to `ChatAndBuild`.
- `brains.runBrief` now returns `BriefRunResponse | null` when there is no recent activity.
- Added an OIDC-based npm publishing workflow.

## [0.3.0] - 2026-10-14

- Regenerated from the Oct 14 OpenAPI export.
- `Page` no longer has an `embedding` field (the API stopped returning it).
- `SearchResult` has a new required `matchedOn` field: `semantic`, `keyword`, or `both`.
- Brain deletion is now documented as a soft delete.

## [0.2.0] - 2026-09-29

