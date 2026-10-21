# Security policy

These repositories are lock firmware and the libraries it is built from. A
defect here can be the difference between a door that opens for its owner and
one that opens for anyone, so please report suspected vulnerabilities privately
rather than in a public issue.

## Reporting a vulnerability

Use GitHub's private vulnerability reporting on the affected repository:
**Security → Report a vulnerability**. That opens a private advisory visible
only to you and the maintainers. No account beyond your GitHub login is needed.

If the affected repository has private reporting switched off, open the
advisory on [ultrawidelock/ultrawidelock](https://github.com/ultrawidelock/ultrawidelock/security/advisories/new)
and name the repository in the title.

Please do not open a public issue, pull request, or discussion for a suspected
vulnerability until an advisory for it has been published.

Useful things to include, in rough order of value:

- The repository, and the commit or tag you tested.
- Which seam is involved: credential protocol, UWB ranging, BLE transport,
  mesh networking, crypto, signed update, or credential storage.
- A reproduction. A host-suite test case is the fastest possible report; a
  serial log or a described sequence is fine too.
- Whether the attack needs physical proximity, a paired credential, or neither.

Never paste a radio capture or a bench log without scrubbing it. Those can carry
live key material and paired-device names.

## Supported versions

Everything here is pre-1.0. Only the latest release and `main` of each
repository are supported; fixes are not backported.

## Scope

In scope: project-original code in any repository of this organization,
including the credential protocol, ranging and distance bounding, transports,
the signed update path, and anything that lets key material reach a log or a
console.

Out of scope, because the code is not ours to fix: vendored drivers and
third-party components kept under their own terms, and the SDKs and stacks a
repository builds on. Please report those upstream, though we are glad to know
about them.

## What to expect

A maintainer acknowledges the advisory, works with you on a fix in the private
fork GitHub creates for it, and publishes the advisory with credit to you once
a fixed release exists, unless you ask not to be named.
