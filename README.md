# Silent Partner Coding

Independent contributor working on reproducible agent security, evidence provenance,
and provider-neutral interoperability.

I prefer tested boundaries and explicit uncertainty to broad trust claims. Every
project here states its own disqualifying limitations — if you want to judge the
work quickly, read a limitations section before you read a README.

## Work merged into other people's projects

- **[bernstein](https://github.com/sipyourdrink-ltd/bernstein)** (928★) — 8 merged PRs
  building signed agent identity and per-tool-call attestation, against the maintainer's
  [issue #2931](https://github.com/sipyourdrink-ltd/bernstein/issues/2931): the
  provider-neutral interlock, native evidence provider, run-anchored signed identity,
  per-dispatch identity binding, run attestation receipts, evidence-gated artefact
  writes, and authenticated run closure. Ongoing — the `identity attest` CLI surface
  is still outstanding.
- **[pipelock](https://github.com/luckyPipewrench/pipelock)** (798★) — external
  reference verifier for mediated requests
  ([#1225](https://github.com/luckyPipewrench/pipelock/pull/1225), merged); authority
  verification before forwarding
  ([#1186](https://github.com/luckyPipewrench/pipelock/pull/1186), open).
- **[nxtlinq-attest](https://github.com/nxtlinqit/nxtlinq-attest)** — fail-closed
  handling for missing or empty attestation scope
  ([#1](https://github.com/nxtlinqit/nxtlinq-attest/pull/1), merged).

## Security review

- **[block/buzz #5515](https://github.com/block/buzz/pull/5515)** — review of a managed
  authorization integration. Reported that trusted-gateway state was granted from an
  executable basename, and that the managed installer was unpinned. Both were addressed.
  A later review of the manifest owner-review path is open on the same PR.

Open and awaiting review: [google-agentic-commerce/AP2 #318](https://github.com/google-agentic-commerce/AP2/pull/318),
[microsoft/agent-governance-toolkit #3563](https://github.com/microsoft/agent-governance-toolkit/pull/3563),
[block/buzz #4066](https://github.com/block/buzz/pull/4066).

## My own projects

- **[Minority Prophet](https://github.com/Silentpartnercoding/minority-prophet)** — how
  copied or commonly controlled claims should affect an evidence assessment.
  Preregistered experiments, reproducible records, machine-checked results with
  documented limits.
- **[Minority Prophet Border](https://github.com/Silentpartnercoding/minority-prophet-border)** —
  portable admission records binding identity, delegated authority, an exact proposed
  action, destination policy, evidence, and human intervention.
- **[Minority Prophet Gate](https://github.com/Silentpartnercoding/minority-prophet-gate)** —
  reference implementation of a deterministic-policy-first decision ladder.
- **[Agent Ablation Harness](https://github.com/Silentpartnercoding/agent-ablation-harness)** —
  measures whether assistance given to an agent changes the judgment it produces, using a
  blind control arm over frozen, hash-manifested evidence. Its §4 is the honest place to
  start: it lists every limitation that disqualifies a causal claim, including two the
  harness itself later had to fix.

These are research and reference implementations, not production certifications.
Evidence assessment does not grant authority, and a different name, key, service, or
verifier does not by itself establish independence.

## How I contribute

Start from the project's issue, policy, and maintainer-defined boundary. Check whether
the problem is already covered before proposing work. Keep changes narrow, testable, and
native to the host project. Preserve negative results and distinguish proofs from bounded
experiments. Use deterministic policy first and fail closed when evidence is unresolved.

For adapter work the aim is compatibility, not a new dependency: preserve the host
project's policy and data model, expose missing trust information clearly, and keep
provider-specific implementations behind neutral interfaces.
