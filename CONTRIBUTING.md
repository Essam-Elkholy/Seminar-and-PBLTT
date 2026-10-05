# Contributing

## Before coding

Read the repository README, your Project task and the interface worksheet. Research your assigned module and record its purpose, role in this system, prior implementations, useful GitHub code, proposed interface and verification plan.

Discuss unresolved assumptions with Essam and neighboring module owners. Do not silently choose clock domains, reset behavior, handshakes, memory latency or image boundary handling.

Use English for documentation, filenames, code comments, commit messages and pull request descriptions.

## Where to put work

- Synthesizable Verilog belongs in `rtl/<module>/`.
- Self-checking testbenches belong in `tb/<module>/`; system tests belong in `tb/system/`.
- Image tools and the reference model belong in `python/`.
- Small shared test inputs and expected outputs belong in `testdata/`.
- Board constraints belong in `constraints/`.
- Research, architecture, interface and verification notes belong in `docs/`.

The current .v files are comment-only placeholders. Add the agreed implementation in the matching file, or propose a justified filename change. Avoid committing generated simulator libraries, waveform dumps or FPGA build directories.

## Branch and pull request workflow

1. Clone the repository once, then keep your local `main` up to date.
2. Create a focused branch from the current `main`, such as `feature/uart-tx`, `feature/fifo` or `docs/uart-research`.
3. Implement the task and check it against its agreed interface and acceptance criteria.
4. Commit and push to your branch.
5. Open a pull request targeting `main`. Use a Draft PR for incomplete work or early feedback.
6. Link the relevant Issue or Project task and request review from Essam.
7. Address review comments and resolve conflicts before merging.

If a Project task is a draft item, convert it to an Issue in this repository when a repository issue number is needed. Use `Closes #<number>` only when the PR fully completes that issue; otherwise link it without an automatic closing keyword.

## Review expectations

An RTL implementation PR should include the module, its testbench, test procedure, actual results and known limitations. Check timing alignment, data order, reset behavior and boundary conditions, not just a visually plausible output.

Documentation and scaffold PRs should state that no RTL tests were run. Never report a placeholder, an unrun test or a saved waveform setup as a passing implementation.

Module owners maintain their local tests. Essam coordinates system tests, interface review and integration. Mark a task Done after its agreed acceptance criteria are met.

## Reference code

Explain studied code before adapting it. Record source links, changes and assumptions, and retain attribution and license notices required by the original source.
