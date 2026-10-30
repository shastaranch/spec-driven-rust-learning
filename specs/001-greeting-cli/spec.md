# Feature Specification: Greeting CLI

**Feature**: `001-greeting-cli` (selected with `SPECIFY_FEATURE_DIRECTORY`)
**Created**: 2026-10-29
**Status**: Draft — ready for learner review; implementation not started
**Input**: Learn Rust and spec-driven development through a simple greeting program.

## User Scenarios & Testing

### User Story 1 — Default greeting (Priority: P1)

As a learner, I can run a program with no arguments and see a predictable greeting.
This is the smallest working slice and teaches the edit/test/run loop.

**Independent Test**: Run the executable without arguments; compare output and status.

**Acceptance Scenario**: Given no arguments, when the program runs, then stdout is
exactly `Hello, world!` followed by one newline, stderr is empty, and status is 0.

### User Story 2 — Personalized greeting (Priority: P2)

As a learner, I can pass one name and see it in the greeting.
This introduces inputs and string handling after the default case works.

**Independent Test**: Run with one positional argument and compare the greeting.

**Acceptance Scenarios**:

1. Given `Ada`, output is `Hello, Ada!` plus one newline; stderr is empty; status is 0.
2. Given one quoted argument `Ada Lovelace`, output is `Hello, Ada Lovelace!` plus one newline; stderr is empty; status is 0.
3. Given `世界`, output is `Hello, 世界!` plus one newline; stderr is empty; status is 0.
4. Given `  Ada  ` as one argument, output is `Hello, Ada!` plus one newline; stderr is empty; status is 0.

### User Story 3 — Invalid input feedback (Priority: P3)

As a learner, I get a clear error for empty names or too many arguments.
This demonstrates defining failure behavior before writing error handling.

**Independent Test**: Run each invalid-input case and inspect both streams and status.

**Acceptance Scenarios**:

1. Given an empty argument or a whitespace-only argument, stdout is empty, stderr is
   exactly `error: name must not be empty` plus one newline, and status is 2.
2. Given two or more arguments, stdout is empty, stderr is exactly
   `error: expected at most one name` plus one newline, and status is 2.
3. Given an empty first argument and a second argument, the too-many-arguments error wins.

### Edge Cases

- Whitespace at the ends is removed; internal whitespace is preserved.
- Punctuation and Unicode names are preserved after trimming.
- All arguments, including `--help` and `-h`, are treated as names; flags are out of scope.
- Non-Unicode operating-system arguments are outside this lesson's contract.

## Requirements

- **FR-001**: No arguments MUST produce the default greeting described in story 1.
- **FR-002**: One nonempty name MUST produce the personalized greeting described in story 2.
- **FR-003**: The program MUST trim leading and trailing Unicode whitespace and preserve all remaining characters.
- **FR-004**: An empty name after trimming MUST produce the empty-name error and status 2.
- **FR-005**: More than one argument MUST produce the argument-count error and status 2, before validating any name.
- **FR-006**: Successful runs MUST write only the greeting and newline to stdout with status 0; invalid runs MUST write only the specified error and newline to stderr.

## Success Criteria

- **SC-001**: All acceptance scenarios pass as reproducible automated checks.
- **SC-002**: The learner can explain how each requirement maps to a test.
- **SC-003**: The learner can change the default greeting by updating the spec, observing a failing test, and changing the implementation.

## Assumptions and Scope

The caller supplies Unicode arguments through a normal terminal with working output
streams. This lesson has no interactive input, files, network, flags, or persistence.
The learner reviews this draft before implementing it. Later lessons introduce parsing
and richer error types. Rust implementation choices belong in the plan.
