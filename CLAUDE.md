# Project Rules

Claude Code loads this file into every session, but it does NOT auto-load
`AGENTS.md` — and a backticked file mention is prose, not an import. The bare
`@` lines below inline the always-required harness context (the "Must in all
lanes" set from `docs/CONTEXT_RULES.md`) at context-load time. Never wrap them
in backticks; that disables the import.

@AGENTS.md

@docs/FEATURE_INTAKE.md

Also run `scripts/bin/harness-cli query matrix` before starting work — the
third all-lanes "Must" is a command, not an importable file.

Lane-dependent context (`README.md`, `docs/HARNESS.md`, `docs/ARCHITECTURE.md`,
`docs/CONTEXT_RULES.md`, product docs, stories, decisions) is intentionally not
imported — read it per lane, as `docs/CONTEXT_RULES.md` prescribes, to keep the
fixed per-session context inside the tiny-lane budget.
