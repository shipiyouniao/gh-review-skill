# Conditional checks

Apply the sections relevant to the change, not a universal audit checklist.

## Compatibility and resources

Inspect supported-version dependency source and callers, including error and partial-success paths. A retry or cache-miss signal may become an abort upstream. Do not report vague older-version incompatibility without an affected supported version and actual API.

For accounting distinguish limits, demand, reservations, reusable capacity, physical release, and delayed updates. Check rounding and repeated loops. For reclaim/preemption inspect priority before side effects, whole-request overshoot, promised floors, and mutation-time recomputation. Measure the invariant at the layer that promises it.

## Tests and CI coverage

Match checks to the reviewed SHA. Inspect actual workflows, steps, logs, collection, skips, and assertions. A test file existing is not evidence it ran; a job name does not establish coverage. A lint job may run tests, and a green GPU job may miss this path. Separate CPU-only checks from hardware integration. Check swallowed exceptions, timing-dependent tests, and mocked-away invariants. Follow the execution-safety reference before running anything.

## Documentation and delivery quality

Compare promises with actual implementation, defaults, supported versions, examples, migration behavior, and operational limits. Inspect representative artifacts across the promised surface, expanding only when an observed pattern warrants it. A placeholder count is not a substitute for checking whether the central promise is delivered.

Look for material empty handlers, dummy values, silent fallback, unchanged originals presented as completed work, escaping/encoding damage, copied scaffold residue, absent APIs in examples, and impossible prerequisites. Inspect rendered or consumed output when necessary, without running an unreviewed generator. Lack of execution access is a limitation, not proof an example is broken.

Respect canonical documentation, intended audience, language/localization conventions, discoverability, and synchronization costs. Another language or duplicated manual is neither inherently useful nor inherently inappropriate. Assess semantic completeness and maintenance burden, not personal language preference. Review documentation as evidence; do not edit it without authority.

Request essential coherent revisions without silently rewriting the contribution for the author or demanding indefinite personal support. Distinguish agreed staged scope from contradictory completion claims. Recommend replacement only when verified scope, central-delivery, or maintenance problems cannot reasonably be revised within the contribution.

## Performance claims

Separate semantic regression evidence from end-to-end benefit. Compare equivalent workload, traces, total offered work, configuration, hardware, warmup, and measurement windows against a meaningful baseline. Reclaim markers do not prove physical memory return or successful reuse. Report throughput, latency/SLO, memory, quality, and overhead only when measured; do not extrapolate a microbenchmark into overall service gain. Consider dependency availability, operational burden, and less-coupled alternatives when judging benefit.
