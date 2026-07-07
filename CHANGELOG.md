# Changelog

All notable changes to the operating layer and handover document.

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
