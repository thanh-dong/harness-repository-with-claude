# Changelog

## 2026-06-13 - PR #3

- docs(harness): impact-analysis plugin on the inbound tool registry (US-026) (@thanh-dong)
- Merge commit: `fe27cbe697cb17bd7fc9806956ffac3a8e458350`
- Harness CLI release: not required
- Changed files:
  - `docs/FEATURE_INTAKE.md`
  - `docs/IMPACT_ANALYSIS.md`
  - `docs/stories/epics/E04-impact-analysis/US-026-blast-radius-plugin.md`
  - `docs/templates/story.md`

## 2026-06-13 - PR #2

- feat(cli): kind-aware inbound tool registry with presence scanning (@thanh-dong)
- Merge commit: `ba27b7c1204612f718c59b8e00624c0db7d73d8a`
- Harness CLI release: `harness-cli-v0.1.10`
- Changed files:
  - `AGENTS.md`
  - `README.md`
  - `crates/harness-cli/src/application.rs`
  - `crates/harness-cli/src/domain.rs`
  - `crates/harness-cli/src/infrastructure.rs`
  - `crates/harness-cli/src/interface.rs`
  - `docs/TOOL_REGISTRY.md`
  - `docs/stories/US-027-inbound-tool-registry.md`
  - `scripts/install-harness.sh`
  - `scripts/schema/005-tool-extensions.sql`

## 2026-06-09 - PR #13

- docs(phase5): Phase 5 — Evolution Infrastructure scope (@hoangnb24)
- Merge commit: `bfef94a77acfa33af81f6da96bc06f053d7f5164`
- Harness CLI release: `harness-cli-v0.1.9`
- Changed files:
  - `PHASE5.md`
  - `crates/harness-cli/src/application.rs`
  - `crates/harness-cli/src/domain.rs`
  - `crates/harness-cli/src/infrastructure.rs`
  - `crates/harness-cli/src/interface.rs`
  - `docs/FEATURE_INTAKE.md`
  - `docs/GLOSSARY.md`
  - `docs/HARNESS.md`
  - `docs/HARNESS_AUDIT.md`
  - `docs/HARNESS_COMPONENTS.md`
  - `docs/HARNESS_MATURITY.md`
  - `docs/IMPROVEMENT_PROTOCOL.md`
  - `docs/TOOL_REGISTRY.md`
  - `docs/decisions/0007-improvement-proposal-rules.md`
  - `docs/stories/US-019-machine-readable-tool-registry.md`
  - `docs/stories/US-020-batch-story-verification.md`
  - `docs/stories/US-021-intervention-recording-schema.md`
  - `docs/stories/US-022-context-rule-measurement.md`
  - `docs/stories/US-023-drift-detection-entropy-score.md`
  - `docs/stories/US-024-improvement-proposal-pipeline.md`
  - `docs/stories/epics/E03-phase-5-evolution-infrastructure/phase-5-progress.md`
  - `scripts/install-harness.sh`
  - `scripts/schema/003-tool-registry.sql`
  - `scripts/schema/004-intervention.sql`

## 2026-06-09 - Post-Merge Automation

- Added post-merge changelog automation for merged pull requests.
- Added conditional Harness CLI patch release automation when merged PRs change Rust CLI source, schema, Cargo metadata, or release packaging files.
- Reused the existing Harness CLI release workflow for release builds so tag, manual, and post-merge releases share the same verification and asset publishing path.
