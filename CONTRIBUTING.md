# Contributing

The most valuable contribution is **field evidence**, not prose. This repo's core principle is that untested rules are decoration — so contributions should come with data.

## What to contribute

**1. Field failure reports (highest value).**
You deployed `OPUS-OPERATING-LAYER.md` and the model still failed in a way the doctrine should have prevented. Open an issue with:
- The (sanitized) prompt and relevant context
- What the model did vs. what the layer says it should have done
- Which section of the layer/handover should have caught it
- Your environment (harness, model version, how the layer was injected)

**2. New eval scenarios.**
A reproducible test targeting a failure mode the current suite misses. Follow the pattern in [`evals/`](evals/): isolated fixture, two-arm protocol (baseline vs. layer), pass criteria that can be verified from artifacts (checksums, row counts, test output) rather than from the agent's self-report.

**3. Adaptations to other models.**
Ports of the layer to other models are welcome as `adaptations/<model>.md` — but only with eval results attached. A port without measurements is a guess.

**4. Doc fixes.** Typos, broken links, clarity — straight PRs, no process.

## What not to contribute

- New rules without an observed failure that motivates them. The layer's value depends on staying short; every rule must earn its tokens with evidence.
- Eval scenarios whose pass criteria depend on judging the agent's prose rather than verifiable artifacts, unless artifact-based verification is genuinely impossible.

## Process

- Open an issue before large PRs.
- For layer changes: state the failure the change addresses, and re-run the affected eval scenario in both arms. Include the results in the PR description.
- Revision numbering: structural rule changes bump the minor version (4.1 → 5.0 if the layer's structure changes, → 4.2 for rule additions/rewording). Update `CHANGELOG.md`.
