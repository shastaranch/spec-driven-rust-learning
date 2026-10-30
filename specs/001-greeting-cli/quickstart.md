# Lesson 1 quickstart

Implementation has not started. First follow T001 in [tasks.md](tasks.md).
After creating the package:

```sh
cd lessons/001-greeting-cli
cargo test
cargo run --
cargo run -- Ada
cargo run -- "Ada Lovelace"
cargo run -- ""
cargo run -- Ada Grace
```

`cargo run` adds Cargo messages to stderr; automated contract checks must launch
the built executable directly. After implementation, a direct manual check is:

```sh
cargo build
./target/debug/greeting-cli Ada
./target/debug/greeting-cli ""
echo $?
```

The last command should print `2` for the invalid name. See the spec for exact output.

## Completion checks (pending)

```sh
cargo fmt --check
cargo clippy --all-targets -- -D warnings
cargo test
```

Record the actual command outcomes and requirement-to-test mapping here when done.
No checks have been run against Rust code because the package does not exist yet.

## Reflection (complete after implementation)

- Which value owns each name, and where is it borrowed?
- What ambiguity did the acceptance scenarios remove?
- Which test caught a mistake, and why?
- What changed when you modified the default greeting?
