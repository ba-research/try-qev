# Qev 1.0: comparison with same-size decision models

Snapshot: 12 November 2026. Qev's [OpenDecisions](https://huggingface.co/datasets/jgeuter/OpenDecisions) results use a 2,352-item development set, not a fresh independent test. Capability averages the benchmark's intelligence and calibration scores; it is not accuracy. Public-231 accuracy is a separate local diagnostic detailed below. Unless marked local, competitor scores are reported by their authors or the benchmark authors using their own serving configurations. Tables list identified comparators, not a complete ranking or proof of global state of the art. Different benchmarks cannot be subtracted.

## 0.8B

| Model | Base | OpenDecisions Capability | Public 231 accuracy | Typed-decisions accuracy | Comparison to Qev 1.0 0.8B |
| --- | --- | ---: | ---: | ---: | --- |
| [Qev 1.0 0.8B](https://huggingface.co/ba-research/Qev1.0-Qwen3.5-0.8B) | Qwen3.5-0.8B | 46.85 | 56.28% | 43.50%† | Our development result |
| Experimental local 0.8B pilot | Qwen3.5-0.8B | 50.45 | 56.28% | 58.15%† | Unreleased workflow-trained pilot; preliminary, not independently accepted |
| [Kev 0.8B](https://huggingface.co/jaredpalmer/kev-0.8b) | Qwen3.5-0.8B-Base | Not verified | — | — | 14,032 monthly downloads; same-suite gap unknown |
| [StartLux 1.1 0.8B Instant](https://huggingface.co/startlux-models/StartLux-Decision-v1.1-0.8B-Instant) | Qwen3.5-0.8B | Not verified | — | — | Gap unknown; same-suite run needed |
| [AA Decision 0.8B](https://huggingface.co/analogalok/Qwen3.5-0.8B-AA-Decision) | Qwen3.5-0.8B | Not verified | — | — | Gap unknown; card reports different benchmarks |
| [labqoat QEV 0.8B](https://huggingface.co/labqoat/qev-0.8b) | Qwen3.5-0.8B | Not verified | — | — | Different project; gap unknown |

## 2B

| Model | Base | OpenDecisions Capability | Public 231 accuracy | Typed-decisions accuracy | Comparison to Qev 1.0 2B |
| --- | --- | ---: | ---: | ---: | --- |
| [Qev 1.0 2B](https://huggingface.co/ba-research/Qev1.0-Qwen3.5-2B) | Qwen3.5-2B | 55.23 | 63.64% | 56.10%† | Our development result |
| [Valen Decision 1.5 2B](https://huggingface.co/Valen-Team/Valen-Decision-1.5-2B) | Qwen3.5-2B | — | 81.39% | — | Local public-231 run; 17.75 points above Qev 2B |
| [Decider 2B](https://huggingface.co/Mapika/decider-2b) | Qwen3.5-2B-Base | Not verified | — | — | 7,391 monthly downloads; same-suite gap unknown |
| [StartLux 1.1 2B Instant](https://huggingface.co/startlux-models/StartLux-Decision-v1.1-2B-Instant) | Qwen3.5-2B | Not verified | — | — | Gap unknown; same-suite run needed |
| [joey-1](https://huggingface.co/baselabs/joey-1) | Qwen3.5-2B | Not verified | — | — | Gap unknown; same-suite run needed |
| [Jev-Style 2B Decision v3](https://huggingface.co/chaoliangUNSW/Jev-Style-2B-Decision-v3) | Qwen3.5-2B | Not verified | — | — | Gap unknown; same-suite run needed |

## 4B

| Model | Base | OpenDecisions Capability | Public 231 accuracy | Typed-decisions accuracy | Comparison to Qev 1.0 4B |
| --- | --- | ---: | ---: | ---: | --- |
| [StartLux 1.1 4B Instant](https://huggingface.co/startlux-models/StartLux-Decision-v1.1-4B-Instant) | Qwen3.5-4B | 82.2 | — | — | 16.22 points above Qev; 19.73% relative gap |
| [Kev 4B](https://huggingface.co/jaredpalmer/kev-4b) | Qwen3.5-4B-Base | Not verified | — | — | 12,499 monthly downloads; same-suite gap unknown |
| [Jeff 1.1 Qwen 4B](https://huggingface.co/jgeuter/Jeff-1.1-Qwen-27B) | Qwen3.5-4B | 79.3 | — | — | 13.32 points above Qev |
| [Wald 4B v2.0](https://huggingface.co/datasets/jgeuter/OpenDecisions/blob/main/README.md) | Qwen3.5-4B | 77.1 | — | — | 11.12 points above Qev; some questions use reasoning |
| [Torchcast decision 4B v1.1](https://huggingface.co/datasets/jgeuter/OpenDecisions/blob/main/README.md) | Qwen3.5-4B | 73.5 | — | — | 7.52 points above Qev |
| [decider 4B v2](https://huggingface.co/datasets/jgeuter/OpenDecisions/blob/main/README.md) | Qwen3.5-4B | 70.8 | — | — | 4.82 points above Qev |
| [Open Decider 4B typed specialist](https://huggingface.co/mvbalaji/od1-typed-decisions) | Qwen3.5-4B | — | — | 79.60% | Author-reported; trained on benchmark workflows |
| [Jeff 1.0 Qwen 4B](https://huggingface.co/jgeuter/Jeff-1.0-Qwen-4B) | Qwen3.5-4B | 68.0 | — | — | 2.02 points above Qev; model-card figure |
| [Qev 1.0 4B](https://huggingface.co/ba-research/Qev1.0-Qwen3.5-4B) | Qwen3.5-4B | 65.98 | 68.40% | 64.50%† | Our development result |
| [nanohunch decider 4B](https://huggingface.co/ubermenchh/nanohunch-decider-4b) | Qwen3-4B | 57.1 | — | — | 8.88 points below Qev; four-seed mean, different Qwen generation |

The 82.2 and 79.3 results are reported in [Jeff 1.1's same-set evaluation table](https://huggingface.co/jgeuter/Jeff-1.1-Qwen-27B). The [OpenDecisions leaderboard](https://huggingface.co/datasets/jgeuter/OpenDecisions/blob/main/README.md) reports 67.7 for Jeff 1.0, versus 68.0 on its model card. Different service configurations can affect results; differences around two points should not be treated as decisive. Our 4B target against the identified 82.2 reference is at least **78.09 Capability** (95% of 82.2); Qev 1.0 does not meet it. This is a provisional validation target, not proof of generalization. We have no measured OpenDecisions SOTA gap or numeric target for 0.8B or 2B yet.

Download counts are Hugging Face's rolling monthly counts observed 12 November 2026 for the linked original repositories, not deduplicated people, quality measurements or sums across quantizations. Kev and Decider are included because of their adoption and relevance; popularity itself does not establish they are the strongest on this benchmark.

We are pursuing fresh, leakage-screened paired evaluations and improved training at all three sizes. Existing Qev training source provenance, rights and independent generalization remain unresolved; see the individual model cards. We will update these tables when comparable, reproducible evidence is available.

The evaluation plan targets at least three typed-decision benchmarks: OpenDecisions, [JevBench's public 231-item subset](https://huggingface.co/datasets/kshitijthakkar/nirnaya-jevbench-public-eval-v1), and [typed-decisions](https://huggingface.co/datasets/LocalLLaMA/typed-decisions) (2,000 test questions). The public-231 diagnostic results above are accuracy, not OpenDecisions Capability; all three Qev typed-decisions results are preliminary local diagnostics. Typed-decisions uses teacher-derived targets; some competing models train on its training split, so distinguish specialists from generalists. None of the OpenDecisions gaps can be transferred to another benchmark. The public 231 subset is not the full sealed JevBench leaderboard.

Public-231 figures are preliminary local diagnostics on the same 231 published items, matched by ID to the pinned upstream source; accuracy is correct / 231, with unsupported Qev cases counted wrong. Qev 0.8B/2B/4B each refused 36 overlength inputs at their 2,048-token limit and answered 195; their answered-only accuracies were 66.67% / 75.38% / 81.03%. Valen 2B answered all 231. At 95% of Valen's 81.39%, the provisional 2B target on this suite is 77.32%; Qev 1.0 is 13.68 points below that target. We used each model's native decision interface and different prompt renderings; the Qev and Valen score adapters have not been independently certified against the upstream benchmark scorer, and training/source overlap has not been fully audited. The 17.75-point gap is a provisional local observation, not a leaderboard rank or uncontaminated estimate.

† Typed-decisions: Qev 0.8B scored 870/2,000 decisions (43.50%), 2B 1,122/2,000 (56.10%), and 4B 1,290/2,000 (64.50%), using argmax of returned distributions; none refused a case. Qev used each question separately, and 200 Noul inputs without criteria were supplied explicit neutral No/Yes definitions. This conversion and our accuracy policy have not been independently certified against the official scorer. Brier/KL against teacher-derived soft targets were 0.2567/0.4553 for 0.8B, 0.2079/0.3884 for 2B, and 0.1369/0.2447 for 4B; our calculation reproduces the benchmark uniform Brier reference at 0.2382. The publisher reports a 47.0% prior baseline and an independently reported 0.8B workflow specialist at 75.1%, but the latter and the 4B specialist trained on the benchmark training workflows and used different request formatting. The published numbers are context, not controlled head-to-head results. [Dataset](https://huggingface.co/datasets/LocalLLaMA/typed-decisions); [specialist model card](https://huggingface.co/mvbalaji/od1-typed-decisions).

The local 0.8B pilot is a separate one-pass LoRA and head trained on 1,000 teacher-target decisions from the typed-decisions training workflows, with temperature fitted on separate scenarios. Its held-out typed test score is 1,163/2,000, with Brier 0.1377 and KL 0.2366. It scored 50.45 Capability on all 2,352 OpenDecisions development items and 130/231 on public-231; the same 36 overlength inputs were counted incorrect. Exact normalized scenario matches across its training and these evaluations were absent, but semantic overlap, scorer equivalence, rights and independent generalization remain unverified. It is not a released model or a clean independent benchmark result; the specialist's reported 75.1% uses a different setup.
