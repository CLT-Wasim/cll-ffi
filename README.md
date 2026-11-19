# cll-ffi

**foreign function interface** — part of [CLL](https://github.com/CLT-Wasim/CLL), the Conserving Logic Language.

> Read [`AGENTS.md`](./AGENTS.md) first. It points at the binding rules; this README is only a summary.

## Purpose

C ABI, DLPack, and the PyTorch bridge. The only place where non-CLL code is allowed to meet CLL code, and it always requires an explicit `cap Ffi` token.

## Status

Pre-v1. Nothing here is shipped until a command produced the result and the result is in a
results table with the command that produced it. See the milestone list in
[`ROADMAP.md`](https://github.com/CLT-Wasim/CLL/blob/main/ROADMAP.md).

## Layout

* `src/`
* `tests/`

## Language policy

Rust for the ABI layer, CLL for the safe wrappers. Python appears only in interop tests.

## License

Apache-2.0. See [`LICENSE`](./LICENSE).
