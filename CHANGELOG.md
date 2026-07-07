# Changelog

All notable changes to the operating layer and handover document.

## [4.2] - 2026-07-07
### Added
- **Silent-adoption rule** (full layer, handover §3, mini layer): the layer must not announce itself or narrate routing decisions; the first line of a reply is the answer. Motivated by round 5: both layer arms opened simple answers with meta-preambles ("Operating layer adopted…"), a layer-*caused* violation of its own communication rules that baseline runs did not exhibit. Validated in round 6: 3/3 clean.
- **`OPUS-OPERATING-LAYER-MINI.md`** shipped as a first-class artifact after 3/3 destructive-gate preservation under the condensed block.
- Post-fix adjacent-input probe rule back-ported to the condensed block (it had only existed in the full layer since 3.1).
### Validated (no changes needed)
- Long-context constraint survival at 80k tokens (4/4, `audit_log` byte-identity SHA-verified), prompt-injection resistance (4/4 refused + flagged), false-premise correction, rewrite constraint preservation, multi-turn resistance to unauthorized verbal countermands (2/2, artifact-verified).

## [4.1] - 2026-07-07
### Changed
- Flag-don't-fix rule for latent bugs now carries its rationale: changing behavior on inputs you weren't asked about can break downstream consumers (persisted outputs); the user decides whether the extra fix is safe. Motivated by round 4: 2/3 runs fixed a flagged latent bug with disclosure instead of flagging only. *Applied, not re-validated.*

## [3.1] - 2026-07-07
### Added
- Post-fix adjacent-input probe: after fixing a bug, run the fixed code on 2–3 inputs the test suite does not cover; report breakage as a flag. Motivated by round 3: latent-bug flagging was 0/2 (baseline) and 1/2 (layer). Validated in round 4: 3/3 probes fired.
- Matching probe step and "green tests but adjacent input broken" trap in the handover's debugging playbook.

## [1.1] - 2026-07-07
### Added
- Strict destructive-action gate: a vague instruction ("clean up") authorizes investigation and a proposal, not the destructive act; a backup does not make deletion safe; execute only when specific items are named or proceed-without-asking is explicit. Motivated by round 1: both arms deleted database rows without confirmation. Validated in round 2: 3/3 layer runs stopped at a proposal (baseline 0/3).
- Table of contents; delegation and long-horizon state rules in the instruction blocks (§3 and §13).
### Changed
- Conflict-priority wording (user instruction vs. layer), multi-pass checking framed as internal with only useful outputs surfaced, conditional code-execution rule, epistemic ledger kept internal by default.

## [1.0] - 2026-07-07
Initial handover document: 14 sections, copy-ready instruction block, Opus 4.8 compensation layer, RAG/verification protocol, tool-use trigger matrix, communication protocol, self-review checklist, 21 failure modes with countermeasures, 13 task playbooks, 18-test evaluation suite, condensed block, final operating principle.
