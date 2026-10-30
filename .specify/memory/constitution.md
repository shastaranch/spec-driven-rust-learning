# Spec-driven Rust Learning Constitution

## Core Principles

### I. Describe behavior before code
Each exercise starts with a small spec containing observable behavior, explicit
boundaries, and concrete acceptance examples. Update the spec before changing behavior.

### II. Keep lessons small
Introduce a few Rust concepts per lesson. Prefer the standard library, synchronous
code, and a local CLI. Add dependencies only when a lesson explains their purpose.

### III. Make requirements executable
Map each functional requirement to a test. Observe a relevant test fail before
implementing the behavior, then refactor with tests passing. Exercise CLI output,
error output, and exit status where specified.

### IV. Explain Rust decisions
Use safe Rust. Explain ownership, borrowing, and error handling as they appear.
Avoid unexplained cloning, panics on expected user errors, and premature abstractions.

### V. Preserve the learning process
Keep spec, plan, tasks, code, and verification evidence consistent. Leave unfinished
tasks unchecked. A learner should be able to explain a change and reproduce its checks.

## Quality Gates

For implemented Rust packages, run `cargo fmt --check`, `cargo clippy --all-targets
-- -D warnings`, and `cargo test` from that package's directory. Record actual outcomes;
do not mark planned checks as passed. Documentation-only lessons need link and
specification consistency checks, not artificial Rust tests.

## Development Workflow

Specify → clarify if needed → plan → tasks → failing test → implementation →
verification → reflection. Complete one acceptance scenario at a time. Each lesson
records what was learned and one small change to explore next.

## Governance

These principles guide every exercise. Amend this document when learning needs
change, explain the reason, and update affected plans. Use semantic versioning:
major for incompatible principles, minor for added principles, patch for wording.

**Version**: 1.0.0 | **Ratified**: 2026-10-29 | **Last Amended**: 2026-10-29
