# Learning roadmap

Assumption: you are new to Rust and want hands-on practice with small examples.
Only lesson 1 is specified so far; later entries are ideas to specify when ready.

| Lesson | Example | Rust focus | Spec-driven practice |
| --- | --- | --- | --- |
| 1 | Greeting CLI | Cargo, functions, String, &str, arguments, tests | Specify output, boundaries, and acceptance scenarios |
| 2 | Temperature converter | Numbers, parsing, Result, match | Clarify units, precision, and invalid input before implementation |
| 3 | Text statistics | Borrowing, iterators, structs | Define what counts as a word and test edge cases |
| 4 | In-memory task list | Vec, enums, mutation, ownership | Split a feature into independently testable stories |
| 5 | File-backed task list | Modules, file I/O, error propagation | Evolve a spec with persistence and failure behavior |

## Repeat this loop

1. Describe what the user can do without prescribing code.
2. Write examples, including empty and invalid inputs.
3. Resolve ambiguity, then choose the simplest Rust design.
4. Turn acceptance scenarios into small, ordered tasks.
5. Write a failing test, implement the smallest change, and refactor.
6. Run formatting, linting, and tests; check implementation against requirements.
7. Record what surprised you and how a requirement change would affect the tests.

For lesson 1, explain the difference between `String` and `&str`, why command-line
arguments are owned strings, and why user errors should not cause a panic. Learning
these concepts is part of completing the lesson, not a timed exercise.
