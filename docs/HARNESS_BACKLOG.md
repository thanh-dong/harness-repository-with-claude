# Harness Backlog

Use this file when an agent discovers a missing harness capability but should
not change the operating model immediately.

## Template

```md
## Missing Harness Capability

### Title

Short name.

### Discovered While

Task or story that exposed the gap.

### Current Pain

What was hard, repeated, ambiguous, or unsafe?

### Suggested Improvement

What should be added or changed?

### Risk

Tiny, normal, or high-risk.

### Status

proposed | accepted | implemented | rejected
```

## Items

## Missing Harness Capability

### Title

Installer does not emit a Claude Code `CLAUDE.md` context shim.

### Discovered While

Probe-testing context effectiveness (2026-06-04): fresh Claude Code (2.1.162)
sessions auto-load `CLAUDE.md` but NOT `AGENTS.md` — even when no `CLAUDE.md`
exists. All four AGENTS.md-dependent probes answered "UNKNOWN" (0/4); after
adding a `CLAUDE.md` that `@`-imports the "Must in all lanes" set
(`@AGENTS.md`, `@docs/FEATURE_INTAKE.md`), probes scored 4/4. Same result
measured earlier in a downstream install (inflow: 25% -> 100% adherence).

### Current Pain

Every repo that installs the harness via `scripts/install-harness.sh` gets an
`AGENTS.md` shim that Claude Code never loads, so the intake gate, lanes, and
read-order are invisible to fresh sessions unless the model happens to Read
the file. A backticked file mention in `CLAUDE.md` does not import it; only a
bare `@AGENTS.md` line does.

### Suggested Improvement

Teach `install-harness.sh` to also emit (or refresh a marked block inside)
`CLAUDE.md` containing the `@AGENTS.md` / `@docs/FEATURE_INTAKE.md` imports,
mirroring this repo's root `CLAUDE.md`. Respect existing user `CLAUDE.md`
content (append marked block, back up first, like the AGENTS.md flow).

### Risk

Normal (installer change, additive, affects downstream installs).

### Status

proposed — repo-level `CLAUDE.md` shim already implemented here.

