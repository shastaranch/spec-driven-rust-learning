# Tasks: Greeting CLI

**Input**: [spec.md](spec.md), [plan.md](plan.md)
**Status**: All implementation tasks pending. Complete in order.

## Setup

- [ ] T001 Review the spec and predict output for each scenario; create the binary package with `cargo new lessons/001-greeting-cli --name greeting-cli --edition 2024`.

## Story 1 — Default greeting

- [ ] T002 Add `tests/cli.rs` with an integration test for FR-001 and FR-006: no arguments, exact stdout, empty stderr, status 0. Run it and observe failure against Cargo's generated greeting.
- [ ] T003 Implement the default greeting in `src/main.rs`; rerun the test and record why it now passes.

## Story 2 — Personalized greeting

- [ ] T004 Add failing unit tests in `src/lib.rs` and CLI tests in `tests/cli.rs` for FR-002 and FR-003: Ada, quoted full name, Unicode, padded name, punctuation, and preserved internal spaces. A missing library/function compile failure can be the first red step; rerun after adding the function stub to observe behavioral failures.
- [ ] T005 Implement greeting construction in `src/lib.rs` and single-argument handling in `src/main.rs`; explain `String`, `&str`, and borrowing; rerun all tests.

## Story 3 — Invalid input

- [ ] T006 Add failing tests for FR-004–006 in `tests/cli.rs`: empty string, spaces, Unicode whitespace, multiple arguments, and empty-first-argument precedence. Assert exact streams and status 2.
- [ ] T007 Implement validation and error reporting in `src/lib.rs` and `src/main.rs`; ensure expected input errors do not panic and all tests pass.

## Review and reflection

- [ ] T008 Run the three quality commands in `quickstart.md`; map FR-001–006 to named tests and record results there.
- [ ] T009 Explain the ownership of CLI arguments, borrowed names, and returned greetings. Complete the reflection in `quickstart.md`; try changing the default greeting through spec → failing test → code.
