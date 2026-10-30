# Implementation Plan: Greeting CLI

**Feature**: `001-greeting-cli` | **Date**: 2026-10-29 | **Spec**: [spec.md](spec.md)
**Status**: Proposed; no Rust code exists yet.

## Summary

Create a standalone Cargo binary package at `lessons/001-greeting-cli`, named
`greeting-cli`, using Rust edition 2024 and the installed stable toolchain. Use only
the standard library. There is no workspace yet; run Cargo commands inside the package.

## Design

- `src/lib.rs`: a greeting function borrowing `&str` and returning `String`;
  trim with `str::trim` and reject empty names. Keep expected errors explicit.
- `src/main.rs`: collect arguments after the executable name; check argument count
  first, choose the default or validate the single name, and print to the correct
  stream. Return the specified process status without panicking on user input.
- `tests/cli.rs`: invoke `env!("CARGO_BIN_EXE_greeting-cli")` through
  `std::process::Command`; assert stdout, stderr, and exit status. Use no shell.
- Unit tests cover trimming, Unicode, and empty names. CLI tests cover FR-001–006,
  including precedence when multiple invalid arguments occur.

No storage, third-party dependencies, async runtime, performance target, or unsafe code
is needed. The supported input scope is Unicode arguments.

## Constitution Check

The spec precedes code; three incremental stories keep the scope small; tests precede
behavior; borrowing and ownership are explicit learning goals. No exceptions needed.
Recheck these points after implementation.

## Planned Structure

```text
lessons/001-greeting-cli/
├── Cargo.toml
├── Cargo.lock
├── src/lib.rs
├── src/main.rs
└── tests/cli.rs
```

## Verification

From the lesson package: `cargo fmt --check`, `cargo clippy --all-targets -- -D warnings`,
and `cargo test`. Match every requirement to tests and record actual results in
`quickstart.md`. Code and verification are pending.
