# Spec-driven Rust learning

Learn Rust and spec-driven development together through small command-line programs.
Start with behavior, describe examples, plan a small change, write a failing test,
implement it, and compare the result with the spec.

## Documentation

Explanations of repository files live in the [GitHub wiki](https://github.com/shastaranch/spec-driven-rust-learning/wiki).
Use the [one-to-one file map](https://github.com/shastaranch/spec-driven-rust-learning/wiki/Repository-file-map)
to find the page matching a source file, or start with the
[greeting specification walkthrough](https://github.com/shastaranch/spec-driven-rust-learning/wiki/File--specs--001-greeting-cli--specdotmd).
When adding or changing a tracked file, update its matching wiki explanation and
file-map entry in the same work session. Specs, plans, tasks, and runnable instructions
remain in this repo; their explanatory guides live in the wiki. The wiki is a separate
Git repository and requires its own commit and push.

## Start here

1. Read the [learning roadmap](docs/learning-roadmap.md).
2. Read the [project constitution](.specify/memory/constitution.md).
3. Open [lesson 1: greeting CLI](specs/001-greeting-cli/spec.md), then its
   [plan](specs/001-greeting-cli/plan.md) and [tasks](specs/001-greeting-cli/tasks.md).
4. Work through one unchecked task at a time. The Rust solution is intentionally
   left for the learner; no Cargo project has been created yet.

Prerequisites: Git, stable Rust with Cargo (`rustc --version`, `cargo --version`),
and Python 3.11+ with `uv` if running the Specify CLI.

## Spec Kit

This repository includes the official [GitHub Spec Kit](https://github.com/github/spec-kit)
1.2.5 scaffold: `.specify/` contains templates, Bash scripts, and workflows;
`.agents/skills/` contains the Codex skills. These are development tools, not Rust dependencies.
Restart or reopen the Codex chat in this repo if the new skills are not discovered.

In Codex chat, invoke skills using `$`:

- `$speckit-clarify` to resolve uncertainties in the current spec.
- `$speckit-plan` to refine the technical approach.
- `$speckit-tasks` to regenerate actionable work after changing the plan.
- `$speckit-analyze` to check consistency before coding.
- `$speckit-implement` to implement tasks (ask for one task at a time when learning).
- `$speckit-specify` to start the next exercise from a behavior description.

For lesson 1, select the feature before invoking those skills. In your terminal:

```sh
export SPECIFY_FEATURE_DIRECTORY="$PWD/specs/001-greeting-cli"
```

Spec Kit stores the selected feature in the ignored, machine-local file
`.specify/feature.json`. After cloning, run the following once from the repo root
to select lesson 1 for subsequent desktop chats:

```sh
SPECIFY_FEATURE_DIRECTORY="$PWD/specs/001-greeting-cli" \
  .specify/scripts/bash/check-prerequisites.sh --json --require-spec --require-tasks
```

To switch lessons later, set `SPECIFY_FEATURE_DIRECTORY` to that lesson's absolute
path when running Spec Kit scripts.

The initial constitution, spec, plan, and tasks are already drafted. Begin with:

> Use specs/001-greeting-cli. Guide me through T001, explain each command, and let me write the Rust code. Use the selected feature in .specify/feature.json.

The equivalent pinned initialization command (already run; do not rerun unless
intentionally refreshing the scaffold) is:

```sh
uvx --from specify-cli==1.2.5 specify init --here --force --non-interactive \
  --integration codex --integration-options=--skills --script sh --ignore-agent-tools
```

See the [official installation guide](https://github.github.io/spec-kit/installation.html).
Keep credentials and local agent state out of version control; only the generated skills are shared.
