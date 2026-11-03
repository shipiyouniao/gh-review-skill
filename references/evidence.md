# Evidence and acceptance

Use the lowest real boundary that retains the disputed behavior. Keep the evidence record proportionate; it need not be a table.

## Follow the claim, not just the patch

Pin the supported version, configuration, input, and observable consequence. Trace backward from the symptom and forward from a supported entrypoint. Check initialization, registration, warmup/readiness, admission, normalization, ownership, locks, callbacks, retry/cancellation, and cleanup where they affect the premise. A registered callback shows a possible edge, not its timing relative to a barrier. A race needs a legally possible interleaving and a violated invariant.

For every critical edge or state cite inspected source, an applicable contract, or a relevant observation. Test the strongest plausible guard or alternative explanation. One complete supported witness can suffice; do not demand every caller. A missing search result, uninspected dependency, or unavailable runtime proves neither reachability nor impossibility. A guard on one configuration does not establish protection in all supported configurations.

## Test the actual boundary

Derive expectations from an independent contract or hand-checked example, not by copying the proposed algorithm. Internal-state assertions, ordering, arguments, and call counts are valid when grounded in that contract after a supported trigger. White-box assertions are not inherently invalid.

When safe and feasible, run the same focused regression on pinned base and head with identical inputs/configuration. Record commands and both results. The negative control must fail for the claimed behavioral reason, not a missing new API, import error, setup failure, or skip. A fixed-head pass alone proves neither the old defect nor its repair.

Identify real, replaced, and bypassed components. Direct field mutation, skipped constructors, invented callback ordering, or doubles that manufacture the disputed state can establish conditional local behavior without proving a supported trigger. Mocks may replace external or irrelevant machinery below the disputed boundary when their effects are independently grounded; they must not replace the behavior being proved. Do not mistake a reimplemented algorithm agreeing with itself for regression evidence.

Clearly distinguish static proof, a unit-level demonstration, native-path reproduction, and full integration coverage. Lack of hardware does not invalidate a complete static proof. It also does not turn a mock-only pass into production validation. Never require unsafe execution or an unnecessary full deployment.

## Public API exception

Establish the pre-existing promise from authoritative repository documentation, supported examples in context, or established compatibility behavior. Verify legal arguments, initialization, lifetime, ownership, and concurrency rules. Export visibility or a method mention is not an unrestricted contract. New PR documentation can propose a new guarantee, but cannot retroactively prove a pre-existing bug.

A supported public call violating a real promise has repair value without a known deployed consumer. Do not demand unrelated application reachability. Conversely, documentation is not proof of deployment or a mandate to accept every API change. Distinguish actual consumers and concrete risk from prospective value; absence of in-repository callers proves neither presence nor absence of external users. Compare the justified benefit with the size, compatibility risk, and ongoing obligations of the proposed change.

## Close gaps and choose a disposition

First inspect accessible callers, same-version public dependency source, defaults, history, and safe tests. Missing evidence in the description is not necessarily missing evidence in the project. Do not offload readily answerable investigation to the author.

Mark material premises established, contradicted, or unresolved with evidence or the exact missing fact. If a central production claim remains unsupported, require substantiation or an accurate narrowing; if contradicted, require correction. A separately valid API fix cannot silently excuse a misleading integration claim. Do not label a legal conditional integration as an ordinary default deployment.

Reflect material uncertainty in the final decision. Distinguish reviewer access limitations from concrete acceptance blockers; request changes only for a material actionable blocker and only when publication is authorized. Do not invent a bug, infer uselessness, or recommend approval merely to force a binary outcome. On changed heads verify author replies against code and classify each prior finding; a green child PR does not repair an inherited parent issue.
