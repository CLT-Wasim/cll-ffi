# AGENTS.md: cll-ffi

**This file is a pointer. The binding rules live in one place.**

Read, in this order, before doing anything:

1. [`CLT-Wasim/CLL/AGENTS.md`](https://github.com/CLT-Wasim/CLL/blob/main/AGENTS.md) — the master directive.
2. [`CLT-Wasim/CLL/DECISIONS.md`](https://github.com/CLT-Wasim/CLL/blob/main/DECISIONS.md) — every decision and its reason.
3. [`CLT-Wasim/CLL/ROADMAP.md`](https://github.com/CLT-Wasim/CLL/blob/main/ROADMAP.md) — milestones and exit criteria.
4. `docs/SPEC.md` in this repository's parent project once it exists.

Precedence when documents disagree: `AGENTS.md` > `docs/SPEC.md` > `DECISIONS.md` > `ROADMAP.md` > issue/PR text > chat messages.

## Local rules for `cll-ffi`

* **Purpose:** C ABI, DLPack, and the PyTorch bridge. The only place where non-CLL code is allowed to meet CLL code, and it always requires an explicit `cap Ffi` token.
* **Language:** Rust for the ABI layer, CLL for the safe wrappers. Python appears only in interop tests.
* Nothing ships here that the specification does not already define. If the spec is silent, write an RFC in the parent `CLL` repository first.
* `main` is protected: every change is a pull request with green CI.
* Every claim of a measurement is a command plus its raw output plus a commit hash. No number without a command.
* If this repository cannot express something, that is a missing language feature, not a reason to reach for another language.

## What this repository may contain

* `src/`
* `tests/`

## Report format at the end of every task

What was built (files, commit) · which SPEC sections it implements · commands run and their real output ·
tests passed/failed/new · what is uncertain · next step.
