# Validation and limitations

Initial release preparation: 2026-11-03.

## Instruction package

| Scope | Files | UTF-8 bytes | Whitespace-delimited words |
|---|---:|---:|---:|
| Entrypoint | 1 | 5,985 | 781 |
| Entrypoint and all references | 5 | 21,541 | 2,889 |
| Optional UI metadata | 1 | 288 | 36 |

These include Markdown and frontmatter, not repository context, tool output, system instructions, or model-generated text. They are not tokenizer counts. The package requires no executable helper, service, hook, or prescribed multi-agent workflow.

## Checks performed

- Frontmatter, skill name, relative links, whitespace, file inventory, and file hashes were checked. The skill-creator structural validator passed.
- Independent textual comparison with the fuller source instructions found no material loss of repository-fit assessment, public-API exception, evidence/uncertainty discipline, bounded implicit-load inspection, injection resistance, precise comment anchors, or publication authority.
- A fresh reviewer context used these exact instructions on six known synthetic changes. It did not receive earlier results or intended labels. It identified two justified public API repairs, three production-bug claims blocked by existing supported-path protections, and one unresolved vendor lifecycle premise.
- All six supplied regressions failed on the base snapshot and passed on the changed snapshot. Five existing API tests passed on both. Additional real public-path checks distinguished the valid repairs from private-helper counterexamples. Tests used Python 3.12.14 with isolated startup, site loading disabled, and no bytecode writes. All 104 input-file hashes remained unchanged.

This was a single known-case regression replay. The editor knew the cases, which had informed related earlier work. It is not an unseen benchmark or evidence of general accuracy improvement. The unavailable vendor lifecycle remained unresolved rather than being replaced with invented semantics. One timing-dependent test was observed in one run, not proved reliable for every interleaving.

Earlier CI and injection exercises on fuller source versions exposed missed pre-execution reads of harmless package initializers. Explicit implicit-load rules were then added and are retained here. Runtime-semantics probes confirm that such loads can execute; they do not show that reviewers reliably inspect every load. This compressed version has not completed a new adversarial safety benchmark.

## Not established

- No comparative accuracy, recall, latency, token-cost, or weaker-model advantage.
- No official Anthropic or Superpowers workflow run, matched repeated trial, or exhaustive compatibility study.
- No claim that these instructions prevent prompt injection or unsafe execution independently of host controls.
- No live review-publication mutation test, actual Actions runner test, hardware integration, or full test-runner discovery test for the synthetic replay.
- No automatic skill discovery or tool integration verification across all hosts.

The synthetic fixtures and raw traces are not included, so this release does not provide a self-contained public benchmark reproduction. Only the instruction package, normal project documentation, and this bounded summary are distributed. Earlier real-PR source and dependency trees used for research are not part of this repository.
