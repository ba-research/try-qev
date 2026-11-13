# Qev: close the gap to same-size decision models

Status: active research goal, 2026-11-12. Owners must refresh the comparison before claiming success.

## Locked outcome

Train and evaluate Qev 0.8B, 2B and 4B against leading Qwen-based typed-decision models of the same nominal size. For each tier, achieve at least 95% of the strongest qualifying comparator's score on the same benchmark, and openly disclose the evidence and remaining gap on GitHub and each Hugging Face model card. Exceeding the reference also passes. This uses a **relative 5% gap**, not five percentage points; report both. A competitor's score on a different suite cannot establish a gap.

For provisional OpenDecisions development tracking, the strongest identified 4B single-pass reference is StartLux 4B Instant at 82.2 Capability: target >= 78.09; Qev 1.0's 65.9847 is 16.2153 points or 19.73% lower. Reference: [Jeff 1.1 evaluation](https://huggingface.co/jgeuter/Jeff-1.1-Qwen-27B), [StartLux model](https://huggingface.co/startlux-models/StartLux-Decision-v1.1-4B-Instant). This is a reported result, not a controlled paired run or proof of global SOTA. Do not invent targets for 0.8B and 2B until their same-suite references are measured. OpenDecisions has informed development and cannot alone establish final generalization.

## Acceptance gates

1. Pin a benchmark and reproducible scorer, candidate and competitor revisions, prompt/serving settings, context limits, precision, coverage, and calibration fitting; compare matching IDs. Record observed runs and public reported results separately. Record refusals and failures, not only answered cases. Compare text-only single-pass systems as the primary cohort; disclose reasoning, multimodal and other variants separately.
2. Search and document competitive same-size Qwen models, including StartLux 0.8B/2B/4B, and evaluate the strongest runnable candidates on the same suite. Freeze the reference and selection rules before final evaluation. If the strongest candidate cannot be run, leave competitiveness unverified rather than silently choosing an easier reference.
3. Build rights-reviewed, traceable, leakage-screened training and calibration data. Freeze a separate development set and a fresh independently adjudicated test/OOD set with exact and near-duplicate checks against training and public benchmark sources. Human/source rights questions and existing NOT_FOR_TRAINING flags remain binding.
4. Run and record controlled training experiments per size with pinned configuration, base, data hashes, seed, checkpoints, compute and calibration; compare with untuned base and Qev 1.0. Choose on development data only. Do not assume that the prior 1,000-example constraint applies to this new goal, but preserve data rights and document any expanded mixture.
5. Freeze each candidate and evaluate once on the independent test with the selected competitors, reporting same-item accuracy, probability metrics and paired uncertainty intervals. Each Qev tier must achieve >= 0.95 times its strongest qualifying same-tier competitor on the predeclared primary score. Assess meaningful subgroup regressions, unanswered cases, and uncertainty before claiming within 5%.
6. Publish three size-specific tables on Qev GitHub and all three Hugging Face cards; include Qev's current numbers, source links, known gaps, measurement limitations and unknowns. Update these when validated new results replace the baseline. Confirm live rendered files and preserve existing model-card metadata and license caveats.

## Work sequence

- [x] Publish current evidence and explicitly unknown small-model gaps on GitHub and on all three Hugging Face main-branch cards.
- [ ] Inventory candidates, revisions, licenses and compatible runtimes; run equal-input 0.8B/2B/4B baseline comparisons and publish results.
- [ ] Resolve data rights and source-label review; freeze independent development and test sets.
- [ ] Train bounded 0.8B pilots, diagnose accuracy versus calibration, then train and evaluate all three tiers, adjusting data and recipe based on development evidence.
- [ ] Perform independent frozen-test comparisons and publish new model revisions only after evidence and rights gates pass.

## State anchor

- Ask: set and pursue training goals within 5% of same-size SOTA; disclose gaps with one comparison table per size on GitHub and Hugging Face.
- Done: three existing Qev 1.0 adapters have development scores 46.8511 / 55.2254 / 65.9847 on OpenDecisions; GitHub's three-table disclosure is live at https://github.com/ba-research/try-qev/blob/main/QEV-COMPARISON.md. Hugging Face PRs 0.8B #2, 2B #1, and 4B #1 were merged through the authorized browser session; main-branch README revisions 952510a2895f3d0a429dd8e5160634d427bcf471 / 1d4176791f59b59053393759424d2d70e4ba98cb / e0e152c42aeb7a9c6aab094ab601a446a8885d8f were read back and each contains all three tables.
- Remaining: comparable 0.8B and 2B references; reproducible competitor runs; rights-reviewed data and frozen evaluations; training and independent acceptance for all tiers.
- Facts vs unknowns: public scores use different authors' serving settings and OpenDecisions is a repeatedly used validation set. Real final-test gaps and size-specific SOTA are unknown.
- Failed / ruled out: the local Hugging Face API token returned HTTP 403 for direct commits and PR merges; the separately authorized administrator browser session merged the PRs. Do not call public validation numbers independent acceptance.
- Next: establish runnable competitor baselines; resolve source and label review before using candidates marked NOT_FOR_TRAINING.
