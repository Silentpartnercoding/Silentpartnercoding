# Silent Partner Coding

Independent contributor working on reproducible agent security, evidence
provenance, and provider-neutral interoperability.

I focus on small, reviewable changes where identity, authority, evidence, and
runtime behavior meet. I prefer tested boundaries and explicit uncertainty to
broad trust claims.

## Current work

- [Minority Prophet](https://github.com/Silentpartnercoding/minority-prophet)
  studies how copied or commonly controlled claims should affect an evidence
  assessment. It includes preregistered experiments, reproducible records, and
  machine-checked results with documented limits.
- [Minority Prophet Border](https://github.com/Silentpartnercoding/minority-prophet-border)
  defines portable admission records that bind identity, delegated authority,
  an exact proposed action, destination policy, evidence, and human intervention.
- [Minority Prophet Gate](https://github.com/Silentpartnercoding/minority-prophet-gate)
  is a reference implementation of a deterministic-policy-first decision ladder:
  ordinary policy remains primary, evidence-sensitive questions may receive a
  provenance assessment, and unresolved cases escalate.

These projects are research and reference implementations, not production
certifications. Evidence assessment does not grant authority, and a different
name, key, service, or verifier does not by itself establish independence.

## How I contribute

- start with the project's issue, policy, and maintainer-defined boundary;
- check whether the problem is already covered before proposing work;
- keep changes narrow, testable, and native to the host project;
- preserve negative results and distinguish proofs from bounded experiments;
- use deterministic policy first and fail closed when evidence is unresolved;
- build small adapters when there is a concrete interoperability need.

For adapter work, the aim is compatibility—not a new dependency: preserve the
host project's policy and data model, expose missing trust information clearly,
and keep provider-specific implementations behind neutral interfaces.
