# Contributing

This file is the default for every repository in the organization. A
repository with its own `CONTRIBUTING.md` overrides it; the main firmware
repository has one, with its exact verification gates.

## What a change needs

1. **Build and test with the repository's own instructions.** Each README
   names the toolchain and the check to run. Run that check before opening a
   pull request, and say in the pull request what you ran and on what hardware,
   if any.
2. **Keep the diff to what the change needs.** No drive-by reformatting, no
   unrelated renames, no speculative features.
3. **Never weaken a test, a purity rule, or an allowlist to get a pass.** If a
   change makes an allowlist entry unnecessary, remove the entry in the same
   change.
4. **Leave vendored code alone.** Trees kept under a third party's terms are
   marked as such in each repository and are updated only by re-vendoring.
5. **Keep private information out.** No credentials, machine-local paths,
   personal identity, radio captures, or bench logs in files, output, or
   commit messages. Captures can carry live key material.

## Pull requests

Use the template. Describe what behavior is different after the merge, why,
and which checks you ran. Paste the relevant outcome, not only a checkmark.

Commit messages: a subject of at most 50 characters, a blank line, then a body
wrapped at 72 columns that says why.

## Bugs and proposals

Open an issue with the matching template. For anything with a security
consequence, do not open an issue: use the private reporting path in
[`SECURITY.md`](SECURITY.md).

## License

Each repository states its own license in its `LICENSE` file. By contributing
you agree that your contribution is licensed under that repository's license,
and that you have the right to license it that way.
